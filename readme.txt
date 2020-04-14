How to compile:

-Download Visual Studio Code
-Run npm init to initialize package.json
-Install two packages (express & mysql)
npm install express mysql
-Create an entry point (index.js)
-Bring in express and mysql
const express = require('express')
const express = require('mysql')
-Initialize express
-You want app to listen on a port
app.listen(5000, () => console.log('Server started'););
-This will run server
node index.js
-Cancel it with ctrl + C
-Implement database
-Create variable called db
const db = mysql.createConnection({
host: 'localhost',
user: <insert username>
password: <insert password>
database: <insert database>
-Create route using get
app.get('/users', (req, res) => {
const sql = 'SELECT * FROM users';

db.query(sql, (err, result) => {
if(err) throw err;

});
});
-Run node.index
-Server started
-Go back to browser and type 'localhost:5000/users' in browser




