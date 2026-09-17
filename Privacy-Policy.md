# Privacy Policy for Sideout

**Last updated: 17 September 2026**

Sideout is a volleyball scoring app for iOS, Android, macOS, and the web. The Dart package name is `volleyball_score`. This policy explains what we collect, why we collect it, and the choices you have.

If you do not agree with this policy, do not create an account. You can still score a Quick Match as a guest; that data stays on your device until you sign in.

**Contact:** [kaveebhashiofficial@gmail.com](mailto:kaveebhashiofficial@gmail.com)

---

## 1. Who we are

Sideout is operated by the independent developer who publishes the Sideout app (bundle ID `com.volleyballscore.volleyballScore`).

This policy covers the Sideout apps, any Sideout website or GitHub Pages site we publish, and the Sideout cloud services that sit behind them.

---

## 2. What this app does not do

Sideout does **not**:

- track you across other companies’ apps or websites
- show ads
- sell your personal information
- share your personal information for cross-context behavioural advertising
- collect precise location
- use App Tracking Transparency or an advertising identifier for tracking
- put passwords, session tokens, or Sign in with Apple identifiers in ordinary app preferences

Apple’s privacy manifest for Sideout declares `NSPrivacyTracking` as false.

---

## 3. Information we collect

### 3.1 Guest scoring (no account)

You can start a Quick Match without signing in. Match scores, team names, lineups, and the rally event log are stored **on this device** in a local database. They are not uploaded until you sign in.

Walk-in player names you save under Me → Walk-ins also stay on this device unless you later add them to a signed-in match or cup that syncs.

### 3.2 Account information

If you create an account or sign in, we collect:

| Data | Why |
| --- | --- |
| Email address | Sign-in, password reset, looking up a teammate by email when an organiser adds them to a roster |
| Password | Only if you choose email/password. Stored hashed by our auth provider. If you turn on Remember me, the password is kept in the device Keychain (iOS/macOS) or Keystore (Android), not in ordinary preferences |
| Display name and optional jersey number | Your player card, rosters, box scores, and leaderboards |
| Account ID | To own your matches and cups, join a team, and apply plan entitlements (Free or Club Pro) |
| Sign-in provider | Email/password, Sign in with Apple, and/or Google |

Sign in with Apple may give us an email (including Apple’s private relay) and, on first authorization, a name if you share one. Google Sign-In gives us the Google account identifier and verified email needed to create or link a Sideout account. We do not receive your Google or Apple password.

### 3.3 Match, cup, and roster data

When you are signed in, Sideout syncs the volleyball data you create so you can use it on another device:

- match rules, team names, officials, captains, lineups, and the rally event log (who won the point, and optional credits such as kill, ace, block, or error)
- tournaments (cups): format, teams, fixtures, schedule, awards you confirm
- player names and jersey numbers you enter, including walk-ins and teammates who join with an invite
- serving, substitutions, libero, sanctions, and remarks you record at the court desk

This is sports scoring data. It is linked to your account because you own the match or cup.

### 3.4 Public and shared content

Some data is visible to other people **because you chose to publish it**:

- **Spectator link.** SHARE assigns an unguessable token. Anyone with `/m/{token}` can see that match’s live or final score, sets, timeline, and result card.
- **Team invite.** An organiser can copy a join code or show a QR. Anyone with `/j/{token}` can look up the cup and team. Joining the roster requires a signed-in account.
- **Public cup.** If you list a cup publicly, other people can search for it, watch scores, and follow it. Invite tokens are stripped from public payloads. An empty search returns nothing.

Followed public cups are stored on the follower’s device. Followers cannot score.

### 3.5 Safety reports and blocks

If you report a profile, cup, match, or player, we store the subject, your reason (abuse, harassment, hate, spam, inappropriate, or other), optional details (up to 500 characters), and your account ID so we can review it.

If you block an account, we store that pair so public cups from that organiser drop out of your search. They are not notified.

### 3.6 Photos (Club Pro roster poster)

Club Pro can import a roster poster or score card from your **photo library**. Sideout asks for photo-library permission only for that feature.

- On iOS and macOS, Apple Vision can read names **on the device**.
- The image is also sent to our server so a vision model (Google Gemini, or OpenAI if Gemini is not configured) can extract team and player names. API keys stay on the server; they are not in the app.
- We use the photo to create sides and walk-in names. We do not build a photo gallery, and we do not use the image for advertising.

You can drop a misread name before or after it is applied.

### 3.7 Device and app settings

On the device we store:

- tutorial completion (ordinary app preferences)
- Remember me email (ordinary app preferences) and password (Keychain / Keystore)
- session token (Keychain / Keystore)
- Sign in with Apple user identifier (Keychain / Keystore), so we can detect a revoked or transferred Apple credential
- local matches, cups, walk-ins, follows, and blocks (on-device database)

Appearance (light / dark / system) and sunlight mode currently live in memory for the session; they are not uploaded.

We do not collect crash analytics, advertising IDs, or usage telemetry beyond what your operating system and our hosting provider record as ordinary server logs (for example, that a signed-in request reached the API).

### 3.8 Children

Sideout is built for gyms, clubs, and adult organisers. It is **not directed at children under 13**. Do not create an account if you are under 13. A parent or guardian may score as a guest on their own device. We do not knowingly collect personal information from children under 13. If you believe we have, email us and we will delete it.

---

## 4. How we use information

We use this information to:

- run scoring, sync, tournaments, invites, spectator links, and your account
- show you as a player on a roster when you join or when an organiser adds you
- apply Free or Club Pro access
- generate a QR image for a join or share link
- read a roster poster you chose (Club Pro)
- review reports and honour blocks
- delete your account when you ask
- keep the service secure (HTTPS only; session secrets in Keychain / Keystore)

We do **not** use this information to profile you for ads or to train a public generative model as a separate product. Roster-poster images are sent to a vision model solely to extract the printed teams and names you asked us to import.

---

## 5. Who we share information with

We share data only as needed to run Sideout:

| Recipient | Role |
| --- | --- |
| **Supabase** | Authentication, database, realtime spectator updates, and edge functions (including account deletion and roster-poster read). Matches and cups you own are stored there when you are signed in |
| **Apple** | Sign in with Apple |
| **Google** | Google Sign-In (OAuth) and, for Club Pro poster import, Gemini vision |
| **OpenAI** | Optional fallback for Club Pro poster import if Gemini is not configured |
| **QRServer (api.qrserver.com)** | Renders a QR image from the join or share URL. Only http(s) invite or spectator URLs are sent |
| **Other Sideout users** | Teammates, spectators with your share link, and people who find a cup you listed as public |
| **Authorities** | If required by law, or to protect people from serious harm |

We do not sell personal information.

Processors may store or process data outside your country (including the United States). They act on our instructions for Sideout.

---

## 6. Legal bases (EEA, UK, Switzerland)

If those laws apply, we process personal data because:

- **Contract.** Creating an account, syncing matches, joining a team, and publishing a share link are needed to provide the service you asked for.
- **Legitimate interests.** Keeping the product secure, reviewing abuse reports, and operating public cups you chose to list.
- **Consent.** Sign in with Apple or Google, photo-library access, Remember me, and optional public listing or sharing. You can withdraw consent by disconnecting the provider, denying photo access in system settings, turning off Remember me, unlisting the cup, or deleting the share by deleting the match or account.

---

## 7. Retention

| Data | Kept until |
| --- | --- |
| Guest scores that never synced | You delete the match, clear app data, or uninstall |
| Signed-in matches, cups, profile | You delete them, or you delete the account |
| Spectator token | Until the match is deleted or the account that owns it is deleted |
| Blocks | Until you unblock or delete your account |
| Abuse reports | As long as needed to review safety. Deleting your account removes reports you filed; reports about content may be kept with the subject identifier |
| Poster image in transit | For the length of the read request. We do not keep a poster album |
| Server logs | Short-lived operational logs on the host |

Deleting the Sideout account (Me → Account → Delete account, or Settings) permanently deletes the auth user. Cloud matches, cups, and profile rows that belong to that user are removed with it. Local guest scores that were never synced stay on the device. This cannot be undone.

If you used Sign in with Apple, you can also stop sharing in Apple ID settings. We check Apple credential state and sign you out if the credential is revoked or transferred.

---

## 8. Your rights

Depending on where you live, you may have the right to access, correct, delete, export, or restrict personal data, and to object to certain processing.

In the app you can:

- edit your display name and jersey
- delete a match or cup you manage (with confirmation)
- unlist a public cup
- remove a walk-in or a misread poster name
- block or report
- delete your account

To request a copy of your cloud data, or if the in-app controls are not enough, email [kaveebhashiofficial@gmail.com](mailto:kaveebhashiofficial@gmail.com) from the address on the account. We may need to verify that it is you.

California residents: we do not sell or share personal information as those terms are used in the CCPA/CPRA for advertising. You can still delete your account in the app.

---

## 9. Security

- Transport is HTTPS only.
- Session tokens, remembered passwords, and the Sign in with Apple user identifier use the system Keychain or Keystore.
- Cloud rows are scoped to your account except for the public paths you turn on (spectator token, public cup search, join-token lookup).
- Clients cannot change their own plan or role.
- We do not put API keys for vision models in the app.

No method of transmission or storage is perfectly secure. Do not put highly sensitive personal data in team names, remarks, or walk-in names.

---

## 10. International users

Sideout may be used from many countries. Your information may be processed in the country where our hosting and auth providers operate. By using a signed-in Sideout account, you understand that your scoring data is stored in the cloud so the app can sync.

---

## 11. Third-party policies

- [Supabase](https://supabase.com/privacy)
- [Apple Privacy Policy](https://www.apple.com/legal/privacy/)
- [Google Privacy Policy](https://policies.google.com/privacy)
- [OpenAI Privacy Policy](https://openai.com/privacy/)
- [QRServer / goQR](https://goqr.me/de/rechtliches/datenschutzerklaerung.html)

Opening a spectator or join link in a browser is also subject to that browser’s own practices.

---

## 12. Changes

We may update this policy when the product changes (for example, if we add in-app purchases, push notifications, or a hosted website origin for invite links). The “Last updated” date at the top will change. Continued use after an update means you accept the revised policy. If a change is material, we will say so in the app or by email where we can.

---

## 13. Contact

Questions, privacy requests, or a request to delete data:

**Email:** [kaveebhashiofficial@gmail.com](mailto:kaveebhashiofficial@gmail.com)

**App:** Sideout — Me → Account → Delete account
