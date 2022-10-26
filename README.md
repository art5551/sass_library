Check npm installed / npm -v
cmd line / npm ini -y
cmd line / npm install -g sass
cmd line / npm install sass --save-dev
cmd line / sass --version
cmd line / npm install parcel-bundler -save-dev

Added following to package.json script:
    "dev": "parcel src/index.html",
    "build": "parcel build src/index.html"

when in development
cmd line / npm run dev

when ready to push into production
cmd line / npm run build
