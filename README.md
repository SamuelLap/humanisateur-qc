# Humanisateur Qc

Skill pour Claude qui retire les tics d'écriture typiques de l'IA d'un texte et le réécrit en français québécois naturel.

C'est une adaptation québécoise de [blader/humanizer](https://github.com/blader/humanizer), pensée pour le français : vocabulaire d'IA en français, calques de l'anglais, typographie de l'OQLF, féminisation, tutoiement/vouvoiement.

## Installation

### Claude.ai (web, mobile) et Claude Desktop

1. Télécharge [`humanisateur-qc.zip`](https://github.com/SamuelLap/humanisateur-qc/raw/main/humanisateur-qc.zip) (ou compresse le dossier `humanisateur-qc/`, avec `SKILL.md` à l'intérieur).
2. Ouvre Personnaliser → Skills (ou Paramètres → Capacités → Skills).
3. Clique sur « Téléverser un skill » et choisis le .zip.

### Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/SamuelLap/humanisateur-qc.git ~/.claude/skills/humanisateur-qc
```

## Utilisation

```
/humanisateur-qc

[colle ton texte ici]
```

Ou demande simplement : « Humanise ce texte en français québécois : … »

Pour calquer ton style, ajoute un échantillon de ton écriture (2 ou 3 paragraphes).

Pour seulement détecter les tics sans réécrire : « Est-ce que ce texte sonne IA? »

## Ce qu'il fait

- repère 26 marques d'écriture générée (importance gonflée, vocabulaire d'IA, parallélismes, tirets en rafale, gras et listes partout, formules de chatbot, conclusions génériques, etc.);
- garde le français standard du Québec, pas de joual sauf demande;
- applique la typographie de l'OQLF (guillemets, espaces, heures, argent, majuscules des titres);
- n'invente aucun fait : il laisse un [repère] quand un détail manque;
- fait un audit final puis une deuxième version.

## Licence et attributions

Licence MIT (voir `LICENSE`).

- Structure et idées générales : [blader/humanizer](https://github.com/blader/humanizer) (MIT)
- Catalogue de marques : Wikipédia, « Signs of AI writing », WikiProject AI Cleanup (CC BY-SA 4.0)
- Normes linguistiques : Office québécois de la langue française
