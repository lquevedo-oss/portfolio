# Facturas e inventario · validación antes de aplicar

**Problema:** pasar de una factura a movimientos de inventario exige reconciliar cantidades, identificar productos y resolver ambigüedades antes de guardar cambios.

**Trabajo:** un esquema de extracción, normalización de unidades, reconciliación de totales, estados de aprobación y verificación de movimientos. La utilidad separa la validación de la ejecución.

**Código público:** validador reutilizable y fixture completamente sintético. Se excluyeron fotografías, documentos tributarios, catálogos, costos, proveedores, equivalencias y registros del negocio.

**Resultado técnico:** validaciones locales que detectan diferencias de totales, stock simulado inconsistente y estados aplicados sin aprobación o registro. Los ejemplos no actualizan inventario real.

**Límite:** el validador no realiza OCR ni infiere aprobación. El usuario debe revisar la extracción y el emparejamiento antes de cualquier carga.
