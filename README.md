# Templates_TechMarket
primera evaluación Ciclo de vida del Software II  

# Flujo de trabajo con ramas
Para el desarrollo de este proyecto se utilizó una estrategia de control de versiones basada en ramas, con el objetivo de mantener un trabajo ordenado, colaborativo y sin conflictos.

*Se definieron las siguientes ramas:*
- master: contiene la versión final del proyecto lista para entrega.
- develop: rama de integración donde se consolidan los avances del equipo.
- feature/: ramas individuales para el desarrollo de funcionalidades específicas.
  
*Flujo de trabajo*
1. Se desarrollan los cambios de forma independiente.
2. Se realiza un Pull Request hacia develop.
3. Se revisan y consolidan los cambios.
4. Finalmente, se integran a master como versión final.

# Estructura de templates CI/CD #

Para este proyecto se implementó una estructura basada en plantillas reutilizables de GitHub Actions, ubicadas en la siguiente ruta:

.github/workflows/templates/

En esta carpeta se definieron los siguientes archivos:

- template_build.yml: encargado del proceso de construcción del proyecto.
- template_test.yml: orientado a la ejecución de pruebas automatizadas.
- template_deploy.yml: destinado al despliegue del sistema en distintos entornos.

