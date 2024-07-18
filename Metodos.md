
Para que las opciones del Menú puedan funcionar de acuerdo a lo requerido, se necesitara la programación de varios metodos
que haran el trabajo neceserio: 

```sql
--thisform.PorDes()
--thisform.PorValor()	
--thisform.PorPeso()
--thisform.PorBulto()	
--thisform.PorCod()
--thisform.PorUnd()

--Todos usan la misma logica

SELECT sqlcab2
SET ORDER TO ""

SELECT * FROM sqlcab2 into cursor sqlcab_orde ORDER BY Unidades desc


SELECT sqlcab_orde 

SELECT sqlcab2 
ZAP

INSERT INTO sqlcab2  SELECT * FROM sqlcab_orde 
	
SELECT sqlcab2  
GO TOP 
thisform.grdDetalle1.Refresh()
```
```sql
lpMenu = ThisForm.ocxMenu
lpMenu.Clear()
lpMenu.AddItem(101, "Por Despacho", 0 )
lpMenu.AddItem(102, "Por Valor", 0 )
lpMenu.AddItem(103, "Por Peso", 0 )
lpMenu.AddItem(104, "Por Bulto", 0 )
lpMenu.AddItem(105, "Por Código", 0 )
lpMenu.AddItem(106, "Por Unidades", 0 )
lpMenu.PopupAny()


IF EMPTY(lpMenu.SelectedItemID)
	RETURN .F.
ENDIF

DO CASE
	CASE lpMenu.SelectedItemID = 101 		
		thisform.PorDes()		
	CASE lpMenu.SelectedItemID = 102
		thisform.PorValor()		
	CASE lpMenu.SelectedItemID = 103
		thisform.PorPeso()
	CASE lpMenu.SelectedItemID = 104
		thisform.PorBulto()	
	CASE lpMenu.SelectedItemID = 105
		thisform.PorCod()
	CASE lpMenu.SelectedItemID = 106
		thisform.PorUnd()	
ENDCASE
```
```sql
CREATE CURSOR SQLCAB( ;
Fecha 		c(40),;
Fecha2 		c(12),;
Despachos	n(10),;
Valor		n(10,2),;
Bulto		n(10),;
Kg			n(10),;
Codigos		n(10),;
Unidades	n(10))
```
