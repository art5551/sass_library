# [Sass:Documentation](https://sass-lang.com/documentation/)

# To Begin This Project

## Enter the following on the command line
<br>  

1. Check to see if npm is installed / npm -v

2. Create the package.json / npm ini -y

3. Install sass globally / npm install -g sass

4. Install locally and save the app in the package.json file / npm install sass --save-dev

5. Check version and confirm sass was installed successfully / sass --version

6. Install parcel-bundler and save to json file / npm install parcel-bundler -save-dev

<br>

### Add following to package.json script:
<br>
    
    "scripts": {
        "dev": "parcel src/index.html",
        "build": "parcel build src/index.html"
    },

## In development mode enter the following into command line to add scss to css file and open in development mode
<br>
    
     npm run dev

## When ready to push into production enter the following into command line to add scss to css file and optimize for production
<br>
    
    npm run build

## To rebuild node modules
<br>
    
    npm install
