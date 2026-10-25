# Deta4Us — website

Professionele statische Nederlandstalige website voor Deta4Us, ontwikkeld voor GitHub Pages. Geen WordPress-abonnement en geen build-tool nodig.

## Bestanden
- index.html — responsive homepage, diensten, opdrachtgevers, professionals, contactformulier.
- privacy.html — privacyverklaring (controleer op juiste bedrijfsgegevens).
- favicon.svg — website-icoon.
- CNAME — gewenst hoofddomein: deta4us.com.
- .nojekyll — publiceert bestanden zonder Jekyll.

## Live zetten op GitHub Pages
1. Ga naar https://github.com/wienes-source/deta4us/settings/pages
2. Kies bij Build and deployment: Deploy from a branch.
3. Kies branch main en folder /(root), daarna Save.
4. Stel onder Custom domain deta4us.com in en kies Save. Verifieer bij voorkeur eerst het eigendom via GitHub.
5. Test de deployment. Zolang DNS nog naar WordPress wijst, blijft de WordPress-website zichtbaar op uw domein.

## DNS voor deta4us.com
Pas de DNS pas aan als u de nieuwe versie wilt inschakelen.
- A-records voor @: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153.
- CNAME voor www: wienes-source.github.io.
- Verwijder alleen conflicterende oude A/AAAA/CNAME records voor de website.
- Behoud bestaande MX, SPF, DKIM en DMARC e-mailrecords ongewijzigd.
- Schakel Enforce HTTPS in zodra GitHub dit mogelijk maakt.

DNS-wijzigingen kunnen tot 24 uur duren. Domeinregistratie en websitehosting zijn gescheiden.

Documentatie:
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Contactformulier
Het formulier post via https://formsubmit.co/ naar Deta4us@icloud.com. De eerste inzending leidt tot een bevestigingsmail aan dat adres. Activeer de koppeling met die e-mail; anders kunnen berichten niet worden bezorgd. Verifieer het juiste zakelijke ontvangstadres.

FormSubmit is een externe dienst en verwerkt persoonsgegevens bij inzendingen. Controleer de privacyverklaring en eventuele benodigde verwerkersafspraken voordat u de site definitief publiceert. GitHub Pages zelf ondersteunt geen PHP of server-side e-mail.

## Onderhoud
Pas HTML-bestanden aan via GitHub en commit naar main. Als GitHub Pages is ingeschakeld, publiceert het nieuwe versies automatisch.