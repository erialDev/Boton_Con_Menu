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
