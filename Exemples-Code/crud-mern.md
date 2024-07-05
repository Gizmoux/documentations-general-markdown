# Guide de Développement Backend avec Node.js et Express

## Table des matières

1. [Initialisation du projet](#initialisation-du-projet)
2. [Création du serveur Node](#création-du-serveur-node)
3. [Configuration d'Express](#configuration-dexpress)
4. [Connexion à la base de données](#connexion-à-la-base-de-données)
5. [Définition du modèle](#définition-du-modèle)
6. [Opérations CRUD](#opérations-crud)
7. [Démarrage du serveur](#démarrage-du-serveur)

## Initialisation du projet

### Commandes de base

```bash
# Initialiser un dépôt Git
git init

# Créer un fichier .gitignore
echo "node_modules" > .gitignore

# Initialiser le projet npm
npm init -y

# Installer les dépendances
npm install express cors mongoose nodemon
```

Création du serveur Node
Node.js utilise le système de modules CommonJS
require est utilisé pour importer des modules au lieu de import
Nodemon est utilisé pour redémarrer automatiquement le serveur lors des modifications

```bash
# Configuration d'Express

const express = require("express");
const cors = require("cors");

const app = express();
app.use(express.json());
app.use(cors());

# Connexion à la base de données
const mongoose = require("mongoose");
mongoose.connect("mongodb://localhost/students-app");

# Définition du modèle
const Student = mongoose.model("Student", {
  name: {
    type: String,
    default: "",
  },
  age: {
    type: Number,
  },
});

Opérations CRUD

- **Create**

app.post("/create", async (req, res) => {
  try {
    const newStudent = new Student({
      name: req.fields.name,
      age: req.fields.age,
    });
    await newStudent.save();
    res.json({ message: "Student created" });
  } catch (error) {
    res.status(400).json({ error: error.message });
  }
});

- **Read**

app.get("/", async (req, res) => {
  try {
    const students = await Student.find();
    res.json(students);
  } catch (error) {
    res.status(400).json({ error: error.message });
  }
});

- **Update**

app.post("/update", async (req, res) => {
  try {
    if (req.fields.id && req.fields.age) {
      const student = await Student.findOne({ _id: req.fields.id });
      student.age = req.fields.age;
      await student.save();
      res.json(student);
    } else {
      res.status(400).json({ message: "Missing parameter" });
    }
  } catch (error) {
    res.status(400).json({ error: error.message });
  }
});

- **Delete**

app.post("/delete", async (req, res) => {
  try {
    if (req.fields.id) {
      await Student.findByIdAndDelete(req.fields.id);
      res.json({ message: "Student removed" });
    } else {
      res.status(400).json({ message: "Missing id" });
    }
  } catch (error) {
    res.status(400).json({ error: error.message });
  }
});

# Démarrage du serveur

app.listen(3000, () => {
  console.log("Server started on port 3000");
});

# Configuration du script de démarrage
- **Dans package.json, ajoutez :**
json
"scripts": {
  "start": "nodemon server.js"
}

Pour démarrer le serveur :
bash
npm start
```

Cette structure est plus claire et plus facile à suivre pour un fichier Markdown. Elle inclut une table des matières, des sections bien définies, et des blocs de code correctement formatés.
