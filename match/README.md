# Espanso Configuration

This repository contains a configuration for Espanso, a cross-platform text expander. The snippets are organized into categorized YAML files for better manageability.

## Structure

The Espanso configuration is structured as follows:

*   **`base.yml`**: This is the main entry point for Espanso. It is configured to load all snippet files from the `user/` directory.
*   **`user/` directory**: This directory contains all the actual snippet definition files, categorized by their purpose:
    *   `ai.yml`: Snippets related to AI tools and guidance (e.g., ChatGSFC, LibreChat).
    *   `contacts.yml`: Email distribution lists and personal contact information.
    *   `cybersecurity.yml`: Snippets for cybersecurity-related phrases and actions.
    *   `dynamic_content.yml`: Snippets that generate dynamic content like dates, times, or execute shell commands.
    *   `forms.yml`: Form-based snippets (e.g., SBI feedback form).
    *   `general.yml`: Common acronyms, initialisms, and simple text replacements.
    *   `media.yml`: Snippets for inserting images and emojis, including a script to copy images to the clipboard.
    *   `microsoft.yml`: Shortcuts for Microsoft product names.
    *   `schedule.yml`: Contains the `jgdaily` snippet, which uses a Python script to generate a daily schedule summary, including meetings and ToDo items from a local file.
*   **`base_archive.yml`**: A backup of the original monolithic `base.yml` file before it was refactored.

## Overview of Snippet Categories

The snippets are organized into the following categories within the `user/` directory:

*   **AI (`ai.yml`):** Quick links and information about AI tools and NASA's GenAI guidance.
*   **Contacts (`contacts.yml`):** Collections of email addresses for distribution and personal contact details.
*   **Cybersecurity (`cybersecurity.yml`):** Common phrases and responses for cybersecurity tasks.
*   **Dynamic Content (`dynamic_content.yml`):** Generate current/relative dates and times, or run shell commands.
*   **Forms (`forms.yml`):** Interactive forms, such as the SBI feedback form.
*   **General (`general.yml`):** Frequently used simple text expansions, acronyms, and common phrases.
*   **Media (`media.yml`):** Insert static images, emojis, or use scripts to copy images to the clipboard (e.g., NASA meatball logo).
*   **Microsoft (`microsoft.yml`):** Shortcuts for Microsoft applications and services.
*   **Schedule (`schedule.yml`):** The `jgdaily` snippet provides a detailed daily agenda by running a Python script that pulls meeting information (hardcoded in the script) and ToDo items (from a local `review.md` file).

## Espanso

Espanso is an open-source, cross-platform text expander that helps you save time by automating repetitive typing tasks. You can learn more about Espanso and its configuration at [https://espanso.org/docs/](https://espanso.org/docs/).

## Usage

1.  **Install Espanso:** If you haven't already, download and install Espanso from [espanso.org](https://espanso.org).
2.  **Place Configuration:**
    *   Copy the `base.yml` file and the entire `user/` directory into your Espanso configuration path.
        *   **Windows:** `%APPDATA%\espanso` (e.g., `C:\Users\YourUser\AppData\Roaming\espanso`)
        *   **macOS:** `~/Library/Application Support/espanso` (or `~/config/espanso` if XDG compliant)
        *   **Linux:** `~/.config/espanso`
    *   Ensure that `base.yml` is in the root of your Espanso configuration directory (e.g., `espanso/base.yml`) and the `user` directory is at the same level (e.g., `espanso/user/`).
3.  **Restart Espanso:** Espanso usually detects changes automatically, but a restart might be necessary.

The `base_archive.yml` file is not needed for operation but is kept as a reference to the original, single-file configuration.
