# Satisfacción y lealtad del cliente en telefonía móvil: modelo SEM (ECSI)

Inferencia Avanzada y Análisis Multivariado - Unidad 3. Autor: Francisco Mario Campo Torne.

Modelo de ecuaciones estructurales basado en covarianzas, estimado por máxima verosimilitud,
sobre datos reales del índice europeo de satisfacción del cliente (ECSI) para telefonía móvil:
250 clientes, 21 indicadores en escala de 1 a 10 y cinco constructos latentes.

**Pregunta:** ¿la cadena imagen → expectativas → calidad percibida → satisfacción → lealtad
explica la permanencia de los clientes?

## Ejecución

```bash
python -m venv .venv
.venv\Scripts\activate          # macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook SEM_ECSI_Satisfaccion_Lealtad.ipynb
```

Kernel > Restart & Run All. Tiempo aproximado: 1 a 4 minutos. Semilla fija: 2026.
GitHub muestra el cuaderno ya ejecutado, con tablas y figuras, sin instalar nada.

## Fases del cuaderno

1. Datos: calidad, descriptivos y normalidad multivariada.
2. Modelo de medición (CFA): cargas, alfa, fiabilidad compuesta y AVE.
3. Hipótesis estructurales registradas antes de estimar.
4. Modelo estructural: contraste ECSI completo (M1) y modelo final mediado (M2).
5. Mediación con bootstrap de percentiles (1000 remuestras).
6. Validez discriminante (Fornell-Larcker y HTMT) y predictiva (validación cruzada, Q²predict).
7. Contraste de hipótesis.
8. Trazabilidad: verificación automática de las 90 cifras citadas en el informe.

Las tablas y figuras se exportan en `resultados/` (CSV separados por punto y coma).

## Datos

Conjunto ECSI de telefonía móvil (Tenenhaus et al., 2005), distribuido en el paquete `seminr` de R.
