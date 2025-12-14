# Compte Rendu - Lab 2 - MLOps

Soufiane MAJDALANE

# **Code Source management**

### **Étape 1 : Initialiser Git dans mlops-lab-01 dans Git bash**

![image.png](image.png)

![image.png](image%201.png)

Creation du fichier `.gitignore`

![image.png](image%202.png)

Vérification de l’état du dépôt :

![image.png](image%203.png)

### **Étape 2 : Premier commit du projet MLOps**

Ajout des dossiers et fichiers principaux

![image.png](image%204.png)

Création du premier commit :

![image.png](image%205.png)

Afficher l’historique :

![image.png](image%206.png)

### **Étape 3 : Observer une modification avec git diff**

**Modification un script existant dans `src/monitor_drift.py`**
`z_threshold (2.5 -> 2.0)`

Affichage les différences par rapport au dernier commit :

![image.png](image%207.png)

Ajout du fichier modifié à l’index et afficher les différences en staging:

![image.png](image%208.png)

Création d’un commit :

![image.png](image%209.png)

### **Étape 4 : Créer une branche de fonctionnalité liée au lab**

Création d’une branche :

![image.png](image%2010.png)

Modification de `src/api.py` :

- ajout d’une gestion de `request_id` automatique

Ajout et commiting :

![image.png](image%2011.png)

Lister les branches :

![image.png](image%2012.png)

Revenir sur la branche principale :

![image.png](image%2013.png)

### **Étape 5 : Fusionner la branche feature dans la branche principale**

Fusion des branches et verification d’historique

![image.png](image%2014.png)

### **Étape 6 : Créer un conflit de merge sur src/train.py**

Création d’une nouvelle branche :

![image.png](image%2015.png)

Modification du `src/train.py` 

- `gate_f1` à 0.50

Ajout et commiting:

![image.png](image%2016.png)

Revenir sur la branche principale et modifier la même ligne dans `src/train.py`:

- `gate_f1` à 0.75

Ajout et commiting :

![image.png](image%2017.png)

Fusion echouee:

![image.png](image%2018.png)

On va résoudre le conflit dans `src/train.py` 

- choisir la valeur 0.70

Résoudre le conflit dans `src/train.py` → 0.70:

![image.png](image%2019.png)

### **Étape 7 : Utiliser git stash dans le contexte du lab**

Modifier un fichier sans vouloir committer

- `ouvrir src/rollback.py et ajouter un commentaire TODO`

Affichage d’etat:

![image.png](image%2020.png)

Mettre de côté les modifications et Lister les stash :

![image.png](image%2021.png)

Récupérer les modifications :

![image.png](image%2022.png)

### **Étape 8 : Tester git reset sur un fichier d’expérimentation**

Création un dossier d’expérimentation :

![image.png](image%2023.png)

Créer un fichier de test :

![image.png](image%2024.png)

Modification puis committing deux fois :

![image.png](image%2025.png)

Effectuer un reset soft :

![image.png](image%2026.png)

Effectuer un reset mixed :

![image.png](image%2027.png)

Effectuer un reset hard :

![image.png](image%2028.png)

### **Étape 9 : Annuler un commit avec git revert**

Ajouter un changement non souhaité dans `src/api.py` :

![image.png](image%2029.png)

Liste des commits :

![image.png](image%2030.png)

Revert du dernier commit :

![image.png](image%2031.png)

Vérifier le contenu du fichier :

![image.png](image%2032.png)

### **Étape 10 : Rebase d’une branche feature sur la branche principale**

Créer une branche :

![image.png](image%2033.png)

Modifier `src/monitor_drift.py` 

- changer `last_n`→ exemple 500 :

Ajouter et committer :

![image.png](image%2034.png)

Revenir sur la branche principale et créer un nouveau commit sur un autre fichier (par exemple `src/generate_data.py`) :

![image.png](image%2035.png)

Revenir sur la branche feature :

![image.png](image%2036.png)

Rebaser la branche feature sur la branche principale :

![image.png](image%2037.png)

Vérifier l’historique :

![image.png](image%2038.png)