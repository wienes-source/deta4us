# Deta4Us — één website, geen dubbele pagina's

Deze GitHub-repository is de **broncode** voor de vernieuwde website. De bestaande WordPress-website op deta4us.com is nog live. Geen DNS of WordPress-instellingen wijzigen voordat de nieuwe hosting getest is.

## Samengevoegde inhoud

- **index.html**: één homepage met alle diensten, opdrachtgeverinformatie, kandidaten, starters, internationale professionals, functieprofielen, werkwijze en één contactformulier.
- **privacy.html**: de privacyverklaring voor het nieuwe formulier.
- **voorwaarden.html**: de bestaande algemene voorwaarden (oorspronkelijke WordPress-versie november 2025). Controleer vóór livegang of deze zakelijk en juridisch nog kloppen.
- **_redirects**: mapping van 26 oude WordPress-URL's naar de samengevoegde onderdelen; werkt bij Netlify.
- **bedankt.html**, **404.html**, **favicon.svg**, **sitemap.xml**, **robots.txt**, **.nojekyll**, **CNAME**: functionele ondersteunende bestanden, geen dubbele openbare dienstenpagina's.

## Waarom niet rechtstreeks GitHub Pages?

GitHub Pages is volgens de eigen voorwaarden niet bedoeld als gratis hosting om een commerciële bedrijfswebsite te exploiteren. Gebruik GitHub daarom voor **versiebeheer** en een voor commercieel gebruik geschikte host, bijvoorbeeld **Netlify Free** (controleer de actuele limieten). Vercel Hobby is evenmin geschikt voor bedrijfsmatig gebruik zonder passend betaald plan.

## Beoogde livegang: GitHub → Netlify → deta4us.com

1. Koppel het bestaande repository `wienes-source/deta4us` aan een bestaand of nieuw Netlify-account. Maak **geen extra Deta4Us-repository**.
2. Publiceer branch `main`, met repository-root als publicatiedirectory, zonder buildcommand.
3. Test de gegenereerde `*.netlify.app` URL op mobiel en desktop. Controleer links, documenten, toegankelijkheid, SEO en formulieren.
4. Vergelijk eerst alle bestaande WordPress-pagina's met de samengevoegde website. **Unieke pagina's** (oude nieuwsarchieven, brochures, specifieke vacaturedetails, teamprofielen en andere informatie) zijn nog niet allemaal volledig overgenomen. Migreer of archiveer bewust; zet het hoofddomein pas daarna om.
5. Voeg in Netlify het aangepaste domein `deta4us.com` en de `www`-variant toe en verkrijg de EXACTE DNS-instructies van Netlify.
6. Wijzig bij WordPress.com DNS uitsluitend de webrecords die met die instructies conflicteren. Behoud MX, SPF, DKIM, DMARC en de domeinregistratie.
7. Controleer geldige HTTPS-certificaten, `deta4us.com`, `www.deta4us.com` en oude URL-redirects.
8. Verzend een eerste testformulier; bevestig de activatiemail van **FormSubmit** in `Deta4us@icloud.com`. Verzend vervolgens een tweede test om de daadwerkelijke aflevering te controleren.
9. Alleen nadat alle controles slagen: beoordeel of het betaalde WordPress Personal-abonnement moet worden beëindigd. **Zeg de losse domeinregistratie nooit per ongeluk op.**

## Opmerkingen over overgenomen informatie

De oude WordPress-website had tegenstrijdige e-mailadressen, telefoonnummers en vestigingsgegevens; voor de nieuwe pagina is voorlopig uitsluitend `Deta4us@icloud.com` gehanteerd, omdat dat op de bestaande Contact-pagina staat. Verifieer het gewenste officiële bedrijfsadres, handelsregistratie en contactnummer voordat ze openbaar worden overgenomen.

De oude pagina's bevatten historische vacatures en ambitieuze claims (zoals gegarandeerde bonussen en aantallen kandidaten). Die claims zijn niet overgenomen. De enkele functieprofielsectie bevat **voorbeelden**, geen garantie dat een vacature nog openstaat.

De privacyverklaring en algemene voorwaarden vereisen een inhoudelijke check op actuele bedrijfsgegevens, juridische verplichtingen en gegevensverwerking door externe formulierdienst FormSubmit.

## Technisch

HTML/CSS en enkele regels JavaScript. Geen buildstap, geen database, geen API-sleutels of geheimen in dit openbare repository. Het contactformulier gebruikt een externe dienst; GitHub zelf verzendt geen e-mails.

Bronnen:
- GitHub Pages beperkingen: https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits
- Netlify Free: https://www.netlify.com/pricing/
- Netlify Git deployment: https://docs.netlify.com/build/configure-builds/repo-permissions-linking/
