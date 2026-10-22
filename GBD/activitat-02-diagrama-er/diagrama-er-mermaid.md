# Diagrama sencer
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
