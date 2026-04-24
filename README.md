Templates_TechMarket
Primera evaluación – Ciclo de Vida del Software II
________________________________________
🌿 Flujo de trabajo con ramas
Para el desarrollo de este proyecto se utilizó una estrategia de control de versiones basada en ramas, con el objetivo de mantener un trabajo ordenado, colaborativo y sin conflictos entre los integrantes del equipo.
Se definieron las siguientes ramas:
- master: contiene la versión final del proyecto lista para entrega.
-	develop: rama de integración donde se consolidan los avances del equipo.
-	feature/: ramas individuales utilizadas para el desarrollo de funcionalidades específicas.
🔄 Flujo de trabajo
1.	Cada integrante desarrolla sus cambios en una rama feature.
2.	Se realiza un Pull Request hacia la rama develop.
3.	Los cambios son revisados y validados.
4.	Finalmente, se integran a master como versión final del proyecto.
________________________________________
⚙️ Estructura de templates CI/CD
Para este proyecto se implementó una estructura basada en plantillas reutilizables de GitHub Actions, ubicadas en la siguiente ruta:
.github/workflows/templates/
En esta carpeta se definieron los siguientes archivos:
- template_build.yml: encargado del proceso de construcción del proyecto.
-	template_test.yml: orientado a la ejecución de pruebas automatizadas.
-	template_deploy.yml: destinado al despliegue del sistema en distintos entornos.
Estas plantillas están diseñadas para ser reutilizadas mediante workflow_call, permitiendo su uso en distintos pipelines sin necesidad de duplicar código.
________________________________________
🔧 Uso de acciones externas
En las plantillas se integraron acciones externas provenientes de GitHub Marketplace, tales como:
-	actions/checkout: permite clonar el repositorio dentro del pipeline.
-	actions/setup-node: configura el entorno de ejecución para aplicaciones Node.js.
-	aws-actions/configure-aws-credentials: simula la configuración de un entorno de despliegue en la nube.
El uso de estas acciones permite acelerar la implementación de pipelines, evitando desarrollar funcionalidades desde cero y asegurando compatibilidad con estándares de la industria.
________________________________________
🔁 Parametrización de las plantillas
Las plantillas fueron diseñadas para ser reutilizables mediante el uso de parámetros configurables:
-	inputs: permiten definir valores como versión de Node, entorno o comandos de ejecución.
-	outputs: permiten retornar resultados entre jobs o workflows.
-	variables de entorno (env): facilitan la adaptación a distintos contextos de ejecución.
Gracias a esta parametrización, las plantillas pueden ser utilizadas en distintos proyectos sin necesidad de modificarlas, mejorando la escalabilidad y mantenibilidad.
________________________________________
🚀 Beneficios para el negocio
La implementación de estas plantillas estandarizadas no es solo una mejora técnica, sino una decisión estratégica para TechMarket basada en los siguientes pilares:
- Reducción de tiempos y costos (Eficiencia): Al utilizar plantillas preconfiguradas, el tiempo de configuración de CI/CD para nuevos microservicios se reduce de horas a minutos. Esto permite que el equipo de desarrollo se enfoque en el valor de negocio y no en la infraestructura (alineación con objetivos organizacionales).
- Mitigación de riesgos y reducción de errores: La estandarización de los pasos de build y test actúa como una red de seguridad técnica. Al forzar la ejecución de pruebas en cada workflow_call, reducimos el riesgo de "errores humanos" y despliegues fallidos en producción, lo que protege la reputación de la empresa y la continuidad del servicio.
- Escalabilidad y mantenimiento: Gracias a la parametrización (inputs/env), TechMarket puede escalar de 1 a 100 proyectos manteniendo una única fuente de verdad. Si es necesario actualizar una versión de seguridad en una acción externa, solo se modifica la plantilla base y el cambio se propaga a toda la organización instantáneamente.
- Optimización mediante Acciones Externas: La integración de componentes como aws-actions y setup-node del Marketplace garantiza que TechMarket utilice herramientas validadas por la comunidad, asegurando compatibilidad y actualizaciones de seguridad constantes sin costo de desarrollo interno.
- Cultura DevOps y colaboración: Estas plantillas crean un lenguaje común entre los equipos de Desarrollo y Operaciones. Al ser modulares y claras, cualquier equipo puede adoptar el estándar rápidamente, fomentando la agilidad operativa y la entrega continua de alta calidad.
________________________________________
🧠 Conclusión
El uso de plantillas reutilizables en pipelines CI/CD permite mejorar significativamente la eficiencia y agilidad en el desarrollo de software.
En este proyecto, se logró diseñar una estructura modular, clara y reutilizable, alineada con buenas prácticas de integración y entrega continua.
Estas soluciones permiten a TechMarket optimizar sus procesos, reducir tiempos de implementación y mejorar la calidad del software entregado.
________________________________________
📚 Referencias Bibliográficas (APA)
GitHub. (2024). Reusing workflows. GitHub Docs. Recuperado de https://docs.github.com/en/actions/using-workflows/reusing-workflows.
GitHub. (2024). GitHub Actions Documentation. Recuperado de https://docs.github.com/en/actions.
________________________________________
🤖 Declaración de uso de IA
Para la realización de esta evaluación, se utilizó la inteligencia artificial Gemini como herramienta de apoyo para la revisión de sintaxis YAML, validación de la estructura del documento y redacción de la justificación de negocio según la rúbrica institucional. Los conceptos técnicos y la lógica de los pipelines fueron desarrollados por el estudiante.
