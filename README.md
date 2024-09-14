# Gmail-Spam-Cleaner---Sir-Spamabot🧹🤖

![Spam Cleaner Bot](https://github.com/RNBBarrett/Gmail-Spam-Cleaner---Sir-Spamabot/blob/main/spam-cleaning-robot.jpg?raw=true)

This Google Apps Script scans your Gmail inbox for spam keywords, unsubscribes from those emails if an unsubscribe link is available, and then deletes the mail. It then sends you a summary of what was deleted and unsubscribed from, including links to recover emails if necessary.

### Features:
- **Keyword-based spam detection**: Detects spam emails based on a customizable list of keywords.
- **Automatic Unsubscribe**: Unsubscribes from emails with an available unsubscribe link before deleting.
- **Detailed Summary**: Sends you a summary of deleted and unsubscribed emails, with links to restore them if necessary.

---

## 🚀 How to Set Up:

### 1. **Open Google Apps Script:**
- Go to [Google Apps Script](https://script.google.com/).
- Click the `New Project` button to create a new Apps Script project.

### 2. **Paste the Code:**
- Copy the script from this repository.
- In the Google Apps Script editor, paste the script into the main code editor window.

### 3. **Save the Script:**
- Once the script is pasted, click the `File` menu and then `Save`.
- Give the project a name like `Gmail Spam Cleaner`.

### 4. **Grant Permissions:**
- Before running the script, Google Apps Script will request permissions to access your Gmail.
- Click `Run` -> `cleanUpSpam()` for the first time, and the script will prompt you to grant the necessary permissions.
- Follow the prompts and approve the required permissions to allow the script to manage your Gmail inbox.

### 5. **Set Up Triggers to Automate the Script:**

To make the script run automatically at a set interval (daily, weekly, etc.), you'll need to set up a trigger:

1. **Open the Triggers Menu:**
   - In the Apps Script editor, click the clock icon in the left-hand toolbar (or go to `Triggers` -> `Add Trigger` from the top menu).

2. **Create a Trigger:**
   - **Choose which function to run:** Select `cleanUpSpam`.
   - **Select event source:** Choose `Time-driven`.
   - **Select type of time-based trigger:** Select `Day timer` for daily cleanup, or `Week timer` for weekly cleanup.
   - **Set time of day:** Choose a specific time for the script to run (e.g., every morning).

3. **Save the Trigger:**
   - Click `Save`, and the trigger will be scheduled. The script will now run automatically at the selected intervals to clean your inbox.

---

## 🧰 Customization Options:

### 1. **spamKeywords** (Array):
The list of keywords used to detect spam. The script searches for these keywords in both the subject line and body of the email. You can easily expand this list to add new keywords based on your preferences.

```javascript
var spamKeywords = [
  'unsubscribe', 'promotion', // Add more keywords as needed...
];

You can...
