# Diagrama Mermaid
## Diagrama Personatje
``` mermaid
erDiagram
    PERSONATJE {
        string DNI PK
        string Nom "Not Null"
        string Cognom
        int Vida
        int Força
        int Carisma
        int Agilitat
    }
```
El DNI és obligatori perquè és la clau primària i serveix per identificar de manera única cada personatge. El nom no pot ser nul perquè és una dada necessària per saber com s'anomena el personatge.
Així s'evita que hi hagi personatges sense identificació o sense nom.
## Diagrama Mascota
``` mermaid
erDiagram
    MASCOTA {
        string NumChip PK
        string Nom "Not null"
        int Motxilla
    }
```
El número de xip és la clau primària perquè permet identificar de manera única cada mascota i és obligatori.
El nom té la restricció "Not Null" perquè és una dada necessària i no pot quedar buida.
L'atribut Motxilla indica la motxilla de la mascota i s'emmagatzema com un nombre enter.
## Diagrama Habilitat
``` mermaid
erDiagram
    HABILITAT {
        int Codi PK
        string Nom "Not null"
        int Cost
        int Dany
        int Cooldown
        string Tipus "Not null"
}
```
El codi és la clau primària perquè permet identificar de manera única cada habilitat.
El nom i el tipus tenen la restricció "Not Null" perquè són dades obligatòries i no poden quedar buides.
La resta d'atributs indiquen el cost, el dany i el temps de reutilització de cada habilitat.
## Diagrama Item
``` mermaid
erDiagram
    ITEM {
        int Codi PK
        string Nom "Not null"
        string Equipable
        string Tipus "Not null"
        string Comerciable "Not null"
        int Pes "Not null"
        string Qualitat "Not null"
        int Mesura-X "Not null"
        int Mesura-Y "Not null"
        int Mesura-Z "Not null"
    }
```
El codi és la clau primària perquè permet identificar de manera única cada ítem.
El nom, el tipus, si és comerciable, el pes, la qualitat i les mesures són obligatoris perquè no poden quedar buits.
La resta d'atributs indiquen si l'ítem es pot equipar i les seves característiques físiques.
## Diagrama Enemic
``` mermaid
erDiagram
    ENEMIC {
        int Codi PK
        string Nom "Not null"
        string Tipus "Not null"
        int Nivell "Not null"
        int Vida
        int Força
        int Agilitat
        int Carisma
    }
```
El codi és la clau primària perquè permet identificar de manera única cada enemic.
El nom, el tipus i el nivell són obligatoris perquè no poden quedar buits.
La resta d'atributs indiquen les característiques de cada enemic, com la vida, la força, l'agilitat i el carisma.
## Diagrama sencer
``` mermaid
erDiagram
PERSONATJE || -- || MASCOTA : acompaña
PERSONATJE }o--o{ HABILITAT : Posseix
HABILITAT }o--o{ HABILITAT : Combina 
PERSONATJE }o--o{ ITEM : Equipa
PERSONATJE }o--o{ ENEMIC : Enfrenta
ENEMIC }o--o{ HABILITAT : Enfrenta
MASCOTA ||--|{ ITEM : Carrega
    PERSONATJE {
        string DNI PK
        string Nom "Not Null"
        string Cognom
        int Vida
        int Força
        int Carisma
        int Agilitat
    }
    MASCOTA {
        string NumChip PK
        string Nom "Not null"
        int Motxilla
    }
    HABILITAT {
        int Codi PK
        string Nom "Not null"
        int Cost
        int Dany
        int Cooldown
        string Tipus "Not null"
    }
    ITEM {
        int Codi PK
        string Nom "Not null"
        string Equipable
        string Tipus "Not null"
        string Comerciable "Not null"
        int Pes "Not null"
        string Qualitat "Not null"
        int Mesura-X "Not null"
        int Mesura-Y "Not null"
        int Mesura-Z "Not null"
    }
    ENEMIC {
        int Codi PK
        string Nom "Not null"
        string Tipus "Not null"
        int Nivell "Not null"
        int Vida
        int Força
        int Agilitat
        int Carisma
    }
```
