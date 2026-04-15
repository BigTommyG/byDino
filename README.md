# byDino – Nettside

Velkommen til kildekoden for **byDino** sin nettside! 🎉  
Dette er en enkel, rask nettside bygget med HTML, CSS og JavaScript – ingen fancy rammeverk, bare kode du selv kan lese og endre.

---

## 📁 Filstruktur

```
bydino/
├── index.html      ← Hele nettsiden (HTML + CSS + JS i én fil)
├── netlify.toml    ← Konfigurasjon for Netlify-hosting
└── README.md       ← Denne filen (instruksjoner)
```

---

## 🚀 Slik deployer du til Netlify (første gang)

Du trenger en **gratis Netlify-konto**. Gå til [netlify.com](https://netlify.com) og registrer deg.

### Alternativ A – Dra og slipp (enklest!)

1. Gå til [app.netlify.com](https://app.netlify.com)
2. Logg inn på kontoen din
3. Klikk **"Add new site"** → **"Deploy manually"**
4. Dra hele **`bydino`-mappen** inn i det blå feltet på skjermen
5. Netlify setter opp siden din automatisk – vanligvis på under ett minutt!
6. Du får en nettadresse som `storebror-katt-12345.netlify.app` – den kan du endre til noe penere (se under)

### Alternativ B – GitHub (anbefalt for fremtidige oppdateringer)

1. Opprett en gratis konto på [github.com](https://github.com)
2. Opprett et nytt **privat repository** (kall det f.eks. `bydino`)
3. Last opp filene dine dit
4. Gå til Netlify → **"Add new site"** → **"Import an existing project"**
5. Velg GitHub og velg ditt repository
6. La alle innstillingene stå som de er – Netlify finner `netlify.toml` automatisk
7. Klikk **"Deploy site"**

**Fordelen med GitHub:** Neste gang du endrer en fil og laster opp til GitHub, oppdaterer Netlify nettsiden din automatisk! ✨

---

## 🌐 Endre domenenavn

Den automatiske adressen fra Netlify er ikke så pen. Slik bytter du til noe bedre:

### Gratis Netlify-subdomene (f.eks. `bydino.netlify.app`)

1. Gå til **Site settings** → **Domain management**
2. Klikk **"Options"** ved siden av `.netlify.app`-adressen → **"Edit site name"**
3. Skriv inn `bydino` og lagre

### Eget domene (f.eks. `bydino.no`)

1. Kjøp et domene på f.eks. [domeneshop.no](https://domeneshop.no) (~120 kr/år for .no)
2. Gå til **Netlify → Domain management → Add custom domain**
3. Skriv inn domenenavnet ditt
4. Følg instruksjonene for å peke DNS-innstillingene mot Netlify
5. Netlify ordner HTTPS/SSL-sertifikat gratis og automatisk

---

## 📬 Netlify Forms – Motta forespørsler på e-post

Skjemaet på nettsiden bruker **Netlify Forms** for å sende forespørsler – ingen server nødvendig!

### Slik aktiverer du e-postvarsling:

1. Gå til [app.netlify.com](https://app.netlify.com) og velg siden din
2. Klikk på **"Forms"** i toppmenyen
3. Du skal se skjemaet som heter **"forespørsel"** etter at noen har sendt inn noe
4. Klikk på skjemaet → **"Form notifications"** → **"Add notification"**
5. Velg **"Email notification"**
6. Skriv inn e-postadressen du vil motta forespørsler på (f.eks. `post@bydino.no`)
7. Klikk **"Save"**

Nå får du en e-post hver gang noen sender inn en forespørsel! 📧

> **Tips:** På gratis Netlify-plan kan du motta opptil **100 innsendinger per måned** uten kostnad.

---

## ✏️ Slik oppdaterer du innholdet

All tekst og alle farger finner du i `index.html`. Her er de viktigste stedene å endre:

### Endre tekst

Åpne `index.html` i en teksteditor (f.eks. [VS Code](https://code.visualstudio.com/) – gratis).  
Bruk **Ctrl+F** (eller **Cmd+F** på Mac) for å søke etter teksten du vil endre.

| Hva du vil endre | Søk etter |
|---|---|
| Tagline i hero | `Har du en idé?` |
| Intro-tekst | `byDino er en 3D-printingtjeneste` |
| E-postadresse | `post@bydino.no` |
| Tjenestebeskrivelser | `Print fra din fil` / `Knekt del` / `Egne design` |
| Copyright-år | `© byDino 2025` |

### Endre farger

Øverst i `<style>`-blokken finner du CSS-variablene:

```css
:root {
  --farge-bakgrunn:  #0d0d0d;   /* bakgrunnsfargen (veldig mørk) */
  --farge-aksent:    #f97316;   /* oransje – endre denne for ny accentfarge */
  --farge-tekst:     #f5f5f5;   /* hvit tekst */
  /* ... osv. */
}
```

Bare bytt ut hex-verdien (f.eks. `#f97316`) med en ny farge.  
Du kan finne fine farger på [coolors.co](https://coolors.co).

### Endre fonter

Øverst i `<head>` finner du Google Fonts-lenken. Gå til [fonts.google.com](https://fonts.google.com),  
velg en ny font, og erstatt `Space+Grotesk` med fonten du valgte. Husk også å oppdatere  
`--font` i CSS-variablene.

---

## 🔁 Oppdatere nettsiden etter endringer

- **Dra-og-slipp-metoden:** Gå til Netlify, klikk på siden din, og dra mappen inn på nytt.
- **GitHub-metoden:** Lagre endringene dine i VS Code, "commit" og "push" til GitHub.  
  Netlify oppdaterer nettsiden automatisk innen 30 sekunder.

---

## 🐛 Noe fungerer ikke?

- Skjemaet vises ikke i Netlify Forms? Sjekk at du har lagt til `netlify` og `data-netlify="true"` i `<form>`-taggen (allerede gjort).
- Nettsiden lastes sakte? Prøv å slette nettleserbufferen (Ctrl+Shift+R).
- Spørsmål? Sjekk [Netlify-dokumentasjonen](https://docs.netlify.com) – den er veldig god!

---

Laget med ❤️ av **byDino**
