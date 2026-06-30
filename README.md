# TaskQuest RPG GitHub Pages policy draft

Created: 2026-06-30
Status: draft only. Not deployed, not store evidence.

## Target URLs

- Privacy Policy: `https://horusuzu.github.io/taskquest-rpg-policy/privacy/`
- Support: `https://horusuzu.github.io/taskquest-rpg-policy/support/`
- Terms: `https://www.apple.com/legal/internet-services/itunes/dev/stdeula/`
- Support email: `burningtribesuzu@gmail.com`

## Files to publish

Copy this directory's contents to a public GitHub Pages repo named `taskquest-rpg-policy`.

```text
privacy/index.html
support/index.html
```

## Publish gate

Do not update App Store Connect, Google Play, or in-app constants until all checks pass:

```bash
curl -IL https://horusuzu.github.io/taskquest-rpg-policy/privacy/
curl -IL https://horusuzu.github.io/taskquest-rpg-policy/support/
```

Required readback:

- HTTP 200, no login, no redirect to an editor or account page
- Privacy page includes `TaskQuest RPG`, `inc.burningtribe.taskquest`, AI processing, RevenueCat purchases, no AdMob/no tracking
- Support page includes contact email and links to the same privacy URL
- No `burningtribe.tokyo`, `burningtribe.jp`, Google Sites, PDF, Drive, Notion, or raw markdown URL is used as the store URL

## After 200 OK

Update these local/store surfaces to the target URLs:

- `src/App.tsx` `PRIVACY_POLICY_URL`
- `STORE.md` privacy policy URL
- `STORE_SUBMISSION_RUNBOOK.md`
- App Store Connect privacy/support URL fields
- Google Play App content privacy policy URL

Store write/upload/submit/country changes still require explicit owner approval.
