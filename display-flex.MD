Display Flex (CSS)
display: flex
display: flex transforme un conteneur en conteneur flexible. Les

éléments enfants s'alignent facilement sur une ligne ou une colonne.
.container {
display: flex;
}

justify-content
Contrôle l'alignement des éléments sur l'axe principal (horizontal

par défaut).
Valeur Effet

flex-start Début du conteneur

center Centre

flex-end Fin du conteneur

space-between Espaces égaux entre les éléments

space-around Espace autour de chaque élément

space-evenly Espaces parfaitement égaux
.container {
display: flex;
justify-content: center;
}

align-items
Contrôle l'alignement des éléments sur l'axe secondaire (vertical

par défaut).
Valeur Effet

stretch Étire les éléments (par défaut)

flex-start En haut

center Au centre

flex-end En bas

baseline Aligne selon la ligne de base du texte
.container {
display: flex;
align-items: center;
}

Exemple complet
.container {
display: flex;
justify-content: center;
align-items: center;
height: 100vh;
}

Résultat : les éléments sont parfaitement centrés horizontalement et

verticalement.
Astuce
· justify-content → axe principal (horizontal par défaut).
· align-items → axe secondaire (vertical par défaut).
Mémo : - Gauche ↔ Droite → justify-content - Haut ↕ Bas →

align-items
