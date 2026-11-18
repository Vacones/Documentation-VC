# Modeling
_Nota: Esta fase se siguió en su forma pura, sin ninguna adaptación **(esta es la etapa en la que el equipo sigue trabajando)**_

Por cada modelo se incluye una carpeta con su respectiva documentación.

## Modelos
Listados en el orden en que se desarrollaron:

1. **[modelo_sin_cajas](modelo_sin_cajas/)**: ResNet18 que clasifica el BCS a partir de la fotografía completa de la vaca.
2. **[modelo_con_cajas](modelo_con_cajas/)**: detector YOLO de la vaca y la grupa, más EfficientNet-B0 que clasifica el recorte de la grupa.
3. **[con_cajas_ordinal](con_cajas_ordinal/)**: EfficientNet-B0 + CORAL sobre el recorte de la grupa, tratando el BCS como escala ordenada y evaluando por vaca con validación cruzada.
4. **[DinoV2+LDL](DinoV2%2BLDL/)**: extractor DINOv2 que predice una distribución de probabilidad sobre los niveles de BCS.
5. **[DinoV2+Ridge](DinoV2%2BRidge/)** **(modelo final)**: detector de la grupa, extractor DINOv2-S y regresión ridge; entrega una predicción por vaca a partir de varias fotos.

Los modelos `DinoV2+LDL` y `DinoV2+Ridge` no tienen documento de Test Design propio, ya que reutilizan el protocolo de validación cruzada por vaca definido en `con_cajas_ordinal`.

## Orden de lectura de los documentos
1. Select Modelling Technique
2. Test Design
3. Model Description
4. Model Assessment
