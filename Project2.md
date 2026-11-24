# Studio Project 1, Milestone 2: Project Notebook

> **How to use this notebook.** Replace every line that says `YOUR ANSWER HERE` (and delete the grey instruction lines that start with `>`) with your own work. Keep the headings. Commit after each part. Do not leave any instruction text in your final version. Save this file in the root of your repository as `notebook-m2.md`.

**Student name:** Matt Pheaton
**GitHub username:** Matt120056
**Project name:** Smart mining dashboard

> This notebook is my own individual work. I wrote my own plan, data, code, tests and reflections.

---

## Part 0: Set Up and Adapt Your Issues

**Repository link:** https://github.com/Matt120056/Smart-Mine-Operations-Dashboard.

```text
(git log --oneline | wc -l   and   git tag   from step 0.1)

(base) ➜  aa1-A00305272 git:(main) git log --oneline | wc -l
      40

Git tag
V1.0.0
v0.1.0
```

### 0.3 Live Server

- **The address bar of my page when opened with Live Server:** http://127.0.0.1:5500/dashboard/index.html

### 0.4 My three features

> Each of your Issues #3, #4 and #5 becomes one browser-only feature: **Show** (load and display a list from `data.json`), **Find** (live search), **Add** (validated form, then mark and tally). Edit each issue on GitHub with a new, specific title. The "Done when" checklist comes at the end of Part 1.

| Issue | Feature title (as edited on GitHub) | Kind (Show, Find or Add) | Success criterion from Milestone 1 it serves |
|---|---|---|---|
| #3 | Sensor readings from data.json | Show |  |
| #4 | Search sensors by name and category | Find | |
| #5 | New sensor records using validated form | Add | |

**Did any of my Milestone 1 Must-haves need a server (log in, save forever, send email)? What did I do with it?** as of right now none were needed

---

## Part 1: Plan the Behaviour

### 1.1 Show spec

| Question | My answer |
|---|---|
| Which pages show data, and which part of the page | The Sensors page (sensors.html) displays all sensor records loaded from data.json. The Home page (index.html) displays the first three sensor records as a preview. |
| Fields of each card, in wireframe order | The fields appear in this order:

Sensor ID

Measurement Type

Location

Current Reading

Maintenance Status |
| Loading message (exact text) | Loading Sensor Information... |
| Message if the file cannot be loaded (exact text) | Could not load sensor information. Please try again. |
| Empty-list message (exact text) | Could not load sensor information (status [status code]). |
| How many cards the home page shows | The Home page displays the first three sensor records. |

### 1.2 Find spec

| Question | My answer |
|---|---|
| Fields the search looks at (at least two) | The search checks the Sensor ID and Measurement Type fields. |
| What must NOT matter (capitals, extra spaces) | Capital letters and spaces before or after the search text must not affect the results. |
| Count line, in my own words (pattern with numbers) | Showing X of Y sensors.
X represents the number of matching sensors, and Y represents the total number of sensors. |
| No-match message (exact text) | No sensors match your search. Try another sensor ID or measurement type. |
| When the filter runs (events, and once after the data arrives) | The filter runs every time the visitor types a character into the search box. It also runs again immediately after the sensor data finishes loading. |

### 1.3 Add spec

> List the fields in the same order as the form. Validate in this order and stop at the first problem. Write the exact message now, and use it exactly in the code.

| # | Field | Control type | Rule | Exact message |
|---|---|---|---|---|
| 1 | Sensor ID |  | | |
| 2 | Measurement Type | | | |
| 3 | Location | | | |
| 4 | Current Reading | | | |

- **What a good add does (list every change on the page):** Clears the previous form error message.

Creates a new sensor record with a unique ID.

Adds the new sensor to the sensor records array.

Displays the new sensor if it matches the current search.

Clears the form fields.

Moves the cursor back to the first form field.

Updates the result count.

Updates the maintenance tally.
- **The mark state (what the true/false field means, and the words for each state):** The needsMaintenance field will be a true/false value.

true = Requires Maintenance

false = Operational

Visitors can change this status using a button on each sensor card.

- **Tally line (pattern):** X of Y sensors require maintenance.

X represents the number of sensors requiring maintenance, and Y represents the total number of sensors.

### 1.4 Test plan

> At least five tests per feature, written BEFORE the code. Keep the same numbering when you run them in Part 6.

| ID | Feature | Do this | You should see |
|---|---|---|---|
| S1 | Show | open sensors page | All sensor records load from data.json. |
| S2 | Show | open the home page | Only the first three sensor records appear. |
| S3 | Show | open a page while the data is loading | Loading sensor information... appears. |
| S4 | Show | Temporarily rename data.json and reload | A friendly error message appears. |
| S5 | Show | Temporarily use an empty JSON array. | No sensor records are currently available. |
| F1 | Find | Search for an existing sensor ID. | The matching sensor appears. |
| F2 | Find | Search using capital letters. | Matching results still appear. |
| F3 | Find | Search with spaces before and after a sensor ID. | Matching results still appear. |
| F4 | Find | Search for a measurement type. | Sensors with that measurement type appear. |
| F5 | Find | Search for random text that does not exist. | No-match message appears and count shows zero. |
| A1 | Add | Submit the form with all fields empty. | The first validation error appears and no record is added. |
| A2 | Add | Enter spaces in a required text field. | Validation rejects the field. |
| A3 | Add | Enter an invalid reading. | An appropriate validation message appears. |
| A4 | Add | Submit a valid sensor record. | A new sensor card appears and the form resets. |
| A5 | Add | Mark a sensor as requiring maintenance, then mark it operational again. | The maintenance tally increases and decreases correctly. |

### 1.5 "Done when" checklists

> Three checks for each issue, copied from your test plan. Paste what you wrote on GitHub.

| Issue | "Done when" (three checks, with test ids) |
|---|---|
| #3 | 	S1: All sensor records load from data.json. S2: Home page displays only the first three sensors. S4: A friendly error appears when data.json cannot be loaded. |
| #4 | F1: Searching an existing sensor ID shows the matching sensor. F3: Searching with extra spaces still finds matching sensors. F5: Searching for something that does not exist displays the no-results message. |
| #5 | A1: Empty form submissions are rejected with a validation message. A4: A valid sensor record is added and the form resets. A5: The maintenance status can be changed and the tally updates correctly. |

---

## Part 2: The Data File

### 2.2 My data.json

> Paste the whole file. 8 to 12 items. Note which item has the tricky text and which has the long text.

```json
YOUR ANSWER HERE
```

- **Fields, and what each one holds (one line each):** YOUR ANSWER HERE
- **Which M1 data detail each field comes from:** YOUR ANSWER HERE
- **Tricky-text item (id) and long-text item (id):** YOUR ANSWER HERE
- **Which of my Milestone 1 form controls are NOT fields of an item, and why:** YOUR ANSWER HERE

### 2.3 Console proof

```text
(JSON.parse('[{"id": 1,}]')   the exact error message)
```
```text
(JSON.parse('[{"id": 1}]')   the result)
```

**What is wrong with `[{"id": 1,}]`, and why would the same mistake in `data.json` break the page?** YOUR ANSWER HERE

### 2.4 Network panel proof

- **Request method:** YOUR ANSWER HERE
- **Status code:** YOUR ANSWER HERE
- **Content-Type:** YOUR ANSWER HERE
- **Size and time:** YOUR ANSWER HERE

---

## Part 3: Show It (fetch and render)

### 3.1 My code

```js
YOUR ANSWER HERE
```

### 3.2 Home page code

```js
YOUR ANSWER HERE
```

### 3.3 Live Server or file://

- **The Console message when I opened the core page by double-clicking it (file://):** YOUR ANSWER HERE

### 3.4 Console proof

```text
(document.querySelectorAll("#item-list article").length)
```
```text
(the message I see when the path is wrong, for example "dta.json")
```
```text
(the message I see when data.json has a trailing comma)
```
```text
(the message I see when data.json is []  )
```

### 3.5 Breakpoint

- **Where I put the breakpoint (file and line):** YOUR ANSWER HERE
- **One sentence on what I saw in the Scope panel and what it told me:** YOUR ANSWER HERE

### 3.6 Explain

- **Why does `fetch()` not reject on a 404, and what do I check instead?** YOUR ANSWER HERE
- **Why are there two `await` lines (fetch and `.json()`)?** YOUR ANSWER HERE
- **What did I see on Slow 3G, and why did the page not freeze?** YOUR ANSWER HERE

```text
(git log v0.1.0..HEAD --oneline | wc -l   after the merge of feature/show-items: expect about 12)
```

---

## Part 4: Find It (live filter)

### 4.1 My code

```js
YOUR ANSWER HERE
```

### 4.2 Console proof

```text
(document.querySelector("#result-count").textContent   on load, after one search, after a nonsense search)
```
```text
(document.querySelector("#no-results").classList.contains("hidden")   for the same three moments)
```

### 4.3 Explain

- **Why does an empty search box show every item?** YOUR ANSWER HERE
- **Why do I filter the `items` array and not the cards on the page?** YOUR ANSWER HERE
- **Why is `filterItems` called again inside `loadItems`?** YOUR ANSWER HERE

```text
(git log v0.1.0..HEAD --oneline | wc -l   after the merge of feature/find-items: expect about 18)
```

### 4.4 Pace check

```text
(git log v0.1.0..HEAD --format='%ad' --date=short | sort -u | wc -l   halfway: you need at least two days now)
```

---

## Part 5: Add It (validated form, mark and tally)

### 5.1 My code

```js
YOUR ANSWER HERE
```

### 5.2 Console proof

```text
(document.querySelector("#form-message").textContent   after each refused input in tests A1 to A4)
```
```text
(document.querySelector("#item-list").textContent.trim()   after my own good add, and after the <b>Ana</b> add)
```
```text
(document.querySelector("#tally").textContent   after load, after one mark, after one unmark)
```

### 5.3 Explain

- **Why do I listen for `submit` on the form and not `click` on the button?** YOUR ANSWER HERE
- **Why does `Number("")` need a check before `Number.isInteger()`?** YOUR ANSWER HERE
- **Why must the mark state live in the `items` array and not only in a CSS class?** YOUR ANSWER HERE

```text
(git log v0.1.0..HEAD --oneline | wc -l   after the merge of feature/add-items: expect about 26)
```

---

## Part 6: Test, Break and Debug

### 6.1 Test results

> Run every test from your plan (1.4). Mark Pass or Fail. A failure that you found and fixed is a good sign.

| ID | Pass or fail | If fail: what was wrong, and the commit that fixed it |
|---|---|---|
| S1 | | |
| S2 | | |
| S3 | | |
| S4 | | |
| S5 | | |
| F1 | | |
| F2 | | |
| F3 | | |
| F4 | | |
| F5 | | |
| A1 | | |
| A2 | | |
| A3 | | |
| A4 | | |
| A5 | | |

### 6.2 Break it on purpose

| Break | What I predicted | Exact Console message (or what I saw) | Cause | Fix |
|---|---|---|---|---|
| (a) Wrong id in a `querySelector` | | | | |
| (b) No `await` before `response.json()` | | | | |
| (c) No `event.preventDefault()` in the submit handler | | | | |
| (d) No `return` after a refusal message | | | | |

### 6.3 Two requests compared

- **The `data.json` row, status and size, when the file is there:** YOUR ANSWER HERE
- **The same row when the file is renamed:** YOUR ANSWER HERE
- **What changed in the response, and why my code had to check `response.ok`:** YOUR ANSWER HERE

### 6.4 Bug log

> At least one real bug that you did not plan, found while testing. Write "none" only if you truly found none, and say how you looked.

| # | What I saw | Where I found it (file and line) | Cause | Fix |
|---|---|---|---|---|
| 1 | | | | |

### 6.5 My Milestone 1 success criteria, re-checked

| Success criterion (copy from Milestone 1) | Met? | Evidence (a number, a time, a Console line) |
|---|---|---|
| 1. | | |
| 2. | | |
| 3. | | |

### 6.6 Screen sizes

- **375px (no sideways page scroll, text and buttons readable):** YOUR ANSWER HERE
- **800px:** YOUR ANSWER HERE
- **1280px:** YOUR ANSWER HERE

---

## Part 7: Polish

### 7.1 Checks

- [ ] `#list-status`, `#latest-status`, `#result-count`, `#no-results` and `#tally` have `aria-live="polite"`, and `#form-message` has `role="alert"`
- [ ] Both pages have a `<noscript>` message, and I saw it with JavaScript turned off
- [ ] `.hidden`, `.message` and `.done` work, and use colours from `:root`
- [ ] No red messages in the Console during normal use
- [ ] No `localStorage`, no cookies, and no data from any address except my own `data.json`
- [ ] No sideways page scroll at 375px

### 7.2 Contrast re-check

| Text colour | On | What it is | Ratio | Passes? |
|---|---|---|---|---|
| | | Error message on the page | | |
| | | Error message on a card | | |
| | | Text of a marked (done) card | | |
| | | | | |

### 7.3 Code scan

```text
(the grep commands from step 7.3 of the guide: each one should print nothing)
```

### 7.4 Validators and screenshots

- **Home page (HTML):** screenshot `screenshots/m2/home-validation.png`
- **Core page (HTML):** screenshot `screenshots/m2/core-validation.png`
- **What the W3C CSS Validator said (and whether any warning matters):** YOUR ANSWER HERE

> Embed your screenshots: `screenshots/m2/home-1280.png`, `screenshots/m2/core-375.png`, `screenshots/m2/core-1280.png`, and `screenshots/m2/core-error-375.png` (a form error on show).

YOUR ANSWER HERE

---

## Part 8: Git and GitHub

**Repository:** https://github.com/...
**Issue #3 (closed):** https://github.com/...
**Issue #4 (closed):** https://github.com/...
**Issue #5 (closed):** https://github.com/...
**Merged Pull Request, Show:** https://github.com/...
**Merged Pull Request, Find:** https://github.com/...
**Merged Pull Request, Add:** https://github.com/...
**Merged Pull Request, Polish:** https://github.com/...
**Three open issues for the server milestone:** https://github.com/... , https://github.com/... , https://github.com/...
**Release v0.2.0:** https://github.com/...

```text
(git log v0.1.0..HEAD --oneline | wc -l)
```
```text
(git log v0.1.0..HEAD --format='%ad' --date=short | sort -u | wc -l)
```
```text
(git tag)
```
```text
(git branch -a)
```
```text
(git log --oneline --graph --all | head -25)
```

---

## Part 9: Reflection

> Two to four sentences each, about your own project.

1. **Async:** YOUR ANSWER HERE
2. **Data and page:** YOUR ANSWER HERE
3. **Validation:** YOUR ANSWER HERE
4. **The hardest bug:** YOUR ANSWER HERE
5. **Plan against result:** YOUR ANSWER HERE
6. **Next milestone (what changes when `data.json` becomes a server address):** YOUR ANSWER HERE
7. **Tools (including any AI tool, and what I did myself):** YOUR ANSWER HERE

### Self-assessment

| Area | Points | My score | One line of justification |
|---|---|---|---|
| Behaviour plan and data file | 10 | | |
| Show: fetch and render | 20 | | |
| Find: live filter | 15 | | |
| Add: validated form, mark and tally | 20 | | |
| Testing and debugging | 10 | | |
| Quality and accessibility | 5 | | |
| Git and GitHub | 15 | | |
| Reflection and completeness | 5 | | |

## Bonus (optional)

- **Level up (+3):** which one, the code, and a Console proof: YOUR ANSWER HERE
- **Live site (+2):** https://...