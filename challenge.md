# Cinquième challenge Github



- En travaillant par groupe (ou en solo)
- Créez un nouveau dépôt
- Créez un code Go qui permet d'afficher un message via une vache, vous pouvez utiliser le code ci dessous :

```
package main
import (
    "fmt"
    "log"
    cowsay "github.com/Code-Hex/Neo-cowsay/v2"
)
func main() {
    // Message à afficher avec la vache
    message := "Hello, Go World!"
    // Génère le message cowsay
    cow, err := cowsay.Say(
        message    , // Le texte que la vache dira
        cowsay.Type("default"), // Le type de vache (peut être changé, par ex. "dragon")
    )
    if err != nil {
        log.Fatalf("Erreur lors de la génération de la vache : %v", err)
    }
    // Affiche la vache
    fmt.Println(cow)
}
```

- <mark>Ecrire un workflow Github action</mark> qui contient deux étapes :
  
  - build -> compile le programme Go en un exécutable
  - deploy -> déploie votre code Go sur un serveur

- <mark>Préparer une image Docker</mark> qui va afficher une vache en utilisant le programme précédent
  
  - Préparer un Dockerfile avec l'exécutable dedans
  - Publiez l'image sur le Dockerhub via une workflow Github action

- <mark>Mettre en place un système de mise à jour automatique</mark> pour avoir une nouvelle image générée chaque nuit.

