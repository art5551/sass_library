# To Begin This Project

## Enter the following on the command line

1. Check npm installed / npm -v
2. Create the package.json / npm ini -y
3. Install sass globally / npm install -g sass
4. Install locally and save the app in the package.json file / npm install sass --save-dev
5. Check version and confirm sass was installed successfully / sass --version
6. Install parcel-bundler and save to json file / npm install parcel-bundler -save-dev

### Add following to package.json script:
    "dev": "parcel src/index.html",
    "build": "parcel build src/index.html"

## In development mode enter the following into command line to add scss to css file and open in development mode
     npm run dev

## When ready to push into production enter the following into command line to add scss to css file and optimize for production
    npm run build

## To rebuild node modules
    npm install
