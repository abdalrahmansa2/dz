Digital Zone static site
Build date 2025-09-19 07:36

Contents
- index.html  Home
- news.html   News
- product.html Products
- projects.html Projects
- store.html  Store
- contact.html Contact
- dashboard.html Admin mockup
- 404.html     Not found page
- robots.txt   Crawler rules
- sitemap.xml  Basic sitemap

Deploy on shared hosting
1. Extract the zip into public_html
2. Ensure index.html is at the root
3. Test with your domain

Deploy on Nginx
server {
  listen 80;
  server_name your-domain.com;
  root /var/www/your-domain;
  index index.html;
  location / {
    try_files $uri $uri/ =404;
  }
}

Deploy on Netlify
1. New site from zip
2. Drag and drop the zip
3. Set publish directory to root

Deploy on Vercel
1. vercel --prod in the folder
2. Framework preset None
3. Output directory .