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

stencil start may not work do the bad/ill-maintianed dependencies

delete node_modules and npm update if itwill not start
