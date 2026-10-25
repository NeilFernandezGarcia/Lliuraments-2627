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
