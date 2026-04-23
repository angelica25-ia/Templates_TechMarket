name: "Main Pipeline - TechMarket"

# Este workflow se dispara cuando haces push a master o develop
on:
  push:
    branches:
      - master
      - develop
  pull_request:
    branches:
      - master

jobs:
  # 1. Llamada a la plantilla de Construcción (Build)
  build:
    uses: ./.github/workflows/templates/template_build.yml
    with:
      node-version: '18'
      environment: 'dev'

  # 2. Llamada a la plantilla de Pruebas (Test)
  # Solo se ejecuta si el build termina correctamente
  test:
    needs: build
    uses: ./.github/workflows/templates/template_test.yml
    with:
      node-version: '18'
      test-command: 'npm run test'

  # 3. Llamada a la plantilla de Despliegue (Deploy)
  # Solo se ejecuta si el test termina correctamente
  deploy:
    needs: test
    uses: ./.github/workflows/templates/template_deploy.yml
    with:
      environment: 'development'
      region: 'us-east-1'
