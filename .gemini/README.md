# Gemini CLI Commands

This document provides a detailed overview of the available custom commands for the Gemini CLI. Each command is designed to automate specific development tasks, from generating changelogs to scaffolding new components.

---

## Development Related

### `changelog`

**Description:** Drafts a `CHANGELOG.md` entry by categorizing git commits between two tags.

**How to use:**
```bash
@changelog <from_tag> <to_tag>
```
-   `<from_tag>`: The older git tag to start the comparison from.
-   `<to_tag>`: The newer git tag to end the comparison at.

If no tags are provided, the command will automatically use the two most recent tags.

**Example:**
```bash
@changelog v1.0.0 v1.1.0
```

---

### `create_readme`

**Description:** Analyzes a project to generate a comprehensive, well-structured `README.md` file with detailed sections.

**How to use:**
```bash
@create_readme
```
This command takes no arguments. It analyzes the project directory it is run in.

**Example:**
```bash
@create_readme
```

---

### `extract_design`

**Description:** Extracts design system information from an image.

**How to use:**
```bash
@extract_design <image_path>
```
-   `<image_path>`: The path to the image file to analyze.

**Example:**
```bash
@extract_design ./design_mockup.png
```

---

### `iterate_design`

**Description:** Creates UI iterations based on a design system.

**How to use:**
```bash
@iterate_design <task_description>
```
-   `<task_description>`: A description of the UI to build.

**Example:**
```bash
@iterate_design "Create a login form with a username and password field, and a submit button."
```

---

### `outdated_package`

**Description:** Checks for outdated dependencies and fetches changelogs for major updates.

**How to use:**
```bash
@outdated_package
```
This command takes no arguments. It checks the dependencies of the project it is run in.

**Example:**
```bash
@outdated_package
```

---

### `parallel_tasks`

**Description:** Sets up multiple git worktrees and launches parallel sub-agents for concurrent feature development and isolated testing.

**How to use:**
```bash
@parallel_tasks <task_description>
```
-   `<task_description>`: A description of the development task to be worked on in parallel.

**Example:**
```bash
@parallel_tasks "Implement user authentication using JWT"
```

---

### `scaffold`

**Description:** Scaffolds boilerplate files for various frameworks (React, Spring Boot, Flutter).

**How to use:**
```bash
@scaffold <type> <name>
```
-   `<type>`: The type of component to scaffold. Supported types: `react-component`, `springboot-service`, `flutter-bloc`.
-   `<name>`: The name of the component/service.

**Example:**
```bash
@scaffold react-component UserProfile
```

---

### `ui_ux_expert`

**Description:** A UI/UX expert agent that can help with website design from scratch.

**How to use:**
To activate the agent:
```bash
*agent Jhon
```
To start the design process:
```bash
*agent Jhon, begin website design
```
You can also start specific phases:
```bash
*agent Jhon, start discovery & research
*agent Jhon, start strategy & definition
*agent Jhon, start structure & interaction design
*agent Jhon, start prototyping & testing
*agent Jhon, start visual design & refinement
*agent Jhon, start implementation & continuous improvement
```
This command is interactive and will guide you through the process.

---

## Productivity

### `clip`

**Description:** Clips a web article, converts it to clean Markdown, and saves it locally.

**How to use:**
```bash
@clip <URL>
```
-   `<URL>`: The full URL of the article you want to clip.

**Example:**
```bash
@clip https://www.freecodecamp.org/news/the-ultimate-guide-to-becoming-a-great-backend-engineer/
```

---

### `eod`

**Description:** Generates an End-of-Day summary from today's git commits and a `todo.md` file.

**How to use:**
```bash
@eod
```
This command takes no arguments. It uses your git configuration and looks for a `todo.md` file in your `~/Documents` directory.

**Example:**
```bash
@eod
```

---

### `prep`

**Description:** Summarizes a document/URL and generates meeting prep notes.

**How to use:**
```bash
@prep <URL_or_file_path>
```
-   `<URL_or_file_path>`: The URL or local file path of the document to analyze.

**Example:**
```bash
@prep https://docs.google.com/document/d/12345...
```
or
```bash
@prep ./meeting_agenda.md
```

---

## General

### `outline`

**Description:** Extracts and displays all headings from a Markdown file in a structured, indented outline.

**How to use:**
```bash
@outline <file_path>
```
-   `<file_path>`: The path to the Markdown file to analyze.

**Example:**
```bash
@outline ./docs/guide.md
```

---

### `scratchpad`

**Description:** Appends a timestamped note to a central `scratchpad.txt` file.

**How to use:**
```bash
@scratchpad <note>
```
-   `<note>`: The text you want to save to your scratchpad.

**Example:**
```bash
@scratchpad Remember to buy milk on the way home.
```
