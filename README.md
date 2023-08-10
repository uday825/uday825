npm init
npm install express
const express = require('express');
const app = express();
const port = process.env.PORT || 3000;

app.get('/', (req, res) => {
    res.send('Welcome to the Formula Backend');
});

app.get('/circle-area/:radius', (req, res) => {
    const radius = parseFloat(req.params.radius);
    if (isNaN(radius)) {
        res.status(400).send('Invalid radius');
    } else {
        const area = Math.PI * radius * radius;
        res.send(`The area of a circle with radius ${radius} is ${area.toFixed(2)}`);
    }
});

app.listen(port, () => {
    console.log(`Server is running on port ${port}`);
});
Create a .gitignore file in the project directory and add the following lines to exclude node_modules from version control:

Copy code
node_modules/
Initialize a Git repository and make your first commit:

csharp
Copy code
git init
git add .
git commit -m "Initial commit"
Create a new repository on GitHub without initializing with a README or .gitignore.

Follow the instructions provided by GitHub to add your remote repository and push your code:

css
Copy code
git remote add origin <your-github-repo-url>
git branch -M main
git push -u origin main

