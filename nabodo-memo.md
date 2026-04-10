# Nabodo memo v1.6.3
Stabil commit: d265caa (tag: stable-v1.6.3)
Rollback: git show d265caa:index.html > index.html && git add . && git commit -m "rollback v1.6.3" && git push && npx wrangler pages deploy . --project-name nabodo --commit-dirty=true
