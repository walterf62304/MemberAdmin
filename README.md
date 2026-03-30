# Setup Member Administrator
## Create Folders
- backend
  - db
  - repositories
  - routes
  - services
- frontend

## Prepare backend
### Initialize backend
```
cd backend
npm init -y
```
The file *package.json* has been created. 
### Install modules
```
npm install express cors better-sqlite3
```
### Implement 
- db: database access
- routes: message routing express
- sevices: business logic
## Prepare React frontend
```
# install build tool - global installation
npm install -g create-vite
npx create-react-app frontend
```
### Start server and React-app
```
cd backend
node server.js
cd ../frontend
npm start
```
## Compile application
```
# install build tool - global installation
npm install -g pkg
# build server package for Mac Apple Silicon M4
pkg -t node24-macos-arm64 server.js
# compile frontend
cd frontend
npm run build
```
# Client/server API
## Samples for HTTP GET/POST commands via CURL
```
curl -i -X GET http://localhost:3001/api/message \
-H "Content-Type: application/json"

curl -v -X POST http://localhost:3001/api/message \
-H "Content-Type: application/json" \
-d '{"message":"Test"}'
```
