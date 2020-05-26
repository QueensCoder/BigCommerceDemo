# oBundle notes

# install

npm i bigcommerce/stencil-cli >> install cli in a dir

git clone https://github.com/bigcommerce/cornerstone.git >>clone template

cd cornerstone && npm i - make another node_modules for app to run in

need to add presolve to package.json due to missing resolve dependencies

add to package.json

{
// Your current package.json
"scripts": {
// Your current package.json scripts
"preinstall": "npx npm-force-resolutions"
},
"resolutions": {
"graceful-fs": "4.2.3"
}

npm i

stencil ci does not work with a newer version of node
need to revert node v to 8 >= version < 11.0.0

### runnig app - must run these stencil init, and stencil start inside of corner stone dir

stencil start may not work do the bad/ill-maintianed dependencies

delete node_modules and npm update if itwill not start

to push remove inner gitignore and move its content to outer gitignore

    - this is done because stencil cli is not globally installed

stencil start will spin the app up
provide api key/oauth access token

### stencil commands

init Interactively creates a .stencil, which configures how to run a BigCommerce store locally.
start Starts up the BigCommerce store, using theme files in the current directory.
bundle Bundles up the theme into a structured .zip file, which can be uploaded to BigCommerce.
pull Pulls the theme configuration config.json file from the live store and updates the local configuration.
push Bundles the theme into .zip file; then directly uploads the .zip to BigCommerce.
release Creates a new release in a theme’s GitHub repository.
help Displays help and returns all the options available to use for the specified command.
