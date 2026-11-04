# TAREA-IMT2220-GRUPO-10

Tarea Computacional de IMT2220 Cálculo para Ciencia de Datos (2026-2), Grupo 10.

**Integrantes:** Lucas Martín Chicao Carmona, Ignacio Andrés Osorio Orellana, Martín Ignacio Serrano Pizarro y Martin Antonio Von Gehr Campos.

## Estructura

```
informe/
  respuestas.tex     informe con el desarrollo y las respuestas
  plantilla.sty      estilo del equipo docente (no es necesario modificarlo)
  figuras/           figuras del informe; las generan los notebooks
notebooks/
  Problema1.ipynb    reconstrucción de una imagen
  Problema2.ipynb    red neuronal con dos capas ocultas
  datos_P1.npz, datos_P2.csv, datos_P2_g.csv
```

## Cómo trabajar

**Notebooks.** Se necesita Python con `numpy`, `matplotlib` e `ipykernel`:

```
pip install numpy matplotlib ipykernel
```

Abran los notebooks en VS Code y reemplacen cada celda `# TODO` por su código. Ejecuten siempre desde `notebooks/`, porque los datos se leen desde esa carpeta.

**Figuras.** Los notebooks las guardan en `informe/figuras/`. El informe las incluye con `\figura{...}` y, mientras no exista el archivo, muestra un recuadro que dice "Falta". Si cambian el nombre de una figura, cámbienlo en ambos lados.

**Informe.** Reemplacen cada `\pendiente` por su desarrollo y compilen desde `informe/` dos veces, para que se actualicen las referencias:

```
pdflatex respuestas.tex
```

También se puede compilar en Overleaf: suban la carpeta `informe/` comprimida con *New Project > Upload Project*.

## Reglas del código

- **Permitido:** operaciones básicas de `numpy` (arreglos, sumas, `@`, `reshape`, `np.sqrt`, `np.exp`, `np.log`, `np.linalg.norm`, números aleatorios), lectura de datos (`np.load`, `np.loadtxt`, `pandas.read_csv`) y `matplotlib`.
- **No permitido:** `np.linalg.solve`, `inv`, `pinv`, `lstsq` o `eig`, `scipy.optimize`, `sklearn`, `torch`, `tensorflow`, `keras` y `jax`.
- **Excepción:** en el Problema 1 se puede usar `np.linalg.solve` para los sistemas de (b), (c) y (d).

## Antes de entregar

- [ ] No quedan `\pendiente` ni recuadros "Falta" en el informe.
- [ ] Se borraron del informe las indicaciones y la sección "Ejemplos de uso".
- [ ] Ambos notebooks corren de principio a fin (*Reiniciar kernel y ejecutar todo*), sin errores.

Se entregan 5 archivos por Canvas:

- [ ] PDF del informe, con ambos problemas.
- [ ] `Problema1.ipynb`, ejecutado.
- [ ] `Problema2.ipynb`, ejecutado.
- [ ] PDF del notebook del Problema 1, con código y salidas.
- [ ] PDF del notebook del Problema 2, con código y salidas.

Para obtener el PDF de un notebook: menú `···` del notebook → *Exportar* → *HTML*, y luego abrir el `.html` en el navegador e imprimirlo como PDF.
