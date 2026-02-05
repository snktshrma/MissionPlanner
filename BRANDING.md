# Arigni defence – logo and image placement

Use these locations so the app uses your branding assets.

## Image files

| Your file     | Place in folder      | Usage |
|---------------|----------------------|--------|
| **splashbg.png** | `Resources/`         | Splash screen background at startup. If present, it replaces the default splash image. |
| **logo.png**     | `Resources/`         | Available as `MissionPlanner.Properties.Resources.logo` (e.g. for splash or UI). |
| **logo2.png**    | `Resources/`         | Available as `MissionPlanner.Properties.Resources.logo2`. |

All of the above are already referenced in `Properties/Resources.resx`. Add the files under the **MissionPlanner/Resources/** directory (same folder as `splashdark.jpg`, `planner.png`, etc.).

## Application icon (exe and taskbar)

The executable icon is set by **`ApplicationIcon`** in `MissionPlanner.csproj`, which points to an **.ico** file.

- **Option A:** Replace **`mpdesktop.ico`** in the **project root** (same folder as `MissionPlanner.csproj`) with your own .ico file, keeping the name `mpdesktop.ico`.
- **Option B:** Save your icon as **`icon.ico`** in the project root and change the csproj line to:
  ```xml
  <ApplicationIcon>icon.ico</ApplicationIcon>
  ```

Windows requires a **.ico** for the exe icon. If you only have **icon.png**, convert it to .ico (e.g. with an online converter or Visual Studio) and use one of the options above.

## Summary

- **Resources/** (e.g. `MissionPlanner/Resources/`): `splashbg.png`, `logo.png`, `logo2.png`
- **Project root**: `mpdesktop.ico` (replace existing) or `icon.ico` (and update `ApplicationIcon` in the csproj)

After adding the files, rebuild the project.
