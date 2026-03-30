# ⚙️ GEEKTEC - Page de Maintenance Interactive

Une page de maintenance haut de gamme, moderne et interactive, conçue pour divertir vos utilisateurs pendant les interruptions de service.

![Maintenance Page Preview](https://via.placeholder.com/800x450/000000/FFFFFF?text=Maintenance+Page+Preview)

## 🚀 Caractéristiques

- **Esthétique Monochrome Premium** : Un design "Tech-Noir" minimaliste en Noir & Blanc.
- **Système de Thème Interactif** :
  - **Mode Sombre (OLED)** : Arrière-plan noir pur pour un contraste maximal.
  - **Mode Simple (Clair)** : Une version lumineuse et épurée.
  - Sauvegarde automatique de la préférence via `localStorage`.
- **Animation d'Arrière-plan Technologique** : Un système de "Neural Network / Flux de données" dynamique et fluide.
- **Mini-Jeux Intégrés** : Quatre jeux classiques pour occuper vos visiteurs :
  - 🧩 **Tetris**
  - 💣 **Démineur**
  - 🃏 **Memory**
  - 🎮 **Space Invaders**
- **100% Autonome** : Un seul fichier HTML contenant tout le CSS et le JavaScript. Aucun framework externe requis.

## 🛠️ Comment l'implémenter ?

L'implémentation est extrêmement simple car tout est regroupé dans un seul fichier.

### Option 1 : Utilisation directe
1. Téléchargez le fichier `index.html`.
2. Renommez-le en `maintenance.html` (ou gardez `index.html` si c'est votre page racine).
3. Placez-le à la racine de votre serveur web.

### Option 2 : Intégration via redirection (Nginx/Apache)
Configurez votre serveur pour rediriger tout le trafic vers cette page pendant la maintenance.

**Exemple Nginx :**
```nginx
error_page 503 /maintenance.html;
location / {
    if (-f $document_root/maintenance.html) {
        return 503;
    }
}
```

## 🎨 Personnalisation

Vous pouvez facilement changer l'apparence en modifiant les variables CSS au début du fichier dans la balise `<style>` :

```css
:root {
  --primary: #ffffff;    /* Couleur d'accentuation (Défaut: Blanc) */
  --bg: #000000;         /* Couleur d'arrière-plan (Défaut: Noir) */
  --transition: all .3s; /* Vitesse des transitions */
}
```

## 📜 Licence

Ce projet est libre d'utilisation pour vos projets personnels et commerciaux.
