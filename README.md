# 🔒 Safe Open Source - Kit de Publication Sécurisée

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Language](https://img.shields.io/badge/language-Français-blue.svg)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](pulls)

> Transformez vos projets privés en projets open source sans risque de leak de données sensibles.

Kit complet avec guide détaillé, checklist imprimable, script d'automatisation et template de README professionnel pour publier vos projets en toute sécurité.

---

## 🎯 Pourquoi ce Kit ?

Vous avez un projet privé que vous voulez partager en open source, mais :
- ❌ Vous avez des clés API dans le code
- ❌ Votre historique Git contient des secrets
- ❌ Des fichiers `.env` avec des mots de passe
- ❌ Vous ne savez pas par où commencer

**Ce kit vous guide pas à pas** pour nettoyer tout ça de manière sécurisée !

---

## 📦 Contenu du Kit

| Fichier | Description | Utilisation |
|---------|-------------|-------------|
| **[GUIDE-OPEN-SOURCE.md](GUIDE-OPEN-SOURCE.md)** | 📖 Guide complet étape par étape | Lis en premier |
| **[CHECKLIST-OPEN-SOURCE.md](CHECKLIST-OPEN-SOURCE.md)** | ✅ Checklist imprimable (150+ items) | Imprime et coche |
| **[prepare-open-source.sh](prepare-open-source.sh)** | 🤖 Script automatique de nettoyage | Exécute dans ton projet |
| **[README-TEMPLATE.md](README-TEMPLATE.md)** | 📝 Template de README professionnel | Copie et personnalise |

---

## 🚀 Quick Start

```bash
# 1. Clone ce repository
git clone https://github.com/gbourgogne4000K/safe-open-source.git
cd safe-open-source

# 2. Copie le kit dans ton projet
cp -r . /chemin/vers/ton-projet/oss-kit/

# 3. Va dans ton projet
cd /chemin/vers/ton-projet

# 4. Rends le script exécutable
chmod +x oss-kit/prepare-open-source.sh

# 5. Lance le script
./oss-kit/prepare-open-source.sh

# 6. Suis la checklist
# Ouvre oss-kit/CHECKLIST-OPEN-SOURCE.md et coche au fur et à mesure
```

---

## ✨ Fonctionnalités

### 🔍 Détection Automatique de Secrets
- Scan de 8+ patterns de secrets (API keys, passwords, tokens)
- Détection OpenAI, GitHub, AWS, Google Cloud
- Recherche dans le code ET l'historique Git

### 🛡️ Nettoyage Sécurisé
- Backup automatique avant toute opération
- Génération de `.env.example` avec placeholders
- Nettoyage de l'historique Git (3 méthodes)
- Configuration `.gitignore` complète

### 📚 Documentation Complète
- Guide de 16KB avec exemples de code
- Checklist de 150+ points de vérification
- Template README professionnel (500+ lignes)
- Section "En cas de leak" pour gestion de crise

### ⚡ Script d'Automatisation
- Scan de secrets
- Traitement des .env
- Création LICENSE MIT
- Vérifications pré-publication

---

## 📊 Cas d'Usage

### Petit Projet (< 50 fichiers)
```bash
./prepare-open-source.sh  # Réponds "No" au nettoyage d'historique
# Temps: ~15 minutes
```

### Projet Moyen (50-200 fichiers)
```bash
./prepare-open-source.sh  # Utilise la checklist complète
# Temps: ~30-45 minutes
```

### Gros Projet (200+ fichiers)
```bash
# 1. Lis le guide complet
# 2. Audit manuel + script
# 3. Scan avec GitGuardian
# Temps: 1-2 heures
```

---

## 🔒 Sécurité Garantie

Checklist minimale avant CHAQUE publication :

```
☐ Aucun fichier .env (sauf .env.example)
☐ .env.example avec seulement des placeholders
☐ Aucune clé API dans le code
☐ Aucun mot de passe en dur
☐ .gitignore complet
☐ Scan: grep -r "password|api_key|secret" .
☐ Test: clone dans nouveau dossier et teste
☐ Révoque TOUTES les anciennes clés après publication
```

---

## 📖 Documentation

### Guides
- **[Guide Complet](GUIDE-OPEN-SOURCE.md)** - Toutes les étapes détaillées
- **[Checklist](CHECKLIST-OPEN-SOURCE.md)** - Points de vérification

### Outils Recommandés
- [GitGuardian](https://www.gitguardian.com/) - Scan de secrets gratuit
- [BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/) - Nettoyage d'historique
- [Choose a License](https://choosealicense.com/) - Aide au choix de license

---

## 🆘 En Cas de Problème

### J'ai poussé un secret par erreur !

1. **STOP** - Ne panique pas
2. **RÉVOQUE** la clé immédiatement
3. **SUPPRIME** le repo GitHub
4. **NETTOIE** l'historique avec BFG
5. **VÉRIFIE** les logs d'utilisation
6. **REPUBLIE** avec historique propre

Voir [GUIDE-OPEN-SOURCE.md](GUIDE-OPEN-SOURCE.md#si-tu-as-déjà-pushé-un-secret) pour les détails.

---

## 🎓 Workflow Complet

```
┌─────────────────────────────────────────────┐
│ 1. Lis GUIDE-OPEN-SOURCE.md (sections 1-3) │
└──────────────────┬──────────────────────────┘
                   ↓
┌─────────────────────────────────────────────┐
│ 2. Imprime CHECKLIST-OPEN-SOURCE.md        │
└──────────────────┬──────────────────────────┘
                   ↓
┌─────────────────────────────────────────────┐
│ 3. Exécute prepare-open-source.sh          │
└──────────────────┬──────────────────────────┘
                   ↓
┌─────────────────────────────────────────────┐
│ 4. Vérification manuelle des résultats     │
└──────────────────┬──────────────────────────┘
                   ↓
┌─────────────────────────────────────────────┐
│ 5. Copie et personnalise README-TEMPLATE.md│
└──────────────────┬──────────────────────────┘
                   ↓
┌─────────────────────────────────────────────┐
│ 6. Test en local (clone dans nouveau dir)  │
└──────────────────┬──────────────────────────┘
                   ↓
┌─────────────────────────────────────────────┐
│ 7. Push vers GitHub                        │
└──────────────────┬──────────────────────────┘
                   ↓
┌─────────────────────────────────────────────┐
│ 8. RÉVOQUE toutes les anciennes clés API ! │
└─────────────────────────────────────────────┘
```

---

## 🤝 Contributing

Les contributions sont bienvenues ! Si tu as des idées pour améliorer le kit :

1. Fork le repository
2. Crée une branche (`git checkout -b feature/AmeliorationKit`)
3. Commit tes changements
4. Push et ouvre une Pull Request

### Idées de Contributions
- [ ] Support pour d'autres langages (Python, Go, Ruby, etc.)
- [ ] Patterns de secrets supplémentaires
- [ ] Templates README pour différents types de projets
- [ ] Traduction en anglais
- [ ] Scripts pour Windows PowerShell
- [ ] GitHub Actions pour vérification automatique

---

## 📝 License

MIT License - Réutilise librement pour tous tes projets !

Voir [LICENSE](LICENSE) pour plus de détails.

---

## 📊 Statistiques

- **16 KB** de documentation
- **150+** points de vérification
- **8+** patterns de secrets détectés
- **50+** commandes bash prêtes à l'emploi
- **3** méthodes de nettoyage Git
- **500+** lignes de template README

---

## 🌟 Star History

Si ce kit t'a aidé à publier ton projet en toute sécurité, donne-lui une étoile ! ⭐

---

## 💡 Tips Pro

### Réutilisation Rapide

Crée un alias pour accéder rapidement au kit :

```bash
# Dans ton .bashrc ou .zshrc
alias oss-prep='bash ~/safe-open-source/prepare-open-source.sh'

# Puis dans n'importe quel projet :
cd mon-projet
oss-prep
```

### Template de Projet

Garde ce kit dans un endroit accessible :

```bash
# Copie dans ton home
git clone https://github.com/gbourgogne4000K/safe-open-source.git ~/oss-toolkit

# Utilise pour chaque nouveau projet
cp -r ~/oss-toolkit/. /nouveau-projet/oss-kit/
```

---

## 📞 Support

- 📖 [Guide Complet](GUIDE-OPEN-SOURCE.md)
- ✅ [Checklist](CHECKLIST-OPEN-SOURCE.md)
- 🐛 [Report Issues](issues)
- 💬 [Discussions](discussions)

---

**Built with ❤️ pour la communauté open source française**

*Publier en open source devrait être simple et sûr. Ce kit rend ça possible.* 🚀
