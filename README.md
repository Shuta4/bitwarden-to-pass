# Bitwarden to pass
Imports passwords from [bitwarden](https://bitwarden.com/) to [pass](https://passwordstore.org/).

(Better? solution: [pass-import](https://github.com/roddhjav/pass-import/))

## Usage
1. Backup your existing password storage, gpg keys and whatever-else you want.
2. (recommended) Create new empty password storage.
3. Just type `./bitwarden-to-pass --help`.

## Warning
1. **Do not use this script without backing up your password storage.**
2. It is better to use this on empty `PASSWORD_STORE_DIR`.

## Features
- Just one python script.
- Works with types and fields:
  - **Login**:
    - `<folder>/<name>` = `password`
    - `<folder>/<name>.d/username` = `username`
    - `<folder>/<name>.d/notes` = `notes`
  - **Card**:
    - `<folder>/<name>` = `number`
    - `<folder>/<name>.d/cardholder` = `cardholder`
    - `<folder>/<name>.d/code` = `code`
    - `<folder>/<name>.d/expiration` = `<expiration_month>/<expiration_year>`
  - **Secure note**: `<folder>/<name>` = `notes`
  - **Custom fields**: `<folder>/<name>.d/fields/<field_name>` = `<field_value>`
