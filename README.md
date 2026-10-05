# ECR Generator – ₹25,000 wage ceiling

Static web tool: upload an ECR Excel (template or old-style ECR sheet) → applies the
₹15,000 → ₹25,000 ceiling (w.e.f. 17.09.2026, pro-rata 16/14 days for Sep-2026) →
downloads the ECR 2.0 text file (`#~#` separated). All processing is in the browser.

- `site/index.html` – the app
- `site/vendor/xlsx.full.min.js` – SheetJS 0.18.5 (served locally, no CDN needed)
- `site/files/ECR_Template_25000_Ceiling.xlsx` – blank Excel template
- `Dockerfile` + `nginx.conf` – for Coolify (build pack: Dockerfile, port 80)

Run locally: `docker build -t ecr25000 . && docker run -p 8080:80 ecr25000` → http://localhost:8080
