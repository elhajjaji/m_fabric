# m_fabric
## Jeu de données:

+-----------------+       1        N       +---------------------+
|    Individu     |<--------------------->|      Prestation      |
+-----------------+                       +---------------------+
| - id            |                       | - date_debut_prest   |
| - nom           |                       | - date_prestation    |
| - prenom        |                       | - type_prestation    |
| - email         |                       | - montant_prestation |
| - sexe          |                       | - numero_individu    |
| - date_naissance|                       | - date_fin_prest     |
| - date_deces    |                       +---------------------+
| - navs          |
| - numero_individu|
+-----------------+


```mermaid
classDiagram
    direction LR
    Individu "1" --> "N" Prestation : has

    class Individu {
        id: int
        nom: string
        prenom: string
        email: string
        sexe: string
        date_naissance: date
        date_deces: date
        navs: string
        numero_individu: string
    }

    class Prestation {
        date_debut_prestation: date
        date_prestation: date
        type_prestation: string
        montant_prestation: float
        numero_individu: string
        date_fin_prest: date
    }

