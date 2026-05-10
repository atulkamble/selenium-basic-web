# selenium-basic-web

A beginner-friendly Python project for learning web browser automation with [Selenium](https://www.selenium.dev/).

---

## Project Structure

| File | Description |
|------|-------------|
| `browser.py` | Minimal script — opens the Selenium website and quits |
| `selenium-dev.py` | Intermediate script — navigates to the Selenium docs, verifies page titles, and clicks a link |
| `selenium.md` | Reference guide covering Selenium concepts, locators, waits, and practice tasks |
| `README.md` | This file |

---

## Prerequisites

- Python 3.x
- Google Chrome browser
- Matching [ChromeDriver](https://chromedriver.chromium.org/downloads) in your `PATH` (or the same folder as the scripts)

---

## Installation

```bash
pip install selenium
```

---

## Usage

### Open the Selenium website

```bash
python browser.py
```

Opens `https://selenium.dev/` in Chrome and then closes the browser.

### Navigate and interact with the docs

```bash
python selenium-dev.py
```

1. Opens `https://selenium.dev/documentation`
2. Asserts that `"Selenium"` is in the page title
3. Clicks the **WebDriver** documentation link
4. Asserts that `"WebDriver"` is in the new page title
5. Closes the browser

---

## Key Concepts (from `selenium.md`)

| Topic | Summary |
|-------|---------|
| **Locators** | `By.ID`, `By.NAME`, `By.XPATH`, `By.CSS_SELECTOR`, `By.LINK_TEXT` |
| **Interactions** | `send_keys()`, `click()`, `submit()` |
| **Waits** | Implicit (`implicitly_wait`) and Explicit (`WebDriverWait`) |
| **Page info** | `driver.title`, `driver.current_url` |
| **Widgets** | Alerts (`switch_to.alert`), Dropdowns (`Select`) |

---

## Practice Tasks

See [`selenium.md`](selenium.md) for five hands-on exercises covering Google search, form login, dropdowns, JavaScript alerts, and page metadata.

---

## Notes

- Selenium automates **real browsers** and requires a matching browser driver.
- Prefer **explicit waits** over `time.sleep()` for reliable automation.
- Selenium is commonly used alongside **pytest** or **unittest** in CI pipelines.
- Selenium is **not** a performance/load testing tool.
