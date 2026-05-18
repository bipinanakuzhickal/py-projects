# Password Manager

A small GUI application built with `tkinter` that helps generate and save passwords for websites.

## What it does

- Generates a random password containing letters, numbers, and symbols.
- Copies the generated password to the clipboard automatically.
- Lets you save Website / Email / Password entries to a plain text file (`data.txt`).
- Provides a simple graphical interface with buttons for generating and saving passwords.

## How it works

- The main UI is implemented in `main.py` ([Password_Manager/main.py](Password_Manager/main.py#L1)).
- Click `Generate Password` to produce a randomly-created password; it will be inserted into the Password field and copied to the clipboard via `pyperclip`.
- Click `Add` to save the current Website, Email/Username, and Password to `data.txt` in the format: `website | email | password`.
- The application validates that the Website and Password fields are not empty before saving and asks for confirmation with a dialog.

## Files

- `main.py` — main application and UI logic ([Password_Manager/main.py](Password_Manager/main.py#L1)).
- `logo.png` — logo image shown in the UI (should remain in the same folder).
- `data.txt` — text file used to append saved credentials (created/updated at runtime).

## Requirements

- Python 3.x
- `tkinter` (included with standard Python on most platforms; on some Linux distributions install `python3-tk`)
- `pyperclip` — for copying generated passwords to the clipboard

Install `pyperclip` with pip if you don't have it:

```bash
pip install pyperclip
```

## Run

Change to the `Password_Manager` directory and run:

```bash
python main.py
```

## Security note

- Saved credentials are stored in plain text in `data.txt`. This is a simple demo and is NOT secure for storing real passwords. For real use, consider using an encrypted store or a dedicated password manager.

## Improvements (suggested)

- Encrypt saved entries or use an OS secure storage API.
- Add a search or management UI to view/edit saved entries.
- Replace `data.txt` with JSON or a small database for structured storage.

Enjoy!
