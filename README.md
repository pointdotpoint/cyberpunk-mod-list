# Cyberpunk 2077 Ultimate Mod List

A highly curated, deduplicated, and deeply immersive mod list for Cyberpunk 2077, presented in a sleek, hacker-style "Netrunner Terminal" web interface. 

This project is built using the [Hugo](https://gohugo.io/) static site generator and is completely configured for immediate deployment to Netlify.

---

## 🛠️ How to Edit Content

The website is data-driven, meaning you don't have to touch complex HTML to update the mods!

### 1. Editing Mods and Links
All of the mod cards, URLs, titles, and categories are generated automatically from a single database file.
To add new mods, edit broken links, or change descriptions, open this file:
`data/mods.json`

Inside, you will find a list of mods. To add a new mod, copy an existing block and add it to the list, ensuring you follow standard JSON formatting:

```json
  {
    "category": "Immersion Mods",
    "title": "Immersive First Person",
    "description": "Lets you see your body when looking down",
    "url": "https://www.nexusmods.com/cyberpunk2077/mods/2675",
    "source": "Tipsy's Immersive Modlist",
    "final_category": "Gameplay Mechanics"
  }
```

### 2. Editing the FAQ & Intro Text
If you want to edit the large block of text at the top of the website (the FAQ, Modtool guides, and compatibility warnings), open this file:
`themes/cyberpunk/layouts/partials/intro.html`

You can safely write normal text and basic HTML inside that file to update the instructions.

---

## 💻 Running the Site Locally

If you want to preview your changes before pushing them live:

1. Open your terminal in the root directory of this project.
2. Run the Hugo development server:
   ```bash
   hugo server -D
   ```
   *(Note: You must have Hugo installed on your machine. We recommend the `hugo-extended` version).*
3. Open your browser to `http://localhost:1313/`

---

## 🚀 How to Deploy (Netlify)

This repository is already pre-configured to be deployed to [Netlify](https://www.netlify.com/) via the included `netlify.toml` file.

**Initial Setup:**
1. Log in to your Netlify dashboard.
2. Click **"Add new site"** -> **"Import an existing project"**.
3. Connect your GitHub account and select this repository (`cyberpunk-mod-list`).
4. Netlify will automatically read the config file. Just scroll down and click **"Deploy site"**!

**Updating the Live Site:**
Once connected to Netlify, updating your website is completely automatic. Whenever you edit the `mods.json` file or change text, simply commit your changes and push them to GitHub:

```bash
git add .
git commit -m "Updated mod links"
git push
```
Within seconds, Netlify will automatically rebuild your site and push your changes live!
