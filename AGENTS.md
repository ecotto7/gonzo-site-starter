# Hosting rules for this site

- Hosted on Netlify (team: Gonzo Systems). Plain HTML/CSS/JS, no build step.
- netlify.toml stays at the repo root with publish = "."
- Deploys happen ONLY by pushing to the main branch on GitHub.
  Never run `netlify deploy --prod` or deploy through the Netlify MCP
  unless I explicitly ask. Each production deploy costs 15 credits from
  a shared 300/month pool, and if it runs out every site pauses.
- Batch changes into one commit/push when possible.
- Pages use folder URLs: /about/ = about/index.html. Never rename or move a
  page without adding a 301 redirect in netlify.toml.
- Do not use Netlify Forms. Keep the live site's existing form, such as a
  JotForm embed, and do not rebuild it.
- Compress images before committing; keep them under ~300 KB where possible.
- Don't touch DNS or domain settings; I handle those manually.
