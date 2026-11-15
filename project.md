# Studio Project 1, Milestone 1: Project Notebook

> **How to use this notebook.** Replace every line that says `YOUR ANSWER HERE` (and delete the grey instruction lines that start with `>`) with your own work. Keep the headings. Commit after each part. Do not leave any instruction text in your final version.

**Student name:** Matt Pheaton
**GitHub username:** matt12005

> This notebook is my own individual work. I did my own research, sketches, writing and code.

---

## Part 0: Project Snapshot

**Project name:** Smart mines dashboard
**Tagline (10 words or fewer):** Making Mines More Transparent
**Repository link:** https://github.com/Matt120056/Smart-Mine-Operations-Dashboard.

**Idea check** (write yes or no, and one short reason for each):

| # | Question | Yes or no, and why |
|---|---|---|
| 1 | A real group of people has this problem, and I can talk to some of them | yes I can find some people at R&D to talk to |
| 2 | Users do something in the app (not just read) | yes they interact with / Monitor the system |
| 3 | The app needs to remember things | yes it needs to rememeber data to create averages |
| 4 | I can describe the first version in one sentence | A main skeleton of the dashboard with sensor cards defined |
| 5 | I can picture at least three screens | indeed i can: employee location, air quality, moisture/water removal systems |
| 6 | I alone could build a simple first version | I will do my best |

**My one-sentence description of the first version:** A basic skeleton of the dashboard and defined spaces for the proper sensors that will be

---

## Part 1: Define the Problem

### 1.1 Problem statement
> Describe a problem, not a solution. Do not mention an app, a website or a feature. Use: "[Who] struggles to [do what] because [obstacle], which leads to [consequence]." Then expand to three to five sentences.

The problem That I see is the massive amount of data that is being collected and the man power that is always at risk
on a mine site. Even though systems are safer today then they were 20 years ago I still want to work to find a better more condensed way to filter and organize the data. 

### 1.2 Evidence from real people
> Two short conversations. Record a role (not a full name), two exact quotes each, and one surprise. Ask permission before quoting. Do not invent quotes.

**Conversation A**

- **Who (role only):** Mining engineering student
- **Quote 1:** "I want something not complex but that shows me only what I need to see "
- **Quote 2:** "Being prepared is the best way to feel comfortable"
- **What surprised me:** They want something useful but not flashy, simple but effective

**Conversation B**

- **Who (role only):** YOUR ANSWER HERE
- **Quote 1:** "YOUR ANSWER HERE"
- **Quote 2:** "YOUR ANSWER HERE"
- **What surprised me:** YOUR ANSWER HERE

I never got to a seccond conversation and I dont want to make one up.

**Revised problem statement** (re-read 1.1 after your conversations, then write the revised version, or write "no change" and say why):

YOUR ANSWER HERE

### 1.3 Persona
> A made-up person based on what you heard. Their frustrations should echo your quotes.

- **Name, age or life stage, role:** Underground Miner
- **Context (when and where the problem happens):** Knowledge of everything going on
- **Three goals:** 1) Make something good 2) simple to use 3) Easy to edit and maintain 
- **Three frustrations:** 1) getting all info needed 2) learning the mining systems 3) making a mini mine on my desk
- **Technology comfort and devices:** Sensors, My mini pcs and my endless hardware I have aquired
- **A quote that sums them up:** "Pretty cool and intense at times"

### 1.4 What already exists
> Two or three alternatives, including "doing it by hand" if that is what people really do.

| Alternative | What it does well | Where it falls short for my persona |
|---|---|---|
| Existing mine monitoring or control systems | Can collect and display operational information from connected equipment and sensors. | may be specialized or distributed across different systems. The dashboard should not assume it can replace these systems |
| Paper notes, shift logs, or verbal handovers | Familiar and useful for recording observations and passing information between shifts. | Information can be difficult to search, compare, or summarize, especially when records are spread across multiple documents. like they usually are in mining  |

### 1.5 Success criteria
> Three statements you could actually check.

1. A first-time user can identify the purpose of the Home page and find the Sensors page within 10 seconds
2. The Sensors page displays at least three clearly labelled sample sensor categories or readings
3. The Home and Sensors pages remain usable at a 375-pixel mobile viewport and a 1280-pixel desktop viewport without horizontal page scrolling

### 1.6 Abstract (150 to 250 words)
> Three short parts: the problem and who has it, what you are building, and why it matters.

# Smart Mine Operations Dashboard – Project Abstract - Matt Pheaton | A00305272

The Smart Mine Operations Dashboard is a web-based monitoring platform designed to help mine operators, supervisors, and maintenance personnel view important mining and environmental information in one centralized location.

Mining environments present several operational and safety challenges. Equipment conditions, environmental changes, and potential hazards must be monitored regularly. When information is spread across multiple devices or checked manually, important changes may go unnoticed, potentially resulting in equipment failures, unsafe working conditions, and operational delays.

The proposed system aims to address these challenges by connecting monitoring hardware, sensors, and a controller to a web-based dashboard. The platform will display sensor readings, equipment conditions, device connectivity, and important operational information. Monitoring categories may include temperature, vibration, air quality, gas levels, and equipment activity.

The dashboard will also feature a notification and alert system that identifies readings exceeding predefined safety thresholds. Alerts will help operators recognize potential hazards and respond more efficiently. The interface will be organized into dedicated sections for the main dashboard, equipment monitoring, environmental sensors, safety alerts, and personnel information.

The intended users include mine operators, supervisors, and maintenance teams who require a clear overview of underground operations. The project demonstrates how Internet of Things (IoT) hardware, sensor technology, data management, and web development can be integrated into a centralized monitoring solution.

The overall objective is to develop a functional prototype that demonstrates how connected monitoring technologies can support improved operational awareness, equipment monitoring, and workplace safety in mining environments.

**Word count:** 249 haha just under

---

## Part 2: Decide What to Build

### 2.1 Scope (MoSCoW)
> At most five Musts, each with a "because" tied to a success criterion. At least two Won'ts. Ten to fourteen features in total.

| Feature | Group (Must, Should, Could, Won't) | Because |
|---|---|---|
| Home page with a clear operational overview | must | gives users a good starting point |
| Sensors page with organized sensor cards | Must | sensor info in a consistent layout |
| Navigation between Home and Sensors | must | quick nav between pages for ease |
| Clear labels showing sample | must | so I can see what I have setup as demo or actual physical sensors |
| Equipment status page | Should | Adds useful operational context |
| Environment page with air-quality and moisture sections | Should | Organizes important environmental categories for a later development stage |
| Safety alerts page | Should | Gives users a dedicated place to review threshold warnings in a later stage. |
| Employee/location monitoring page | SHould | insure the safety of the employees underground or in hazardis areas |
| Automated notifications to users | Could | Could improve awareness later, but requires back-end logic and decisions about alert delivery. |
| Automated control of mine equipment | Wont | out of scope of the applications itself |

### 2.2 Main user flow
> Five to eight numbered steps, each naming the screen where it happens.

1. Home: The user opens the dashboard and sees a brief overview of the monitoring areas.
2. Sensors: The user selects Sensors from the navigation.
3. Sensors: The user reviews the available sensor categories, such as air quality and moisture/water-removal monitoring.
4. Sensors: The user selects or reviews a sensor card to understand its displayed value, unit, and status.
5. Home: The user returns to the overview to continue reviewing the dashboard.

### 2.3 Data sketch
> Two to four things your app remembers, with three to five details each. No SQL. Then one sentence for each relationship.

| Thing | Details it remembers |
|---|---|
| Sensor | identifier, sensor category, location/area, measurement unit, connection status |
| Alert | Alert identifier, related sensor or equipment, alert message, severity, date and time, acknowledgement status |

**Relationships:** A sensor reading can be associated with an alert when a configured threshold is exceeded. Equipment can be associated with a work area and may have related monitoring sensors or alerts. I will define the relationships in the data base in the next milestone.

### 2.4 Page list
> Every page the finished project might have (at least five). Mark the two you build in this milestone.

| Page | Purpose | Built in Milestone 1? |
|---|---|---|
| Home | Gives users a clear overview and links to the main monitoring areas. | Yes |
| Sensors | Displays organized sensor categories, sample readings, units, timestamps, and status. | Yes |
| Equipment | Shows equipment details and operating status. | No |
| Environment | Organizes air-quality, moisture, and water-removal information. | No |
|Personnel / Location | Potentially displays approved personnel or location information, subject to privacy and project-scope review. | No |

### 2.5 GitHub issues
> Paste the links to your five issues.

1. Build the home page and the core page (HTML): https://github.com/Matt120056/Smart-Mine-Operations-Dashboard./issues/1
2. Style the site: palette, responsive layout and components: https://github.com/Matt120056/Smart-Mine-Operations-Dashboard./issues/2
3. Feature (Must): https://github.com/Matt120056/Smart-Mine-Operations-Dashboard./issues/3
4. Feature (Must): https://github.com/Matt120056/Smart-Mine-Operations-Dashboard./issues/4
5. Feature (Must): https://github.com/Matt120056/Smart-Mine-Operations-Dashboard./issues/5

### 2.6 Abstract check
> Re-read your abstract from 1.6 against your Must-haves. Edit it if it no longer matches (keep it 150 to 250 words), then say what you changed.

- **What I changed (or why nothing):** I just re made the absract recently so I have nothing new as of yet to add or delete.

---

## Part 3: Storyboard

> Four to six panels. The first shows the problem, the last shows it solved, and the same persona appears throughout. Save images in `design/storyboard/` and embed them below with `![description](design/storyboard/panel-1.jpg)`.

| Panel | Scene (where, who) | What happens | What they think or feel | Screen shown |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |

These are in my storyboard.txt via this link: https://github.com/Matt120056/Smart-Mine-Operations-Dashboard./blob/main/storyboard.txt

---

## Part 4: Site Map and Wireframes

### 4.1 Site map
> A Mermaid diagram (GitHub draws it). Replace the example.

```mermaid
flowchart LR
    Home --> PageB
    Home --> PageC
```

### 4.2 Wireframes
> Four images: Home and core page, each on a phone-width and a desktop-width screen. Real words, no colour. Embed them.

**Home, phone:** https://github.com/Matt120056/Smart-Mine-Operations-Dashboard./blob/main/dashboard/screenshots/Screenshot%202026-11-15%20at%205.59.43%E2%80%AFPM.png
**Home, desktop:**  https://github.com/Matt120056/Smart-Mine-Operations-Dashboard./blob/main/dashboard/screenshots/Screenshot%202026-11-15%20at%205.56.01%E2%80%AFPM.png
**Core page, phone:** https://github.com/Matt120056/Smart-Mine-Operations-Dashboard./blob/main/dashboard/screenshots/Screenshot%202026-11-15%20at%206.00.43%E2%80%AFPM.png
**Core page, desktop:** https://github.com/Matt120056/Smart-Mine-Operations-Dashboard./blob/main/dashboard/screenshots/Screenshot%202026-11-15%20at%206.00.51%E2%80%AFPM.png

### 4.3 Annotations
> For each region of each page, name the HTML element and say why.

**Home page**

| Region | HTML element | Why this element |
|---|---|---|
| Top bar | <header> | Site-wide banner that groups the title and system status together |
| Sidebar menu | <aside> with <nav> and <a> links | Navigation is a list of links to other pages, so anchors inside a nav landmark |
| Live sensor data | <ul class="simple-list"> with <li> | A short list of items, so an unordered list is the right semantic element |

**Core page**

| Region | HTML element | Why this element |
|---|---|---|
| Top bar | <header> | Same shared banner as Home |
| Sidebar menu | <aside> with <nav> and <a> | Same shared navigation; "Sensors" gets class="active" |
| Page title | <h2> and <p class="subtitle"> | Introduces the page; the page also uses one <h1> in the top bar |
 
### 4.4 Five-second test
- **Who I tested (role only):** mining student
- **What they said the page is for, and what they would do first:** if it was at work they said they would check warnings first.
- **What I changed because of it (or why I changed nothing):** at first the page was janky and hard to read so I made it easier and nicer to look at.

---

## Part 5: Design Decisions

### 5.1 Mood
- **Three words:** Industrial, easy, clear
- **Why they fit my persona:** A mine operator needs information fast and without decoration as they would. Dark blue sets a nice industrial setting; the light grey background keeps the page calm so the coloured status tags (green/orange) stand out. 

### 5.2 Palette

| Role | Variable | Hex |
|---|---|---|
| Page background | `--color-bg` | #f2f5f9 |
| Card and header surface | `--color-surface` | #ffffff |
| Body text | `--color-text` | #1f2d3d |
| Headings and links | `--color-primary` | #1769aa |
| Buttons and highlights | `--color-accent` | #1f2d3d |
| Button hover | `--color-accent-dark` | #16222e |
| Borders | `--color-border` | #dde5ee |
| Secondary text | `--color-muted` | #6b7b8c |

### 5.3 Contrast table
> At least six real pairs. Every normal-text pair must be 4.5 : 1 or better (3 : 1 for large text). Use https://webaim.org/resources/contrastchecker/

| Text colour | On | What it is | Ratio | Passes? |
|---|---|---|---|---|
| #1f2d3d | #f2f5f9 | Body text on the page | 12.6 : 1 | yes |
| #4a5c70 | #ffffff | Heading on a card | 7.6 : 1 | yes |
| #ffffff | #1f2d3d | Button text | 14.3 : 1 | yes |
| #1f2d3d | #ffffff | Button text on hover | 14.3 : 1 | yes |
| #6b7b8c | #ffffff | Muted text on a card | 4.9 : 1 | yes |
| | | | | |

### 5.4 Type and spacing
- **Heading font stack:** Arial, Helvetica, sans-serif
- **Body font stack:** Arial, Helvetica, sans-serif
- **Type scale (`h1`, `h2`, `h3`, body, in rem):** h1 1.25rem, h2 1.375rem, h3 0.875rem, body 0.875rem (base 16px)
- **Spacing unit:** 5px
- **Corner radius:** 8px on the cards, 6px on links and tags

### 5.5 Pace check
> Halfway through your time, run `git log --format='%ad' --date=short | sort -u | wc -l`. You need commits on at least four different days.

```text
(base) ➜  aa1-A00305272 git:(main) git log --format='%ad' --date=short | sort -u | wc -l
       6
```

---

## Part 6: Build the Structure (HTML)

### 6.1 Build table
> Match the regions from Part 4 to what you built.

| Wireframe region | Element in my HTML | File |
|---|---|---|
| | | |
| | | |
| | | |

### 6.2 Checks
- [ ] Both pages have exactly one `h1` and headings in order
- [ ] Both pages have the viewport meta tag and a unique `<title>`
- [ ] The `nav` links to both pages and marks the current one with `class="active"`
- [ ] There is a list of repeated items, each an `article`
- [ ] The form has a `label`, `id` and `name` for every control
- [ ] Informative images have real alt text and decorative ones use `alt=""`
- [ ] No lorem ipsum anywhere
- [ ] I used at least one absolute, one relative and one same-page link

### 6.3 Validator results
- **Home page:** screenshot `screenshots/home-validation.png`
- **Core page:** screenshot `screenshots/core-validation.png`

**Errors I met and fixed (at least one):** YOUR ANSWER HERE

---

## Part 7: Style It (CSS)

### 7.1 Match table
> Compare the finished pages with your wireframes.

| Page | What matches | What changed, and why |
|---|---|---|
| Home | | |
| Core page | | |

### 7.2 Checks
- [ ] Every colour, font, spacing and radius comes from `:root`
- [ ] No `!important`, no inline `style`
- [ ] Mobile first, with at least two `min-width` media queries
- [ ] Flexbox is used for the header and nav, and Grid for the cards
- [ ] `.btn` and `.card` (or my own reusable classes) are used everywhere
- [ ] There is no sideways page scroll at 375px
- [ ] The page still looks decent with Google Fonts blocked

### 7.3 Contrast re-check
**Pairs I re-tested on the built page, and any I had to change:** YOUR ANSWER HERE

### 7.4 CSS validator
**What the W3C CSS Validator said (and whether any warning matters):** YOUR ANSWER HERE

### 7.5 Screenshots
> Embed them: `screenshots/home-375.png`, `screenshots/home-1280.png`, `screenshots/core-375.png`, `screenshots/core-1280.png`.

YOUR ANSWER HERE

---

## Part 8: Git and GitHub

**Repository:** https://github.com/...
**Issue #1 (closed):** https://github.com/...
**Issue #2 (closed):** https://github.com/...
**Merged Pull Request for HTML:** https://github.com/...
**Merged Pull Request for CSS:** https://github.com/...
**Release v0.1.0:** https://github.com/...

```text
(git log --oneline | wc -l)
```
```text
(git log --format='%ad' --date=short | sort -u | wc -l)
```
```text
(git branch -a)
```
```text
(git log --oneline --graph --all | head -20)
```

---

## Part 9: Reflection

> Two to four sentences each, about your own project.

1. **From idea to problem:** YOUR ANSWER HERE
2. **Evidence:** YOUR ANSWER HERE
3. **The hardest decision:** YOUR ANSWER HERE
4. **Design to code:** YOUR ANSWER HERE
5. **Risks for the next milestones:** YOUR ANSWER HERE
6. **Tools (including any AI tool, and what I did myself):** YOUR ANSWER HERE

### Self-assessment

| Area | Points | My score | One line of justification |
|---|---|---|---|
| Problem definition and evidence | 15 | | |
| Scope and data | 10 | | |
| Storyboard | 10 | | |
| Wireframes and site map | 10 | | |
| Design decisions | 5 | | |
| HTML | 15 | | |
| CSS and responsiveness | 15 | | |
| Git and GitHub | 15 | | |
| Reflection and completeness | 5 | | |

## Bonus (optional)

- **Usability test (+3):** who I tested (roles), what happened, what I changed: YOUR ANSWER HERE
- **Live site (+2):** https://...s# Studio Project 1, Milestone 1: Project Notebook
