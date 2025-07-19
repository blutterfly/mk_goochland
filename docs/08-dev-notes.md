# MkDocs Material site scaffold created ✅

## Resources

+ [Chatgpt](https://chatgpt.com/c/687ad3b6-4064-8328-b081-045638f6f264)  
+ [GitHub](https://github.com/blutterfly/mk_goochland)  
+ [Local Deployment](file://home/larry/mk/mk_goochland)  
+ [Download the project skeleton](sandbox:/mnt/data/goochland_site.zip)

---

## Setup

1. **Create & clone a repo**

   ```bash
   # in GitHub: new repo e.g. goochland
   git clone https://github.com/<your‑user>/goochland.git
   cd goochland
   ```

2. **Unzip the scaffold**

   ```bash
   unzip ~/Downloads/goochland_site.zip -d .
   # or move the contents of goochland_site/ into the repo root
   ```

3. **Set up a Python virtual environment**

   ```bash
   python -m venv .venv
   source .venv/bin/activate          # Windows: .venv\Scripts\activate
   pip install --upgrade pip
   pip install mkdocs-material
   ```

4. **Serve locally**

   ```bash
   mkdocs serve
   # Visit http://127.0.0.1:8000
   ```

5. **Commit & push**

   ```bash
   git add .
   git commit -m "Initial MkDocs Material site"
   git push origin main
   ```

6. **Deploy on GitHub Pages**

   *In repo → Settings → Pages*

   * Source: **GitHub Actions** (MkDocs) or **gh‑pages** branch.
   * URL will appear (e.g. `https://blutterfly.github.io/goochland`).

---

## Next Steps

* **Branding:** tweak `mkdocs.yml` palette or add `docs/stylesheets/extra.css`.
* **Content:** replace placeholders in `docs/` with detailed pages (lesson plans, booking info, maps).
* **Plugins:** add search (`pymdownx.superfences`), social cards, or i18n if needed.
* **CI:** enable the official *Material‑for‑MkDocs* GitHub Action for automatic deploys.

