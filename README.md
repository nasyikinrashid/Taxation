# Income Harbour

**Malaysian Taxation: Other Income — Individuals**  
English · Diploma in Accounting · YA 2025 · 16 questions · 20–25 minutes

A complete cargo-routing learning game written in plain HTML, CSS and JavaScript. Students steer a boat towards an answer dock and dispatch an income file. Correct treatment clears the cargo and opens the next part of the route. Wrong treatment gives an explanation and requires a retry. There is one complete game, with four checkpoints.

## Learning outcome

By the end, students can classify common individual other-income receipts under sections 4(c)–(f), identify selected exemptions and calculate simple income amounts after allowable expenses and exemptions.

Coverage: dividends, interest and discounts (category); non-business rent; royalties; pensions; annuities; residual revenue gains. Questions progress from classification to exemptions, calculations and a new mixed-income case.

## Folder structure

```text
income-harbour-github-pages.zip
├── index.html
├── style.css
├── script.js
├── README.md
├── TEACHER_ANSWER_KEY.md
└── FULL_CODE.md
```

`index.html` is at the ZIP root: extract all files together into a folder of your choice. `FULL_CODE.md` contains the complete text of the HTML, CSS, JavaScript, README and teacher key, each labelled by its exact filename. It is a reference copy; edit the actual files to change the game.

All artwork is inline SVG or CSS. No additional asset downloads, backend, database, API key, package install or build command is required. The default is silent; optional short sound effects are synthesised by the browser, with no audio file. No student data is sent or stored. Home, refresh and closing the page clear the session. No persistence or leaderboard is implied.

## Play and controls

1. Open the homepage. Leave the default **Untimed** option, or select the optional practice stopwatch.
2. Choose **Play the game**.
3. Read the file and task. Click/tap an answer dock, use keys 1–4, or steer with left/right arrows or A/D.
4. Choose **Dispatch cargo**, or press Enter while the game area, a dock or a steering button is focused.
5. Read the feedback. Choose **Continue** when correct, or **Continue to retry** after a mistake. There is no automatic advance.
6. Use **Previous** to review earlier files, then **Next** to return. Unsolved files cannot be skipped. Review cannot add points.
7. After the final correct answer, choose **Continue to results**. Open each learning-log entry for the original choice, correct answer and explanation. **Print report** expands all entries and opens the browser print dialog.
8. **Restart voyage** asks before clearing attempts; **Home** clears the current session immediately. **Play again** starts fresh in untimed mode.

Tab and Shift+Tab move between controls. Enter/Space activate focused buttons. Dialogs have explicit close buttons and support Escape. Reduced-motion preferences suppress boat transitions.

## Scoring and learning support

- **Independent score:** 1 point for a correct first attempt without opening that file's Rule card. Maximum 16.
- **Assisted first attempt:** a correct first attempt after opening the Rule card. It is reported separately and gives no independent point.
- **Retry:** a wrong answer gives feedback; the student must answer correctly before progressing. A later correct answer delivers the cargo but does not restore a first-attempt point.
- **First-attempt accuracy:** independent plus assisted first-attempt answers, reported separately from the independent score.
- **Physical skill and speed:** earn no points. No collisions, aiming tests, timers that end a question, lives or game-over penalties.
- **Optional stopwatch:** active answering time only. It pauses during feedback, review, instructions, restart dialogs and when the page is hidden. It is not a test score or a deadline.
- Every answer is locked immediately when dispatched. Repeated clicks or keys cannot add points or attempts while feedback is open.

The final question is a new combination of income sources to check transfer. The result says whether it was solved independently, with support or after feedback. This is formative practice: a correct retry shows completion after feedback, not independent mastery.

## Test locally — no installation

1. Download and extract the ZIP. Do not open HTML inside the ZIP preview.
2. Double-click `index.html` to open it in a modern browser (Chrome, Edge, Firefox or Safari).
3. Keep `style.css` and `script.js` in the same folder as `index.html`.
4. The game works offline. Internet is only needed to visit the optional official-source links.

If the browser blocks local JavaScript because of an institutional policy, use the GitHub Pages URL or ask your IT team about the policy. The website does not require a server to run.

## Upload to GitHub and publish with GitHub Pages

1. Sign in to GitHub and create a repository, for example `income-harbour`. A public repository works with GitHub Free; private-repository Pages availability depends on the account plan.
2. Open the repository and choose **Add file → Upload files**. Upload the extracted files, not the ZIP. The three website files must be directly at the repository root. Do not upload an extra enclosing folder.
3. Commit the upload to the `main` branch. The Markdown documentation files may be uploaded too; they are not needed for gameplay.
4. Open **Settings → Pages**. In **Build and deployment → Source**, choose **Deploy from a branch**.
5. Select **main**, choose **/(root)**, then **Save**.
6. Wait for GitHub to finish publishing. Open the URL shown on the Pages screen. A project site normally uses `https://YOUR-USERNAME.github.io/income-harbour/`; use the actual link GitHub supplies.
7. To update the site, commit your edited files to `main` and wait for the Pages deployment to finish. Hard-refresh the page if you still see the previous version.

No repository or deployment was created on your behalf. These files are prepared for you to upload.

Official GitHub instructions:  
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

Troubleshooting: a 404 usually means the wrong publishing folder, no completed deployment, or `index.html` not being at its root. Styling missing usually means a renamed/missing `style.css` or different capitalisation. File names and relative paths must match exactly.

## Edit the questions

Open `script.js` in a text editor. Find **EDITABLE QUESTION BANK** at the top. Each case has this structure:

```javascript
{
  id: 'NEW01',
  topic: 'Classification',
  title: 'A short case title',
  q: 'Put the case facts here.',
  ask: 'What should the student determine?',
  options: ['Answer A', 'Answer B', 'Answer C', 'Answer D'],
  correct: 1,
  why: 'Explain the correct answer, calculation and likely mistake.',
  hint: 'A rule or thinking prompt for the optional Rule card.'
}
```

`correct` is zero-based: 0 = A, 1 = B, 2 = C, 3 = D. Keep exactly four distinct answer options. Keep `id` unique. `q` can contain `\n` to start a new line. Keep question text as plain text, not HTML. Escape apostrophes if you use single-quoted JavaScript strings, or use double quotes around the string. Preserve commas between objects.

You may add or remove cases; progress, scoring and checkpoint groupings adapt automatically to the number of questions. The default bank has four questions per checkpoint. The four checkpoint names are in `STOPS`; edit them if your sequence changes. Keep the last question a fresh application case. Update the learning outcome, homepage duration, year, instructions, teacher key and source notes if you change the teaching scope. The stopwatch does not affect question order.

After edits, run through the altered cases in a browser. Check the answer index, arithmetic, feedback and mobile text wrapping. A malformed bank produces a console error instead of silently using an invalid answer. All answers are present in client-side JavaScript, so this is a practice tool rather than a secure examination system.

## Tax scope and assumptions

Unless a question states otherwise, the taxpayer is a Malaysian tax-resident individual and the receipts are Malaysian-source receipts in YA 2025. Classification is considered separately from exemption. Cases explicitly state eligibility or the necessary facts for calculations.

- Section 4(c): dividends, interest and discounts.
- Section 4(d): non-business rent, royalties and premiums.
- Section 4(e): pensions, annuities and other qualifying periodical payments.
- Section 4(f): revenue gains not falling into an earlier category; a one-off receipt is not automatically exempt, taxable, or in 4(f).
- Deposit interest cases distinguish qualifying personal deposits with a Malaysian licensed bank from a private loan.
- Royalty cases use the stated qualifying exemptions. Translation eligibility and literary-publication eligibility are expressly given, rather than assumed for every payment.
- Pension questions specify Malaysian source, Government payment or an approved scheme, retirement conditions and the number of pensions.
- Rental calculations use a non-business source with allowable expenses stated. First-tenant costs are distinguished from costs of renewing an established tenancy. Specialist rental losses, deposits and capital allowances are outside scope.
- YA 2025 dividends: the game teaches the annual RM100,000 threshold and 2% rate on chargeable dividend income. It does not imply that all dividends are taxable or that final tax is always simply 2% of gross dividends less RM100,000. The threshold question asks only for the excess before later deduction allocation.
- The final sum is income after source expenses/exemptions and before personal reliefs, not tax payable.

Foreign-source income, complex business-source decisions, trusts, non-resident withholding tax and a full individual tax-payable computation are outside this game. Review the question bank against the syllabus and relevant YA before adapting it.

## Official tax sources checked

1. **LHDN, Form BE YA 2025 Explanatory Notes**, B2 and B3/B4: dividend rules; interest, royalties, pensions, annuities and other gains.  
   https://www.hasil.gov.my/wp-content/uploads/explanatorynotes_be2025_2.pdf
2. **LHDN Public Ruling 12/2018, Income From Letting of Real Property**, paragraphs 5 and 8.2–8.3: non-business letting, deductible direct expenses and first-tenant costs.  
   https://www.hasil.gov.my/wp-content/uploads/PR_12_2018.pdf
3. **LHDN, Introduction Individual Income Tax**: main income categories.  
   https://www.hasil.gov.my/en/individu/pengenalan-cukai-pendapatan-individu/
4. **LHDN tax-education materials, YA 2025 e-filing**: section 4 categories.  
   https://www.hasil.gov.my/media/34zl34hu/rahsia-jimat-cukai-e-filing-e-be-tahun-taksiran-2025.pdf

Teaching cases and wording are original. The legal rules, eligibility and source facts matter; the short cases do not replace the full guidance. Sources checked on 21 October 2026 for the stated YA 2025 teaching version.

## Verification completed

- JavaScript syntax checked with Node.
- State integration test: empty dispatch, no skipping, wrong answer/retry, duplicate dispatch guard, original choice retention, assisted score, Previous/Next, all 16 cases, completion, restart, steering wraparound and Home.
- Full desktop browser playthrough of all 16 questions, including one wrong first attempt and one assisted first attempt. Expected report verified: **14 independent + 1 assisted + 1 file needing a retry**, 16 delivered.
- Browser checks: Play, mouse selection, keyboard answer selection/Enter, locked answers during feedback, Continue, Previous/Next review, restart cancel/confirm, Home, instructions and stopwatch selection.
- Responsive checks in 360px and 768px browser frames: no horizontal overflow; phone answer docks at least 74px high in the checked case. Long dividend choices also checked at phone width.

Actual hardware touch behaviour and browser-specific printing should still be checked on the classroom devices. No claim of universal device or screen-reader certification is made.

## Classroom manual checklist

- [ ] Extract ZIP; open index.html directly; verify styling and Play.
- [ ] Select a dock, then Dispatch. Confirm feedback stays until Continue.
- [ ] Give a wrong answer, try repeated keys/clicks, then retry correctly. Confirm no independent point is restored.
- [ ] Use the Rule card before a first answer; confirm an assisted first attempt in the report.
- [ ] Test Previous and Next. Check the original response remains recorded and review cannot award points.
- [ ] Complete all questions, including the final mixed-income case. Open the learning-log explanations.
- [ ] Use Play again, Restart cancel/confirm, Home and How to play.
- [ ] Select Untimed; leave a question open. It must not expire. Select the practice stopwatch and check that feedback pauses it.
- [ ] Use keyboard-only controls: Tab, Shift+Tab, Enter/Space, arrow keys, A/D and 1–4.
- [ ] On a real phone, test portrait and landscape, scrolling, taps, long choices and the final case. No sideways scrolling should be required.
- [ ] Test sound on/off. Gameplay must still work if audio is blocked or unsupported.
- [ ] Try Print report on the classroom browser and check the expanded explanations.
- [ ] Open the published GitHub Pages project URL; confirm CSS/JS load from relative paths.
