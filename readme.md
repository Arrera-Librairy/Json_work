# Explication de la classe `jsonWork`

La classe `jsonWork` est conçue pour faciliter la manipulation des fichiers JSON en Python. Elle fournit des méthodes pour lire, écrire et modifier des données dans un fichier JSON.

## Méthodes

### `__init__(self, file)`

*   **Description :** Initialise un nouvel objet `jsonWork`.
*   **Paramètres :**
    *   `file` : Le chemin d'accès au fichier JSON.

### `getJSONDict(self)`

*   **Description :** Retourne le contenu complet du fichier JSON sous forme de dictionnaire Python.
*   **Retourne :** Un dictionnaire représentant le contenu du JSON, ou `None` en cas d'erreur.

### `getContentJsonFlag(self, flag: str)`

*   **Description :** Lit la valeur associée à une clé (flag) spécifique dans le fichier JSON.
*   **Paramètres :**
    *   `flag` : La clé dont vous voulez récupérer la valeur.
*   **Retourne :** La valeur sous forme de chaîne de caractères, ou `None` en cas d'erreur.

### `getContentJsonMultiFlag(self, flag1, flag2)`

*   **Description :** Accède à une valeur dans un dictionnaire imbriqué.
*   **Paramètres :**
    *   `flag1` : La clé du dictionnaire principal.
    *   `flag2` : La clé du dictionnaire imbriqué.
*   **Retourne :** La valeur sous forme de chaîne de caractères, ou `None` en cas d'erreur.

### `getFlagListJson(self, flag)`

*   **Description :** Récupère une liste à partir du fichier JSON.
*   **Paramètres :**
    *   `flag` : La clé qui contient la liste.
*   **Retourne :** La liste, ou `None` en cas d'erreur.

### `getFlagDictJson(self, flag)`

*   **Description :** Récupère un dictionnaire à partir du fichier JSON.
*   **Paramètres :**
    *   `flag` : La clé qui contient le dictionnaire.
*   **Retourne :** Le dictionnaire, ou `None` en cas d'erreur.

### `setValeurJson(self, flag, valeur)`

*   **Description :** Écrit ou met à jour la valeur d'une clé dans le fichier JSON.
*   **Paramètres :**
    *   `flag` : La clé à modifier.
    *   `valeur` : La nouvelle valeur à assigner.
*   **Retourne :** `True` si l'opération a réussi, `False` sinon.

### `setListJson(self, flag, valeur: list)`

*   **Description :** Ajoute un élément à une liste existante dans le fichier JSON.
*   **Paramètres :**
    *   `flag` : La clé de la liste.
    *   `valeur` : L'élément à ajouter à la liste.
*   **Retourne :** `True` si l'opération a réussi, `False` sinon.

### `setDictJson(self, flag, cle, valeur)`

*   **Description :** Ajoute ou met à jour une paire clé-valeur dans un dictionnaire existant dans le fichier JSON.
*   **Paramètres :**
    *   `flag` : La clé du dictionnaire à modifier.
    *   `cle` : La clé à ajouter/mettre à jour dans le dictionnaire.
    *   `valeur` : La valeur associée à la clé.
*   **Retourne :** `True` si l'opération a réussi, `False` sinon.

### `unsetDictJson(self, flag, cle)`

*   **Description :** Supprime une clé d'un dictionnaire dans le fichier JSON.
*   **Paramètres :**
    *   `flag` : La clé du dictionnaire à modifier.
    *   `cle` : La clé à supprimer du dictionnaire.
*   **Retourne :** `True` si l'opération a réussi, `False` sinon.

### `unsetValeurJson(self, flag: str)`

*   **Description :** Efface la valeur d'une clé (la met à une chaîne vide).
*   **Paramètres :**
    *   `flag` : La clé dont la valeur doit être effacée.
*   **Retourne :** `True` si l'opération a réussi, `False` sinon.

### `unsetListJson(self, flag, valeur)`

*   **Description :** Supprime une valeur d'une liste dans le fichier JSON.
*   **Paramètres :**
    *   `flag` : La clé de la liste.
    *   `valeur` : La valeur à supprimer de la liste.
*   **Retourne :** `True` si l'opération a réussi, `False` sinon.

### `unsetDictReorg(self, flag)`

*   **Description :** Supprime une clé du dictionnaire racine et réorganise les clés restantes (suppose des clés numériques).
*   **Paramètres :**
    *   `flag` : La clé à supprimer.
*   **Retourne :** `True` si l'opération a réussi, `False` sinon.

### `unsetDictByFlag(self, flag, name)`

*   **Description :** Supprime un dictionnaire entier de la racine basé sur la valeur d'une de ses clés.
*   **Paramètres :**
    *   `flag` : La clé à rechercher dans les dictionnaires imbriqués.
    *   `name` : La valeur qui, si elle correspond, déclenchera la suppression du dictionnaire parent.
*   **Retourne :** `True` si l'opération a réussi, `False` sinon.

### `setDictOnJson(self, dict: dict)`

*   **Description :** Écrase le contenu entier du fichier JSON avec un nouveau dictionnaire.
*   **Paramètres :**
    *   `dict` : Le dictionnaire à écrire dans le fichier.
*   **Retourne :** `True` si l'opération a réussi, `False` sinon.