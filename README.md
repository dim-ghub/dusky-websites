# Firefox Matugen Setup

## Step 1: Find Your Firefox Profile Directory

In Firefox, go to `about:support` and locate the directory next to **Profile Directory** under the **Application Basics** header.

## Step 2: Edit the Matugen Template

Edit the matugen template to reflect the real path to your Firefox (or Firefox-based browser's) profile directory.

## Step 3: Copy the Template

Copy the template into `~/.config/matugen/templates`.

## Step 4: Update Matugen Config

Add the template to your matugen config at `~/.config/matugen/config.toml`.

## Step 5: Create the Chrome Folder

Inside your Firefox profile directory, create a folder named `chrome`.

## Step 6: Copy the Websites Folder

Copy the `websites` folder into the `chrome` folder you just created.

## Step 7: Create userContent.css

Create a `userContent.css` file inside the `chrome` folder.

### Add the Colors Import

Add this as the first line:

```css
@import url("./colors.css");
```

### Add Website Theme Imports

Add an import line for each website CSS theme you want to have applied. For example:

```css
@import url("./websites/arch-wiki.css");
```

## Step 8: Refresh Matugen

Refresh matugen by either:
- Selecting a wallpaper, or
- Running this command:
  ```
  ~/user_scripts/theme_matugen/theme_ctl.sh refresh
  ```

## Step 9: Relaunch Firefox

Relaunch Firefox to apply the changes.
