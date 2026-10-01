# Upsell du Pass après Reboost · montage dans Scalz

Deux pages identiques, seuls changent le nom du Pass, la description et le témoignage :
- tunnel **Reboost Hormonal** → page `Upsell Hormonal/` (avant/après et témoignage de Julie)
- tunnel **Reboost Ménopause** → page `Upsell Ménopause/` (témoignages de Mélodie et Rosie)

## 1. L'étape dans le tunnel Reboost

1. Dans le tunnel Reboost, ajoute une étape de type **Upsell** juste après le bon de commande à 39 €, avant les consultations.
2. Dans l'onglet **Produits** de cette étape, ajoute le produit **Pass Bien-Être Hormonal** (ou Ménopause) avec un prix **49 €/mois récurrent**.
   - Le code PASS49 ne peut pas être saisi sur un achat en un clic. Le prix de l'upsell doit donc être 49 € directement.
   - Ajoute ce prix à 49 € **sur le produit existant**. Ne crée pas de nouveau produit, sinon le workflow « 1 Achat » (accès au groupe et aux cours) risque de ne pas se déclencher.

## 2. L'ordre des éléments sur la page

| # | Élément Scalz | Contenu |
|---|---|---|
| 1 | Code personnalisé | `1 haut et vidéo.html` |
| 2 | **BOUTON 1** | (natif Scalz, voir plus bas) |
| 3 | Code personnalisé | `2 offre.html` (pourquoi maintenant, un mois dans le Pass, le prix) |
| 4 | **BOUTON 2** | identique au bouton 1 |
| 5 | Code personnalisé | `3 témoignages et questions.html` (témoignages, Laurette, et après, questions) |
| 6 | **BOUTON 3** | identique au bouton 1 |
| 7 | Lien texte ou petit bouton | « Non merci, je continue sans le Pass » → action **Aller à l'étape suivante** |
| 8 | Code personnalisé | `4 pied de page.html` |

Les boutons doivent être des **boutons natifs Scalz** : un bouton dans un bloc de code ne peut pas déclencher l'achat en un clic.

## 3. Réglages des 3 boutons (les mêmes partout)

- **Action** : achat de l'upsell en un clic (« One Click Upsell » / « Acheter l'upsell » selon la langue de Scalz), sur le produit Pass de l'étape.
- **Texte** : Oui, j'ajoute le Pass · 49 €/mois
- **Sous-texte** : En 1 clic, sans ressaisir ta carte
- **Fond** : #C9785B · survol #B4664A · **texte** : #FFFFFF
- **Police** : Outfit, 500, 19 px (sous-texte 14 px)
- **Coins** : arrondis au maximum (forme pilule) · largeur pleine sur mobile, 520 px max sur ordinateur

Astuce : règle le premier bouton, puis duplique-le deux fois.

## 4. La vidéo

Dans `1 haut et vidéo.html`, remplace le bloc entre `<!-- VIDEO -->` et `<!-- FIN VIDEO -->` par le code Wistia de la VSL du Pass (le même que sur la page de vente). Ou envoie-moi le code et je le mets.

## 5. À tester avant de mettre en ligne

1. Un achat test Reboost **par carte** → clic sur le bouton de l'upsell : le Pass doit être acheté sans ressaisir la carte.
2. **Le workflow « 1 Achat » se déclenche-t-il sur l'achat de l'upsell ?** (email de bienvenue, accès au groupe et aux cours). Si non, ajoute un déclencheur « Paiement reçu » filtré sur le produit Pass.
3. Un achat test **par PayPal** : vérifie que l'upsell passe aussi. Si PayPal demande de repayer, la phrase « sans ressaisir ta carte » doit être adaptée.
4. Le lien « Non merci » mène bien à l'étape suivante (consultations ou page merci).
5. Tout se lit bien sur téléphone.

## À valider avec Laurette

- **49 € pour les clientes Reboost, sans date de fin.** La page dit « Prix réservé aux clientes Reboost ». Après le 31 octobre, le Pass passe à 69 € pour les autres, mais l'upsell reste à 49 €. Si elle préfère 69 € après octobre, il faudra changer le prix et le texte.
- Le chiffre **+1 560 femmes accompagnées** est celui de la page du Pass. La page Reboost dit 3 450.
