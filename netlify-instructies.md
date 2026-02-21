# 🚀 Nour Barbershop - Netlify Deployment Gids

De code van de website is nu **100% klaar en perfect geconfigureerd** voor Netlify.
Ik heb de volgende aanpassingen gedaan om fouten te voorkomen:
- Een `netlify.toml` configuratiebestand toegevoegd zodat Netlify precies weet wat hij moet doen (Vite build + redirects).
- De lokale widget link (`http://localhost:3000/...`) tijdelijk uitgecommentarieerd. Netlify draait namelijk op een beveiligde HTPPS (`https://`) verbinding, en browsers blokkeren onbeveiligde `http://` scripts automatisch. Zodra de SaaS backend online is met een beveiligde link, kun je deze weer aanzetten.

## Hoe zet je het online op Netlify? (2 Manieren)

### Manier 1: Via GitHub (Aanbevolen & Automatisch)
Dit is de beste manier. Bij elke aanpassing in de code in de toekomst, update de website automatisch.
1. Zorg dat deze map (`nour-barbershop`) op je GitHub staat.
2. Log in op **[Netlify](https://app.netlify.com/)**.
3. Klik op **"Add new site"** > **"Import an existing project"**.
4. Kies **GitHub** en selecteer je repository.
5. Netlify leest nu automatisch het `netlify.toml` bestand uit. Je hoeft dus **geen instellingen meer in te vullen**! 
6. Klik op **"Deploy site"** en binnen 1 minuut staat je site live.

### Manier 2: Handmatig Drag & Drop (Snelste manier voor nu)
Wil je de website direct online hebben zonder GitHub? Dat kan ook:
1. Open de terminal in de map `nour-barbershop` en draai het commando:
   ```bash
   npm run build
   ```
2. Er verschijnt nu een nieuwe map genaamd `dist`.
3. Log in op **[Netlify Drop](https://app.netlify.com/drop)**.
4. Sleep de **volledige `dist` map** in de browser. 
5. Je website staat direct online!

## Klaar! 🎉
Als alles is gelukt, kun je in Netlify nog de 'Site name' aanpassen zodat je een mooiere link krijgt zoals `nour-barbershop.netlify.app`, of natuurlijk een eigen `.nl` domeinnaam koppelen.
