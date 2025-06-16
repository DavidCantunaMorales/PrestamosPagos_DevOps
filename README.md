# Análisis de Colaboración

## Gráfico de Commits por Miembro
Cada miembro del equipo (David, Luis, Mateo, Sebas) ha contribuido con al menos 5 commits en sus respectivas ramas (david_dev_ecuador, luis_dev_espania, mateo_dev_corea, sebas_dev_costarica). Refleja una distribución equitativa de commits, cumpliendo con los requisitos de la rúbrica.

## Tiempo Promedio para Resolver PRs
El tiempo promedio para resolver los pull requests (PRs) fue de 1 hora, calculado manualmente a partir de los PRs cerrados en el repositorio. Este valor representa el tiempo transcurrido desde la creación hasta el merge o cierre de cada PR.

## Reflexiones

### ¿Cómo se resolvieron los conflictos de timezone?
Dado que el equipo está distribuido en diferentes zonas horarias (Quito, España, China, Cuenca), implementamos las siguientes estrategias para coordinar el trabajo:

- **Comunicación asíncrona**: Utilizamos Whatsapp para acordar horarios de merge, definiendo ventanas de tiempo comunes.
- **Notificaciones automáticas**: Configuramos GitHub Actions para enviar alertas a través de Slack o correo electrónico cuando se creaba o revisaba un PR, permitiendo una respuesta rápida a pesar de las diferencias horarias.
- **Ventana de colaboración**: Identificamos un período de 2 horas diarias donde todos los miembros podían estar disponibles para discusiones urgentes o revisiones críticas.

### ¿Qué pasaría si el equipo en China no tiene acceso a Docker Hub?
Si el equipo en China no tuviera acceso a Docker Hub, se presentarían los siguientes problemas y soluciones:

- **Impacto**: La imposibilidad de descargar imágenes base (como python:3.9 o node:16) o de publicar imágenes generadas interrumpiría el flujo de CI/CD configurado en GitHub Actions.
- **Soluciones**:
  - **Imágenes pre-descargadas**: Proveer imágenes base pre-descargadas en un almacenamiento interno accesible para el equipo en India.
  - **Construcción offline**: Modificar el Dockerfile para usar paquetes locales o cachés, aunque esto podría limitar la portabilidad.

**Recomendación**: Incluir un plan de contingencia en el README del proyecto, con instrucciones claras para configurar un registro alternativo en caso de restricciones de acceso.

## Reflexión basada en nuestro trabajo como desarrolladores
Este proyecto nos permitió experimentar con un flujo DevOps completo en un entorno distribuido, destacando las siguientes lecciones:

- **Convenciones claras**: Las ramas nombradas por región (david_dev_quito, sebas_dev_cuenca, etc.) facilitaron el seguimiento del trabajo, pero requirieron una convención estricta para evitar conflictos.
- **Automatización eficiente**: La configuración de GitHub Actions para pruebas automáticas y builds de Docker redujo errores manuales, aunque demandó tiempo inicial para su correcta implementación.
- **Colaboración intercultural**: Adaptarnos a diferentes zonas horarias y estilos de trabajo nos enseñó a ser más empáticos y precisos en la comunicación. Por ejemplo, los comentarios en los PRs debían ser detallados para evitar malentendidos entre regiones.
