# AllTrails QA Final Project - Manual Testing
![QA Status](https://img.shields.io/badge/QA%20Process-Ready-brightgreen?style=flat-square)
![Testing Type](https://img.shields.io/badge/Testing-Manual-blue?style=flat-square)
![Browser](https://img.shields.io/badge/Cross--Browser-Validated-lightgrey?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Web-orange?style=flat-square)
![Documentation](https://img.shields.io/badge/Docs-STP%20|%20STD%20|%20STR-yellow?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-lightgreen?style=flat-square)


**Quick links:**  
[STP](./docs/STP.md) · [STD](./docs/STD.md) · [STR](./docs/STR.md) · [Screenshots](./screenshots/) · [Live project](https://lahavmauda.github.io/alltrails-final-project/)

## Test coverage overview

**Legend:** ✅ passed · 🟡 in progress · ❌ open · 🔁 to regress · 🧪 exploratory

| Area          | Scenarios covered                                   | Status | Notes |
|---------------|------------------------------------------------------|--------|-------|
| Login         | valid, invalid, empty, edge length, lockout timer    | ✅     | edge cases verified with screenshots |
| Search        | keyword, filters, empty query, no results            | ✅     | verified on desktop and mobile |
| Navigation    | header, footer, category links, back-forward flows   | ✅     | cross page linking checked |
| Account       | profile view, edit profile, validation messages      | 🟡    | edit form validations in progress |
| Error states  | 404 page, network fail simulation                    | 🧪    | exploratory notes in STR |

**Traceability:**
- Design → [STD](./docs/STD.md)
- Plan → [STP](./docs/STP.md)
- Execution and defects → [STR](./docs/STR.md) and [Issues](../../issues?q=is%3Aissue+label%3Abug)

**Next planned checks:**
- 🔁 mini regression after Account fixes
- 🧪 exploratory on slow networks and small viewports


![Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)
![Process](https://img.shields.io/badge/QA%20Process-Ready-blue?style=flat-square)
![Manual](https://img.shields.io/badge/Manual-Verified-green?style=flat-square)
![Cross Browser](https://img.shields.io/badge/Cross%20Browser-Checked-lightgrey?style=flat-square)
![Docs](https://img.shields.io/badge/Docs-STP%20|%20STD%20|%20STR-orange?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-black?style=flat-square)
![Pages](https://img.shields.io/badge/Live-GitHub%20Pages-brightgreen?style=flat-square)

## 🌟 Overview
Hands-on manual QA project for a live web app.  
Focus on test planning, test case design, sanity and regression runs, clear defect reporting, and final summary.

**Live demo:** https://lahavmauda.github.io/alltrails-final-project/

---

## 🧭 Scope and Goals
- Validate core user flows and critical paths
- Cover sanity and selected regression areas
- Document tests so anyone can reproduce results
- Report defects with evidence and clear expected vs actual

---

## 🗂 Project Structure
- `index.html` - project landing and samples
- `README.md` - project description and quick navigation
- `AllTrails QA Final Project – Manual Testing.pdf` - full STR export (encoded link below)

> Full STR PDF:  
> [Open report](AllTrails%20QA%20Final%20Project%20%E2%80%93%20Manual%20Testing.pdf)

---

## 📝 STP - Test Plan (high level)
- **Risks and assumptions:** cross browser differences, network latency, missing validations
- **Test levels:** sanity first, then targeted regression
- **Environments:** desktop web and mobile web views
- **Entry criteria:** stable build, defined user stories, basic data ready
- **Exit criteria:** sanity pass, no open critical defects, known issues documented

---

## 🧪 STD - Test Design (samples)
| ID  | Area              | Title                               | Type        |
|-----|-------------------|-------------------------------------|-------------|
| TC01| Auth              | Login with valid user               | Sanity      |
| TC02| Auth              | Login with invalid password         | Negative    |
| TC03| Search            | Search by keyword and open result   | Sanity      |
| TC04| Navigation        | Header links respond and track      | Regression  |

> The full STD is included inside the STR report and the live page.

---

## 📊 STR - Test Summary
- **Sanity:** passed with minor UI observations
- **Regression:** selected flows passed
- **Defects filed:** see Issues tab for labeled items
- **Recommendations:** enforce input validation, unify error messages, add empty state hints

---

## 🐞 Defect Reporting
Issues follow a standard template: environment, steps to reproduce, expected vs actual, evidence, scope.  
Open a new bug: **Issues → New issue → Bug report**.

---

## 🔍 Test Execution Notes
- Verified on common resolutions for desktop and mobile views
- Checked orientation change - portrait and landscape
- No console errors on critical pages during sanity run

---

## 🔗 Quick Links
- Live project: https://lahavmauda.github.io/alltrails-final-project/  
- Full STR PDF: [AllTrails QA Final Project – Manual Testing](AllTrails%20QA%20Final%20Project%20%E2%80%93%20Manual%20Testing.pdf)  
- Issue template: [bug_report.md](.github/ISSUE_TEMPLATE/bug_report.md)  
- PR template: [pull_request_template.md](pull_request_template.md)

---

## 📚 Tech and Tools
- Test docs: STP, STD, STR
- Tracking: spreadsheets and structured tables
- Version control: Git and GitHub
- Communication style: clear, factual, user focused

---

## 🧩 Notes
- This repository is manual testing focused.  
- Automation learning path is separate and uses Python and Playwright.

---

## 🐞 Bug Evidence

Below are selected **real functional issues** discovered during testing.
These findings show the tester’s analytical ability and real QA mindset.

| Screenshot | Description | Result |
|-------------|--------------|---------|
| ![Invalid characters](./screenshots/No_error_message_for_invalid_characters.png) | No error message for invalid characters in First and Last Name fields | ❌ Bug |
| ![Jerusalem French](./screenshots/Searching%20Ramot%20Menashe%20without%20Internet.png) | Incorrect result when typing Jerusalem in French | ⚠️ Defect |
| ![Jerusalem Italian](./screenshots/store_location_not_prominent_Italian.png) | Incorrect result when typing Jerusalem in Italian | ⚠️ Defect |
| ![Store location](./screenshots/The%20store's%20location%20is%20not%20prominent.png) | The store’s location is not prominent on the map | ❌ Bug |
| ![Camping and Skiing](./screenshots/No%20results%20when%20selecting%20Camping%20and%20Skiing.png) | Missing results when selecting “Camping and Skiing” | ❌ Bug |

---

## 💡 UX & Usability Findings

Below are **non-functional issues** found during exploratory testing,  
focused on user experience and accessibility aspects.

| Screenshot | Description | Type |
|-------------|--------------|------|
| ![Social](./screenshots/No%20Sharing%20on%20Social%20Media.png) | No sharing option for social media | 💡 UX Suggestion |
| ![Offline](./screenshots/No%20results%20without%20internet.png) | App behavior while offline (no informative message) | ⚠️ Needs improvement |

---

> 🧠 These screenshots reflect **real manual testing** findings and support issues documented in the STR report.

---

## 🧠 QA Insights & Recommendations

### 🔍 Key Findings
- Multiple **functional issues** found in multilingual search and input validation.  
- **Offline handling** and **social sharing** lack proper user feedback.  
- **Map visibility** can be improved to highlight important locations.  
- UI/UX inconsistencies detected between desktop and mobile views.

### 🧭 Recommendations
| Priority | Area | Recommendation | Type |
|-----------|------|----------------|------|
| 🔴 High | Input Validation | Add proper error handling for invalid name characters | Functional |
| 🟠 Medium | Search Logic | Standardize language-based results (e.g., Italian, French) | Functional |
| 🟡 Medium | Map Visibility | Make store or location markers more noticeable | UI |
| 🟢 Low | Offline Mode | Display clear “No Internet” feedback message | UX |
| 🟢 Low | Social Sharing | Integrate share options for user content | UX |

### 💬 Summary
This testing cycle reflects strong coverage of **functional**, **usability**, and **exploratory** testing.  
It highlights improvement opportunities for user experience consistency and communication clarity.  
Further regression testing is recommended after fixes are implemented.
---
---

## 📈 QA Test Summary

Visual summary of the manual test execution results.  
Reflects the ratio between successful, defective, and UX-related cases during the AllTrails QA process.

<p align="center">
  <img src="./screenshots/QA_Overview.png" alt="QA Summary Chart" width="600"/>
</p>

**Interpretation:**
- ✅ 69% of test cases passed successfully  
- ❌ 19% identified as functional bugs  
- 💡 12% noted as UX improvements or usability findings

---

### 🧠 Footer
Built by Lahav Mauda – Manual QA transitioning to Automation  
Currently studying at Automation College Tel Aviv with Gal Matalon.
