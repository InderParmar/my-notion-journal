# My Notion Journal

https://github.com/user-attachments/assets/d355c097-4fbc-4f5e-bbed-9afccf30e0f3

Automate the creation of a daily journal in [Notion](https://notion.so).

### ⚠️ Note

This project is a personal one that I'm refining in my free time. That means it may still have bugs and isn't perfect, so if you decide to use it, please keep in mind that some tweaks might be necessary. Feel free to report any bugs or make suggestions :)

## Features

- Creates a "Daily Journal" page in Notion every day.
- Migrates any unchecked tasks from the previous day's page to the new daily page.
- Runs daily via GitHub Actions for continuous automation.

---

## Requirements

- **Node.js** (recommended version 14+)
- A **Notion Integration** with access to your workspace and the relevant parent page ID.

---

## Setup

1. **Clone this repository:**

   ```bash
   git clone <repository_url>
   cd <repository_directory>
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Create a Notion Integration and Get Your API Key:**

   - Go to https://www.notion.so/my-integrations and create a new integration.
   - Save the **API Key** generated by Notion.

4. **Get the Parent Page ID:**

   - Open the Notion page you want to use as the parent in your browser.
   - Copy the ID from the URL after `notion.so/`, which should look like `xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx`.

      **p.s** If you created the integration as `internal`, make sure to connect it to the page by opening the three-dot menu at the top right → connections → click the integration name to connect.
  
5. **Create a `.env` File in the Root Directory:**

   Copy the `.env.example` file and rename it to `.env`. Update the file with your API key and Parent Page ID.

   ```plaintext
   NOTION_API_KEY=placeholder
   PARENT_PAGE_ID=placeholder
   ```

## Running the Automation

To run this script locally and create the daily page, use:

```bash
node index.js
```

If you want to set up this automation to run daily using GitHub Actions, follow the steps below.

## GitHub Actions Setup

**todo**
