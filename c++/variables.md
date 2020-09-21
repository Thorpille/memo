# Les variables

## Les types de variables

* **int      petit nombre entier**
* long_int ou long    grand nombre entier
* long long
* short
* unsigned int...

* **double   nombre à virgule**
* float
* long double

* **char** chaine de caractères
* wchar_t chaine de caractères encodé en UTF-8
* char16_t
* char32_t

* **bool**

* **auto**

### Déclaration :
int var1{12}, var2{23};

### Pour convertir d'un type à un autre :

    static_cast<int>(nombreAVirgule)

## Variables spéciales

### Les références

    int& maReference{maVariable} 
maReference est égale à maVariable (Meme emplacement mémoire)

### Les pointeurs

&maVariable renvoie l"adresse mémoire dans laquelle est stockée maVariable

    int *monPointeur{&maVariable}
monPointeur contient l'adresse mémoire de maVariable

\*monpointeur renvoie la valeur de maVariable
