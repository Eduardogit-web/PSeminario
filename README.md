# Amazon Fine Food Reviews: Predicción de Utilidad con NLP

## Pregunta de Negocio
**¿Es posible predecir la probabilidad de utilidad de una reseña de e-commerce basándose en sus atributos textuales y su coherencia con la calificación, para priorizar automáticamente el contenido de alta calidad y mejorar la experiencia de compra?**

### Justificación
La plataforma de Amazon recibe miles de reseñas diarias. La utilidad actual se mide de forma reactiva (esperando votos de otros usuarios). Este proyecto busca identificar proactivamente las reseñas valiosas mediante ingeniería de características, permitiendo que el contenido de calidad sea visible de inmediato, aumentando la confianza del consumidor y optimizando las decisiones de compra.

---------

## Estructura del Repositorio

```text
├── arvhive/               # Datasets originales y procesados
│   ├── database.sqlite
│   ├── Reviews.cvs     # Datos crudos (CSV original)
│   └── hashes.txt      # Datos 
├── docs/               # Documentación técnica
│   └── ficha_dataset.md
├── notebooks/          # Compilacion clases datos (EDA)
├── src/                # Código fuente modular
├── .gitattributes      # Archivos Git LFS punteros
├── .gitignore          # Archivos excluidos del control de versiones
├── requirements.txt    # Dependencias del proyecto
└── README.md           # Descripción general
