# Firefox Matugen Setup

## Step 1: Find Your Firefox Profile Directory

In Firefox, go to `about:support` and locate the directory next to **Profile Directory** under the **Application Basics** header.

## Step 2: Copy the Template

Copy `matugen/firefox-websites.css` into `~/.config/matugen/templates`.

## Step 3: Update Matugen Config

An example entry is provided in `config.toml` in this repository. Copy that entry to your matugen config at `~/.config/matugen/config.toml`.

**Important:** You must swap out the Firefox profile directory path in the example with your own profile directory path found in Step 1.

## Step 4: Create the Chrome Folder

Inside your Firefox profile directory, create a folder named `chrome`.

## Step 5: Copy the Websites Folder

Copy the `websites` folder into the `chrome` folder you just created.

## Step 6: Create userContent.css

Create a `userContent.css` file inside the `chrome` folder.

### Add the Colors Import

Add this as the first line:

```css
@import url("./colors.css");
```

### Add Website Theme Imports

Add an import line for each website CSS theme you want to have applied. For example:

```css
@import url("./websites/arch_wiki.css");
```

## Step 7: Refresh Matugen

Refresh matugen by either:
- Selecting a wallpaper, or
- Running this command:
  ```
  ~/user_scripts/theme_matugen/theme_ctl.sh refresh
  ```

## Step 8: Relaunch Firefox

Relaunch Firefox to apply the changes.
