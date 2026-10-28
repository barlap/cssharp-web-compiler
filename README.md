<p align="center">
  <a href="https://cssharp.icegame.ro">
    <img src="https://cssharp.icegame.ro/images/logo-2.png?v=2" alt="CounterStrikeSharp Online Compiler">
  </a>
</p>

[![Website](https://img.shields.io/badge/Website-cssharp.icegame.ro-blue)](https://cssharp.icegame.ro)
[![Guides](https://img.shields.io/badge/Guides-16%20languages-green)](https://cssharp.icegame.ro/guides)

#### 👉 **[cssharp.icegame.ro](https://cssharp.icegame.ro)** **is a free online compiler for [CounterStrikeSharp](https://docs.cssharp.dev/) (CS2) plugins.**
#### **Upload your plugin project as a `.zip`, pick the CounterStrikeSharp.API version, and download the compiled plugin. No local .NET SDK or Visual Studio required.**

## Why this exists

CounterStrikeSharp plugins are full C# projects, not a single file like `.sma` or `.sp` used by AMX Mod X or SourceMod. This compiler handles the whole workflow in the browser: unpacking the project, restoring NuGet packages, building it against the API version you choose, and handing you the result.

## Features

**Project-based workflow**
- Upload a `.zip` with your full project: the `.csproj` plus all `.cs` files
- Built-in code editor to adjust `.cs` and `.csproj` files before compiling
- Compiled plugin is downloaded as a `.zip`, ready for your server
- NuGet packages used by the project are restored automatically

**CounterStrikeSharp.API versions**
- Choose the API version to build against, with search for older versions
- If your plugin targets a different .NET framework or API version, the compiler detects the mismatch and suggests the right version automatically
[![Compilation result](https://github.com/barlap/cssharp-web-compiler/blob/main/cssharp_version_mismatch.PNG)](https://github.com/barlap/cssharp-web-compiler/blob/main/cssharp_version_mismatch.PNG)
- Build configuration: `Release` for live servers, `Debug` for local troubleshooting only

**Isolated builds**
- Dependencies are fetched in an isolated sandbox
- The actual compilation runs in a separate container with no network access, away from the server files
- Compilation queue and per-IP rate limit keep the service stable for everyone

**Interface**
- 16 languages: English, Romanian, Italian, Hungarian, Serbian, Bulgarian, German, French, Russian, Turkish, Portuguese, Hindi, Spanish, Arabic, Japanese, Chinese
- Dark and light mode, responsive layout, usable on mobile
- Compilation statistics by framework and by API version
- Navbar button to switch between the CounterStrikeSharp, SourceMod and AMX Mod X compilers

**Built-in guides (16 languages)**
- Metamod and CounterStrikeSharp setup, your first Hello World plugin, becoming admin, commands and chat, game events, plugin config, NuGet and databases
- Troubleshooting: plugin not loading, compile errors explained, version mismatches, missing project references

## How to use it

1. Go to **[cssharp.icegame.ro](https://cssharp.icegame.ro)** and pick your interface language.
2. Select the **CounterStrikeSharp.API version**. Not sure which one? Use the latest.
3. Upload your project as a **`.zip`** (it must contain the `.csproj`), or edit the files in the built-in editor.
4. Choose the build configuration and press **Compile Now**.
5. If the build succeeds, press **Download** to get the compiled plugin as a `.zip`.

To check which CounterStrikeSharp version your server is running, type `meta list` in the server console.

## Screenshots

<details>
<summary>📸 Main page (click to expand)</summary>

<br>

[![Compilation result](https://github.com/barlap/cssharp-web-compiler/blob/main/cssharp_main_page.PNG)](https://github.com/barlap/cssharp-web-compiler/blob/main/cssharp_main_page.PNG)

</details>
<details>
<summary>📸 Compilation result (click to expand)</summary>

<br>

[![Compilation result](https://github.com/barlap/cssharp-web-compiler/blob/main/cssharp_compiler_result.PNG)](https://github.com/barlap/cssharp-web-compiler/blob/main/cssharp_compiler_result.PNG)

</details>
<details>
<summary>📸 Admin Dashboard (click to expand)</summary>

<br>

[![Admin dashboard](https://github.com/barlap/cssharp-web-compiler/blob/main/cssharp_admin_dashboard.png)](https://github.com/barlap/cssharp-web-compiler/blob/main/cssharp_admin_dashboard.png)

</details>

## Good to know

- The archive must contain the **full project**, not just loose `.cs` files. The `.csproj` is required for the build.
- If your plugin references another project (for example a git submodule), GitHub's "Download ZIP" does **not** include the submodule contents. Add that folder to the archive yourself. The [guides](https://cssharp.icegame.ro/guides) explain how to fix this.

## Links

- Compiler: https://cssharp.icegame.ro
- Guides: https://cssharp.icegame.ro/guides
- IceGame Romania: https://icegame.ro

## Feedback

Found a bug or have a suggestion? Open an [issue](../../issues). Feedback is welcome.
