# CONTENT.md — Translation source-of-truth

This file is the canonical reference for all user-facing strings on the UPN Migration Hub. Translators should update the SV / NO columns and then sync each cell into the corresponding HTML file. The DOM structure (IDs, classes, element order) must stay identical across `/en/`, `/sv/`, `/no/` — only text content differs.

**Translation status:**
- 🇬🇧 EN: ✅ Complete (source of truth)
- 🇸🇪 SV: ⏳ Pending — Swedish reviewer assigned
- 🇳🇴 NO: ⏳ Pending — Norwegian reviewer assigned

**Style notes for translators:**
- Tone: direct, friendly, non-jargon. We're explaining a change to clinicians, not engineers.
- Keep technical terms in English where the system UI is English (e.g. "Other user" on Windows is shown in English regardless of OS locale at Kry/Livi).
- `@ad.kry.se` and `@kry.se` are literal strings — do not translate.
- "HCP" is healthcare professional — translate to local conventions (vårdpersonal / helsepersonell) or keep as HCP if widely understood.
- Project code "ITA-1779" stays as-is.

---

## Page titles & metadata

| Where | EN | SV | NO |
|---|---|---|---|
| `<title>` index | Your login is changing — UPN Migration Hub \| Kry/Livi | _TODO_ | _TODO_ |
| `<title>` login-guide | Login guide — UPN Migration Hub \| Kry/Livi | _TODO_ | Endre brukernavn og utloggingsprosess \| Kry/Livi |
| meta description (index) | Information about Kry/Livi's UPN migration: what's changing, when it happens, and what you need to do. | _TODO_ | _TODO_ |

## Site navigation (top bar)

| Where | EN | SV | NO |
|---|---|---|---|
| `.brand` | UPN Migration Hub | _TODO_ | _TODO_ |
| nav link 1 | Home | Hem | Hjem |
| nav link 2 | Login guide | Inloggningsguide | Innloggingsguide |
| nav link 3 | Apps | Appar | Apper |
| nav link 4 | FAQ | Vanliga frågor | Ofte stilte spørsmål |
| nav link 5 | Support | Support | Support |

## Hero (home page)

| Where | EN | SV | NO |
|---|---|---|---|
| eyebrow | Active project · ITA-1779 | Aktivt projekt · ITA-1779 | Aktivt prosjekt · ITA-1779 |
| h1 | Your login username is changing | _TODO_ | _TODO_ |
| lead paragraph | We're simplifying how you log in to your Kry/Livi computer. Your username is moving from `@ad.kry.se` to `@kry.se`. There's a small action you'll need to take the first time you log in after the change. | _TODO_ | _TODO_ |
| hero-key label | Your new login | Ditt nya inloggningsnamn | Ditt nye brukernavn |
| pwd-note | Your password stays exactly the same. | Ditt lösenord förblir oförändrat. | Passordet ditt forblir uendret. |

## Timeline section

| Where | EN | SV | NO |
|---|---|---|---|
| section num | 01 / TIMELINE | 01 / TIDSPLAN | 01 / TIDSPLAN |
| h2 | When does this happen for me? | _TODO_ | _TODO_ |
| sub | The rollout happens in waves, by country and clinic group. Changes are applied overnight on a Sunday, so you'll notice them the following Monday. | _TODO_ | _TODO_ |
| Norway date | Sunday 25 May 2026 | Söndag 25 maj 2026 | Søndag 25. mai 2026 |
| Norway meta | ~39 HCPs · BA Norway Clinicians Remote | _TODO_ | _TODO_ |
| Sweden date | Phased through June 2026 | _TODO_ | _TODO_ |
| Sweden meta | ~800+ HCPs · 40+ clinic locations | _TODO_ | _TODO_ |
| status pill | ⏳ Upcoming | ⏳ Kommande | ⏳ Kommende |
| phase: June W1 | Stockholm inner | Stockholm inre | Stockholm indre |
| phase: June W2 | Sweden outer | Sverige yttre | _N/A — Sverige_ |
| phase: June W3 | Digital / Remote | Digital / Distans | _N/A — Sverige_ |

## Important callout

| Where | EN | SV | NO |
|---|---|---|---|
| callout body | **Important:** on your first login after the change date, you must click **"Other user"** on the Windows login screen — don't tap your existing profile tile. | _TODO_ | _TODO_ |
| callout 2nd line | If you click your existing profile, the login will fail. See the **step-by-step login guide** with screenshots before your first login. | _TODO_ | _TODO_ |

## Action steps (3-up)

| Where | EN | SV | NO |
|---|---|---|---|
| section num | 02 / WHAT YOU NEED TO DO | 02 / VAD DU BEHÖVER GÖRA | 02 / HVA DU MÅ GJØRE |
| h2 | First login after the change — three steps | _TODO_ | _TODO_ |
| sub | A quick summary. For the full walkthrough with screenshots, see the login guide. | _TODO_ | _TODO_ |
| Step 1 h3 | Confirm the change | Bekräfta ändringen | Bekreft endringen |
| Step 1 bullet 1 | Check you've received the IT confirmation email that your username has been updated. | _TODO_ | _TODO_ |
| Step 1 bullet 2 | Your new username will be **firstname.lastname@kry.se** | _TODO_ | _TODO_ |
| Step 2 h3 | Sign out of your computer | Logga ut från datorn | Logg ut fra datamaskinen |
| Step 2 bullet 1 | Click the **Windows (Start)** button. | Klicka på **Windows (Start)**-knappen. | Klikk på **Windows (Start)**-knappen. |
| Step 2 bullet 2 | Click your **profile name / icon**. | Klicka på ditt **profilnamn/ikon**. | Klikk på **profilnavnet/ikonet** ditt. |
| Step 2 bullet 3 | Select **"Sign out"**. | Välj **"Logga ut"**. | Velg **"Logg ut"**. |
| Step 3 h3 | Sign in with your new username | Logga in med ditt nya användarnamn | Logg inn med nytt brukernavn |
| Step 3 bullet 1 | On the login screen, look at the **bottom-left**. | _TODO_ | På innloggingsskjermen, se **nederst til venstre**. |
| Step 3 bullet 2 | Click **"Other user"**. | Klicka på **"Annan användare"**. | Klikk på **"Annen bruker"**. |
| Step 3 bullet 3 | Enter your **new username** and your **existing password**. | _TODO_ | Skriv inn det **nye brukernavnet** og det **eksisterende passordet**. |
| read-more link | Read the full guide → | Läs hela guiden → | Les hele guiden → |

## App impact section

| Where | EN | SV | NO |
|---|---|---|---|
| section num | 03 / IMPACT ON YOUR APPS | 03 / PÅVERKAN PÅ DINA APPAR | 03 / PÅVIRKNING PÅ APPENE DINE |
| h2 | What changes — and what doesn't | _TODO_ | _TODO_ |
| sub | Most of your apps will continue working with no action needed. A small number of systems IT doesn't control may still show your old username — this is expected. | _TODO_ | _TODO_ |
| Good card h3 | ✓ Working as normal | ✓ Fungerar som vanligt | ✓ Fungerer som normalt |
| Good card note | Other apps via MyApps/SSO (Zendesk, WinningTemp, Anaplan, Contentful, WorkRamp, Sana, Printer Logic, XM Fax, TeamTailor) continue working with no action needed. | _TODO_ | _TODO_ |
| Warn card h3 | ! May still show your old username | ! Kan fortfarande visa ditt gamla användarnamn | ! Kan fortsatt vise ditt gamle brukernavn |
| Warn card note | If something *stops working* (rather than just showing the old username), raise a Zendesk ticket and we'll investigate. | _TODO_ | _TODO_ |

App labels (keep names, translate "chats, calls, meetings" etc.):
- **Microsoft Teams** — chats, calls, meetings / chatt, samtal, möten / chat, samtaler, møter
- **Outlook** — email and calendar / e-post och kalender / e-post og kalender
- **SharePoint & OneDrive** — files and folders / filer och mappar / filer og mapper
- **MyApps / SSO** — most enterprise applications / de flesta företagsapplikationer / de fleste virksomhetsapplikasjoner
- **VLS** — handled automatically via SCIM (same in all)
- **Quinyx** — scheduling / schemaläggning / planlegging
- **Workday** — HR system (same in all)

## FAQ items

For brevity, FAQ questions and answers are not duplicated here in full. Source-of-truth English copy lives in `/en/index.html` `#faq` section and `/en/login-guide.html` `#troubleshooting` section. Translators should:
1. Read the EN copy in those files
2. Translate question (in `<summary>`) and answer (in `<div class="faq-body">`)
3. Keep `<code>`, `<strong>`, `<a>` tags and their `href`/`target`/`rel` attributes intact

## Support banner

| Where | EN | SV | NO |
|---|---|---|---|
| h2 | Need help? IT is here. | Behöver du hjälp? IT finns här. | Trenger du hjelp? IT er her. |
| body | If you can't log in, see something unexpected, or want to double-check before the change — raise a ticket and the IT Service Desk will help you. | _TODO_ | _TODO_ |
| primary button | Open a Zendesk ticket → | Öppna ett Zendesk-ärende → | Opprett en Zendesk-sak → |
| secondary button | Reset your password | Återställ ditt lösenord | Tilbakestill passordet |
| teams note | Or ask in **#it-support** on Teams | Eller fråga i **#it-support** på Teams | Eller spør i **#it-support** på Teams |

## Footer

| Where | EN | SV | NO |
|---|---|---|---|
| left | UPN Migration · Project ITA-1779 · Last updated May 2026 | UPN-migrering · Projekt ITA-1779 · Senast uppdaterad maj 2026 | UPN-migrering · Prosjekt ITA-1779 · Sist oppdatert mai 2026 |
| right | Kry / Livi · IT | Kry / Livi · IT | Kry / Livi · IT |

## Login guide page — step descriptions

| Where | EN | SV | NO |
|---|---|---|---|
| h1 | First login after the change | _TODO_ | Første innlogging etter endringen |
| Step 1 h3 | Confirm the change | _TODO_ | Bekreft endringen |
| Step 2 h3 | Sign out of your computer | _TODO_ | Logg ut fra datamaskinen |
| Step 3 h3 | Sign in with your new username | _TODO_ | Logg inn med nytt brukernavn |
| Screenshot caption (signout) | Start menu → click profile → Sign out | _TODO_ | Startmeny → klikk profil → Logg ut |
| Screenshot caption (other user) | Login screen → click **Other user** at bottom-left | _TODO_ | Innloggingsskjerm → klikk **Annen bruker** nederst til venstre |
| Screenshot caption (new creds) | Enter `firstname.lastname@kry.se` + your existing password | _TODO_ | Skriv inn `firstname.lastname@kry.se` + ditt eksisterende passord |
| Back-home link | ← Back to UPN Migration Hub | ← Tillbaka till UPN-migreringshubben | ← Tilbake til UPN-migreringshuben |
| Troubleshooting h2 | If something goes wrong | _TODO_ | Hvis noe går galt |

---

## Process for updating translations

1. Open this file. Update the SV or NO column for the row you're working on (replace `_TODO_` with the translation).
2. Open the matching HTML file (`/sv/index.html`, `/sv/login-guide.html`, `/no/index.html`, `/no/login-guide.html`).
3. Find the matching text (EN copy is still there as placeholder) and replace with the translation.
4. Keep all HTML tags, attributes, and links intact — only change text nodes.
5. When all rows for a language have a value (no more `_TODO_`), remove the `<!-- TRANSLATION PENDING ... -->` comment block from the top of the corresponding HTML files.
6. Update the translation status at the top of this file when a language is complete.
