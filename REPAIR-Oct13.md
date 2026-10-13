# Repair, October 13, 2026

RN asked for this site to be corrected after the Ask a Neuroscientist audit (`aan-studio/audit/nervous-system-studio.md` in rn-content-second-brain). What changed:

## Forms
- **Beta page and contact page:** both forms only saved entries in the visitor's own browser while promising a reply. They are gone. Each page now says plainly that it does not send anything and links to RN's contact page, https://rn-selected-work.vercel.app/contact. They were not wired to rn-api because there was no way to confirm the endpoint delivers to RN without sending a fake message.
- **Contact the Architect (footer button):** now shows a consent line above Send (what is collected: name, email, message; why: so RN can reply; who gets it: RN only) with a link to a privacy note, plus a required consent checkbox. It only says "sent" when rn-api answers with success; otherwise it says the message was not sent and links to the contact page. The "Sent!" alert is gone.
- **Privacy note:** new section "The Contact the Architect form" on the Safety and legal page (`#/disclaimer`).
- Removed the team email address on the `nervoussystem.studio` domain.

## Links
- Removed the Aloha AI Consulting link (no-JavaScript fallback and bottom credit line; the credit text "Built by Aloha AI" stays, unlinked) and the Myelin CE link (footer "Related tools"). They remain in git history.

## Cannabis and disclaimer
- "Education, not medical advice." now opens the site-wide safety line, so it shows on every page of the app and in the footer, and at the top of the dossier.
- Adults 21 and over notice: on the cannabis question in the Sensory Profile (before any cannabis option), the cannabis goals step, the optional cannabis section of the log form, the cannabis note on blueprints, the home and "Who it's for" cannabis cards, and the footer.

## Style
- All em and en dashes removed from `index.html`, the dossier and the README by rewording. Page ranges in citations now use a plain hyphen. No exclamation points remain.

## Citations (checked against PubMed)
- **Music meta-analysis:** the dossier cited *eClinicalMedicine* 2025; the Research page cited *Health Psychology Review* 2020 but linked to a different paper (Adiasto et al. 2022, *PLoS ONE*, which found no significant effect of music on stress recovery in healthy people). Both now cite de Witte et al. 2020, *Health Psychology Review* 14(2):294-324, doi:10.1080/17437199.2019.1627897 (104 RCTs; d = 0.380 physiological, 0.545 psychological). The 2025 *eClinicalMedicine* paper (music therapy and anxiety, doi:10.1016/j.eclinm.2025.103293) is listed as related on both.
- **"99%":** Gooley et al. 2011 found room light delayed melatonin onset in 99% of its 116 young adult participants and shortened melatonin duration by about 90 minutes. The dossier said it "suppresses and shortens melatonin in ~99% of people". Reworded to what was measured, with a note.
- **">50-fold":** Phillips et al. 2019 (PNAS) measured individual half-suppression doses from 6 to 350 lux (about 58-fold between the two most extreme of 55 people; the paper says "over an order of magnitude", 26% coefficient of variation). Replaced with the measured numbers and a note.

## Still open for RN
- Whether rn-api really delivers Contact the Architect messages to you (the endpoint answers, but delivery was not tested to avoid sending a fake lead).
- Whether "Built by Aloha AI" should stay as plain text.
- The dossier's full reference list still lives in six memos that are not in this repo.
- The "Support sleep routine" cannabis goal (audit item) was left as is.
