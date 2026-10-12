# NSS-Parcial1-Surge 🚀

**1er Parcial de Electiva 2 (DevOps) - ITLA**

Hecho por Nicole Alejandra Santana Sánchez, matrícula 2025-1213.

Profesor: Elvis Cruz.

## ¿De qué trata?

De integración continua con GitHub Actions y Surge.sh. O sea, cada vez que hago `git push` a la rama `main`, GitHub Actions publica mi página solita en Surge, sin que yo suba nada a mano.

## ¿Dónde la veo?

👉 https://nicky-electiva2-parcial1.surge.sh

## ¿Cómo está organizado?

```
NSS-Parcial1-Surge/
├── .github/
│   └── workflows/
│       └── main.yml   → la integración continua con GitHub Actions
├── index.html         → la página con el Hola Mundo
└── README.md          → esto que estás leyendo
```

## ¿Cómo funciona?

1. Escribo la página en mi compu, en mi repositorio local.
2. Hago `git push` a GitHub.
3. GitHub Actions lee el archivo `.github/workflows/main.yml` y arranca solo en una máquina virtual de Ubuntu (el *runner*).
4. Clona el repositorio, instala Node.js y Surge, y publica la página.

## ¿Y la clave de Surge? 🔒

Pues no está en el código. Guardé mi correo y mi token como **secrets** en GitHub (`SURGE_LOGIN` y `SURGE_TOKEN`), así nadie los ve, pero GitHub Actions sí los puede usar.