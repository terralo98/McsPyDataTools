# 🧠 McsPyDataTools - Analyse de Signaux Neuronaux MEA2100

📌 **McsPyDataTools** est une boîte à outils Python conçue pour analyser les fichiers **HDF5** générés par les systèmes d’enregistrement **Multi Channel Systems (MCS)**.
Elle permet d’exploiter efficacement les signaux neuronaux enregistrés via **MEA2100** et d’extraire des informations essentielles pour l’analyse des réseaux de neurones in vitro.

---

## 👤 Auteurs
**Auteur principal :** [Votre Nom]
**GitHub :** [Votre Profil GitHub](https://github.com/votre-utilisateur)

---

## 📂 Structure du Dépôt
```
McsPyDataTools/
🗋 McsPyDataTools/         # Package principal contenant les fonctions Python
   📚 __init__.py         # Initialise le package
   📚 data_processing.py  # Fonctions de traitement des données
   📚 visualization.py    # Fonctions pour tracer les signaux
   📚 io_utils.py         # Fonctions de lecture et d'écriture des fichiers HDF5
🗋 docs/                   # Documentation et tutoriels
   📚 McsPy-Tutorial_Toolbox.ipynb  # Tutoriel interactif (Jupyter Notebook)
   📚 mcs_hdf5_protocol.rst        # Description du format HDF5
   📚 api.rst                     # Documentation de l’API
🗋 tests/                  # Scripts de test pour valider les fonctionnalités
   📚 test_data_processing.py
🗋 McsPyDataNotebooks/     # Notebooks Jupyter avec des analyses détaillées
📚 requirements.txt        # Liste des dépendances Python
📚 .gitignore              # Fichiers à ignorer par Git
📚 README.md               # Documentation principale (ce fichier)
```

---

## 🔧 Fonctionnalités Principales
✅ **Lecture des fichiers HDF5** exportés par MCS.  
✅ **Extraction des signaux ADC** et récupération des données brutes.  
✅ **Traitement des signaux neuronaux** (filtrage, normalisation).  
✅ **Visualisation des signaux et des pics**.  
✅ **Optimisation et conversion des données** pour l’analyse statistique.  

---

## 🚀 Installation

### 1️⃣ **Cloner le dépôt sur votre machine**
```bash
git clone https://github.com/votre-utilisateur/McsPyDataTools.git
cd McsPyDataTools
```

### 2️⃣ **Installer les dépendances**
Avant d’exécuter les scripts, assurez-vous d’installer les bibliothèques nécessaires :
```bash
pip install -r requirements.txt
```

---

## 🛠️ Utilisation des Scripts

### 📌 **1. Lecture d’un fichier HDF5**
Utilisez **`io_utils.py`** pour ouvrir un fichier d'enregistrement :
```python
from McsPyDataTools.io_utils import load_hdf5_file

file_path = "data/neuronal_recording.h5"
data = load_hdf5_file(file_path)
print(data.keys())  # Affiche les canaux disponibles
```

### 📌 **2. Traitement des signaux**
Exemple d'application d'un **filtre passe-haut** :
```python
from McsPyDataTools.data_processing import highpass_filter

filtered_signal = highpass_filter(data['channel_1'], cutoff=300, fs=10000)
```

### 📌 **3. Visualisation des Signaux**
Tracer un signal brut et filtré :
```python
from McsPyDataTools.visualization import plot_signal

plot_signal(data['channel_1'], title="Signal brut")
plot_signal(filtered_signal, title="Signal filtré")
```

---

## 📚 Tutoriels et Documentation
- 📘 **[Tutoriel McsPyDataTools (Jupyter Notebook)](McsPyDataTools/docs/McsPy-Tutorial_Toolbox.ipynb)**
- 📂 **[Définitions du format MCS HDF5](McsPyDataTools/docs/mcs_hdf5_protocol.rst)**
- 📄 **[Documentation de l’API](McsPyDataTools/docs/api.rst)**

---

## 👥 Contribution

🚀 **Vous voulez améliorer le projet ?** Voici comment contribuer :
1. **Forker le dépôt** et cloner votre propre version.
2. **Créer une nouvelle branche** :
   ```bash
   git checkout -b feature-nouvelle-fonction
   ```
3. **Faire vos modifications** et commit :
   ```bash
   git commit -am "Ajout d'une fonction de détection de pics"
   ```
4. **Pousser vos modifications** et ouvrir une **Pull Request**.

Merci pour votre aide précieuse ! 🙌

---

## 🛠️ Dépendances Utilisées
- **NumPy** → Calculs et manipulation des tableaux de signaux
- **Pandas** → Gestion des données sous format tableur
- **h5py** → Lecture des fichiers HDF5
- **Matplotlib / Seaborn** → Visualisation des signaux
- **SciPy** → Traitement du signal (filtres, transformations)

Installez toutes les dépendances avec :
```bash
pip install numpy pandas h5py matplotlib seaborn scipy
```

---

## 👤 Contact & Support

💎 **Auteur :** [Votre Nom]  
🌐 **GitHub :** [Votre Profil GitHub](https://github.com/votre-utilisateur)  
💬 **Support :** Ouvrez une issue [ici](https://github.com/votre-utilisateur/McsPyDataTools/issues)  

Si ce projet vous aide, **n’hésitez pas à lui donner une ⭐ sur GitHub** ! 🚀

