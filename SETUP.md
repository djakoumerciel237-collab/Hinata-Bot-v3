# Configuration d'Hinata Bot V3

## ⚠️ Important - Sécurité

**Ne commitez JAMAIS vos identifiants sensibles sur le dépôt !**

Les fichiers de configuration suivants contiennent des données sensibles et doivent rester locaux :
- `config.dev.json`
- `config.*.json`
- `.env`
- `.env.local`

## Configuration Initiale

### 1. Créer votre fichier de configuration local

```bash
cp config.dev.example.json config.dev.json
```

### 2. Remplir vos identifiants

Ouvrez `config.dev.json` et remplacez les valeurs suivantes :

#### Compte Facebook
```json
"facebookAccount": {
  "email": "votre_email_facebook@gmail.com",
  "password": "votre_mot_de_passe_facebook"
}
```

#### Compte Gmail (pour les notifications)
```json
"gmailAccount": {
  "email": "votre_gmail@gmail.com",
  "clientId": "YOUR_CLIENT_ID",
  "clientSecret": "YOUR_CLIENT_SECRET",
  "refreshToken": "YOUR_REFRESH_TOKEN"
}
```

#### Google reCAPTCHA
```json
"gRecaptcha": {
  "siteKey": "YOUR_SITE_KEY",
  "secretKey": "YOUR_SECRET_KEY"
}
```

### 3. Autres paramètres importants

- `adminBot` : ID admin Facebook
- `timeZone` : Votre fuseau horaire
- `language` : Langue du bot (en, vi)
- `prefix` : Préfixe des commandes

## ✅ Vérification

Avant de lancer le bot :

```bash
# Vérifiez que config.dev.json n'est pas tracké
git status

# config.dev.json ne doit PAS apparaître
```

## 📚 Ressources

- [Documentation fb-chat-api](https://github.com/ntkhang03/fb-chat-api/blob/master/DOCS.md)
- [node-cron documentation](https://www.npmjs.com/package/node-cron)
- [Google OAuth Setup](https://developers.google.com/identity/protocols/oauth2)
