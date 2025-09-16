# Hola, soy Santiago Contreras 

name: Snake
on:
  schedule: [{ cron: "0 3 * * *" }]   # diario 03:00 Bogotá
  workflow_dispatch:
permissions:
  contents: write
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Generar snake
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: santiago-contreras   # <-- tu usuario exacto de GitHub
          outputs: |
            dist/snake.svg
            dist/snake-dark.svg?palette=github-dark
      - name: Publicar a rama output
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}


Estudiante de Ingeniería de Sistemas (Bogotá). Construyo backend con **Java / Spring Boot**, trabajo bases de datos **MySQL/PostgreSQL**, automatizo con **Selenium** y mido calidad con **SonarQube**. También desarrollo con **React Native**, **TypeScript**, **Python** y **Node.js**.

## Ahora
-  **sistema_alquileres** (Spring Boot + Thymeleaf + MySQL)
-  **HealthOne** (ERD + normalización a 3NF)
-  Automatización con **Selenium** y pruebas de integración

## Tech
Java • Spring Boot • Maven • JPA/Hibernate • MySQL/PostgreSQL • Thymeleaf • JUnit5 • Mockito • Docker • GitHub Actions • React Native • TypeScript • Python • Node.js

## Proyectos destacados
-  **Sistema de Alquileres** — roles (admin/visor/empresa), reportes y CRUD completo.  
-  **HealthOne DB Design** — modelo entidad-relación, 2NF/3NF y documentación.  


> Cuando publique/abra cada repo aquí, los fijaré en el perfil (Pins) para acceso rápido.

## Cómo trabajo
- Commits con **Conventional Commits** (`feat:`, `fix:`, `docs:`).  
- CI con **GitHub Actions** (build + tests).  
- Cobertura con **JaCoCo** y reportes en PR.  
- Issues/PRs con plantillas y roadmap breve.

## Contacto
[LinkedIn](https://www.linkedin.com/in/santiago-contreras-chillsanto) • [Email](mailto:santocontreras22003@gmail.com)


