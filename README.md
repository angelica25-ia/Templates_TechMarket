# Templates_TechMarket
primera evaluación Ciclo de vida del Software II  

# Flujo de trabajo con ramas
Para el desarrollo de este proyecto se utilizó una estrategia de control de versiones basada en ramas, con el objetivo de mantener un trabajo ordenado, colaborativo y sin conflictos.

*Se definieron las siguientes ramas:*
- master: contiene la versión final del proyecto lista para entrega.
- develop: rama de integración donde se consolidan los avances del equipo.
- feature/: ramas individuales para el desarrollo de funcionalidades específicas.

*Ejemplo de ramas utilizadas:*
- feature/build-template
- feature/test-template
- feature/deploy-template
  
*Flujo de trabajo*
1. Cada integrante crea su rama desde develop.
2. Se desarrollan los cambios de forma independiente.
3. Se realiza un Pull Request hacia develop.
4. Se revisan y consolidan los cambios.
5. Finalmente, se integran a master como versión final.

Este enfoque permitió mejorar la organización del trabajo, evitar conflictos y facilitar la colaboración entre los integrantes del equipo.

# Estructura de templates CI/CD #

Para este proyecto se implementó una estructura basada en plantillas reutilizables de GitHub Actions, ubicadas en la siguiente ruta:

.github/workflows/templates/

En esta carpeta se definieron los siguientes archivos:

- template_build.yml: encargado del proceso de construcción del proyecto.
- template_test.yml: orientado a la ejecución de pruebas automatizadas.
- template_deploy.yml: destinado al despliegue del sistema en distintos entornos.

Estas plantillas no se ejecutan directamente desde GitHub Actions, ya que están diseñadas para ser reutilizadas mediante workflow_call en otros workflows. Esta estrategia permite estandarizar los procesos de integración y despliegue continuo, facilitando la reutilización, mantención y escalabilidad de los pipelines en distintos proyectos o equipos.
