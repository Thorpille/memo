# Les listes

### Ajout suppression d'éléments :
    ma_liste = [1, 2, 3]           Déclaration + affectation
    ma_liste.append(ma_var_a_ajouter)         ajout d'une seule valeur
    ma_liste.extend([1, 2, 3])           ajout plusieurs valeurs sous forme d'une liste
    ma_liste.remove(ma_var_a_sup)                    Enlève la première occurrence de l'élément indiqué
    ma_liste.pop(-1)    Enlève le dernier élément, renvoie le contenu de l'élément enlevé
    ma_liste.clear()     Vide la liste
    
### Info sur la liste :
    len(ma_liste)                            Renvoie le nombre d'éléments
    ma_liste.index("truc")   Renvoie l'index de truc
    ma_liste.count("truc")  Renvoie le nombre d’occurrence de truc
    
### Réorganistion de la liste :
    ma_liste.sort()          Range les élément par ordre alphabétique, écrase l'ancienne liste
    sorted(ma_liste)        Renvoie la liste triée par ordre alphabétique
    ma_liste.reverse() inverse l'ordre de la liste et écrase l'ancienne
    "-".join(ma_liste)      Joint les élément de la liste avec - comme séparateur
    courses.split(",")   Découpe la chaine de caractère à chaque , (par défaut coupe aux espaces)
    
### Accès aux valeurs
    ma_liste[0]       Accède au premier élément de ma_liste
    ma_liste[-1]     Accède au dernier élément de ma_liste

### Conversions
    list(mon_tuple)    tuple => liste
    tuple(ma_liste)     liste => tuple
    
### Les slices :
    ma_liste[0:2]    Renvoie les deux première valeur de la liste (le deuxième index est exclu)
    ma_liste[3:]      Renvoie les valeurs de la de la quatrième à la dernière
    ma_liste[::2]      Renvoie les éléments par pas de deux (index 0, 2, 4...)
    ma_liste[::-1]    Affiche tout les éléments en commençant par la fin

### Les compréhensions de liste
    liste = [-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5]
    nombre_positifs = [i for i in liste if i > 0]
    nombre_positifs_fois_deux = [i * 2 for i in liste if i > 0]
