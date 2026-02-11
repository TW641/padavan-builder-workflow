# Padavan 3.4 ng Builder - The "Dave Täht Tribute" Edition

> **"When you miss Dave, modprobe sch_cake!"**
> — *A tribute to the soul of bufferbloat mitigation.*

---

## 🕊️ In Loving Memory of Dave Täht

### **"穿越時空的夢想，我來幫他實現！"**
**(Making a time-traveling dream come true!)**
### **🇹🇼：靈魂永駐，精神長存**
### **🇺🇸：May his soul find eternal peace, and his spirit live on forever.**

This workflow is dedicated to **Dave Täht**, a visionary whose work on **FQ-CoDel**, **CAKE**, and **LibreQoS** changed the internet forever. We are fulfilling a wish he made 5 years ago on Reddit:

### ❝ Help port the code to more chipsets. ❞

> **The BEST engineering result I ever had:**
> Essentially the summation of my 16+ years of work to that point on making wifi better. Unpatented. Please share and enjoy.
> **Help port the code to more chipsets.**
>
> — *Dave Täht (Reddit, 5 years ago)*

*Original Source:* [Reddit - r/Starlink](https://www.reddit.com/r/Starlink/comments/okmx3x/comment/h61unnn/)

Dave turned down numerous lucrative contracts to keep his code **Free and Open Source**. He valued global impact over prestige. Because of him, millions of devices—from Starlink satellites to rural ISP routers—deliver smoother connectivity.

**May his soul find eternal peace, and his spirit live on forever in our routers.**

[👉 Read the full Memorial at LibreQoS](https://libreqos.io/2025/04/01/in-loving-memory-of-dave/)

---

## 🌟 Project Philosophy: Open & Accessible

### **「永遠保持開放且開源的精神」**
**(Forever maintaining an open and open-source spirit)**

This repository automates the building of **Padavan 3.4 ng** firmware. It empowers users to compile their own firmware easily using GitHub Actions, honoring the giants who paved the way.

1.  **CAKE Integration**: Supports the `sch_cake` module (backported to 3.4) to honor Dave's legacy.
2.  **Interactive Build System**: No need to edit config files manually! Just select your model and options from the menu.
3.  **Flexible Language System**: Choose between **English Only** (clean) or **Custom Language** (Localized) directly in the build menu.

---

## 🗣️ Tributes from the Community

> "Dave’s impact on society was immense... He wanted, ultimately, to speed up the internet so that a drummer in London could play in real-time with a guitarist in Los Angeles."
> — **Steven J. Vaughan-Nichols**

> "I will miss him but will be always grateful to have known him."
> — **Vint Cerf**

> "Without him, Netflix and similar services might still be plagued by glitches and stutters."
> — **Eric S. Raymond**

### See also:

* [LibreQoS Project](https://libreqos.io/)
* [LibreQoS Github Project](https://github.com/LibreQoE/LibreQoS/)
* [Dave's Talks: Reducing Network Latency (GOTO 2024)](https://www.youtube.com/watch?v=UDo9W4tt69c)

![Dave Täht Tribute](https://i0.wp.com/libreqos.io/wp-content/uploads/2025/04/WISPAPALOOZA-2024_6.jpg)
*[Image Credit: LibreQoS]*

---

## 🚀 Supported Devices (Kernel 3.4)

We support a vast array of **MT7620/MT7621** devices. Pick the one you love!

| Brand | Models (Examples) |
| :--- | :--- |
| **Xiaomi** | MI-3, MI-4, MI-MINI, MI-NANO, MI-R3G (v1/v2), R2100 |
| **ASUS** | RT-N56U, RT-N14U, RT-AC1200, RT-AC51U, RT-N11P |
| **TP-Link** | TL-WR840N/841N (multiple versions), TL-C20, TL-C50, TL-MR series |
| **ZyXEL** | Keenetic series (Giga III, Ultra II, Extra, Lite, Omni, Viva) |
| **D-Link** | DIR-882, DIR-878, DIR-860L, DIR-620 |
| **And many more** | Newifi, Phicomm, Totolink, Belkin, GL.iNet, HiWiFi, Linksys, ZTE... |

---

## 🛠️ Usage (How to Build)

This workflow uses **GitHub Actions** to build firmware in the cloud. You don't need a Linux PC!

### 1. Start the Workflow
1.  Go to the **[Actions](../../actions)** tab in this repository.
2.  Select the workflow **"Build firmware (Ultimate Fix)"** (or `build.yml`) from the left sidebar.
3.  Click the **Run workflow** button on the right.

### 2. Configure Your Build (Interactive Inputs)
You will see a menu with the following options. **Customize it to your liking!**

* **target_select** (Required):
    * Choose your router model from the list (e.g., `TL_C2-V1`, `MI-MINI`, `RT-N56U`, `K2P`...).
    * *Note: This list includes all supported 3.4 kernel devices.*

* **language_select** (New!):
    * `English_Only`: Keeps the interface clean and lightweight.
    * `CN (繁體中文)` / `RU` / `ES` etc.: Automatically adds your selected language pack.

* **nanoversion**:
    * `true`: Performs extreme size optimization (removes unused modules) to fit into small flash memory (4MB/8MB).

* **customization**:
    * Set your default WiFi SSID, Password, and Login credentials here (JSON format).

### 3. Wait & Download
1.  Click the green **Run workflow** button.
2.  The build process usually takes **15 to 40 minutes**.
3.  When the circle turns **Green (Success)**, click on the task.
4.  Scroll down to the **Artifacts** section to download your firmware `.zip` file.

---

## ⚖️ Credits & Disclaimer

This project is based on `shvchk/padavan-builder-workflow` and the incredible `padavan-ng` project by **Sergey Hadzhioglu**.

### Support the Original Developers
To express gratitude and support Sergey's work on Padavan-NG:
* **ЮMoney wallet**: `4100118647832050`
* [Link for quick replenishment](https://yoomoney.ru/to/4100118647832050)

### DISCLAIMER
**NO WARRANTY OR SUPPORT**
This product includes copyrighted third-party software. The firmware is provided "AS IS" without warranty of any kind. You expressly acknowledge that use of this software is at your sole risk. Flash at your own risk!

---

<p align="right">English | <a href="README.ru.md">Русский</a></p>

## Automatic Padavan firmware builds using GitHub servers

### Usage

- [Fork this repository](https://github.com/shvchk/padavan-builder-workflow/fork), further steps should be performed in your fork

- Copy your build config to [`build.config`](build.config)

  Build config template can be found in the [firmware repository](https://gitlab.com/hadzhioglu/padavan-ng/-/tree/master/trunk/configs/templates)

- Run the build process: [Actions](../../actions) → [Build firmware](../../actions/workflows/build.yml) → Run workflow

  ![run workflow](misc/run-workflow.webp)

  The build process will appear on the same page (if it doesn't appear, just refresh the page). You can get process details by clicking on it.

  Depending on the build config, build process usually takes from 10 to 60 minutes.

- While the process is in progress, its status indicator would be gold-ish circle

  ![workflow status progress](misc/workflow-status-in-progress.webp)

- If the process finishes successfully, its status indicator would turn green with a check mark

  ![workflow status success](misc/workflow-status-success.webp)

  Click on the finished process. Archive with the firmware would be stored as its artifact:

  ![workflow artifacts](misc/workflow-artifacts.webp)

  Firmware license does not permit binaries distribution, so artifacts are stored for 7 days for personal use.

- If the process finishes with an error, its status indicator would turn red with a cross

  ![workflow status fail](misc/workflow-status-fail.webp)

  Click on the finished process. To get details about the error, click on the failed `build` job at the left:

  ![workflow details fail](misc/workflow-details-fail.webp)

  Job report will be opened:

  ![workflow details get logs](misc/workflow-details-get-logs.webp)

  Here it's immediately obvious that it was *Check firmware size* step that failed — it is marked with a red circle with a cross. Specific reason is shown below: *Firmware size (18,492,849 bytes) exceeds max size (16,187,392 bytes) for your target device* — i.e. built firmware size is too big for the target device.

  In case of any error its reason is usually shown at the end of the log, as in the example above. To view full log click on the cog ⚙️ icon in the top right corner → View raw logs. You can also download compressed log archive in the same menu → Download log archive.

  If you can't figure out the problem on your own, you can ask community or firmware developer for help. In this case don't forget to attach the log archive.


### Updating your fork

To sync your fork with its origin repository, just click *Sync fork* → *Update branch* at the top of the main page of your fork:

![sync fork](misc/sync-fork.webp)


### Advanced usage

You can set the firmware repository, branch, specific tag or commit in the [`variables`](variables) file.

In the [`variables`](variables) file you can also specify which themes you want to install by uncommenting theme names in the `PADAVAN_THEMES` variable. Themes repository can be set with the `PADAVAN_THEMES_REPO` variable.

You can create a `pre-build.sh` script with any custom commands, which will be executed just before build process. By that time firmware source code is already downloaded, so you can add or change anything in it.

You can create a `post-build.sh` script, which will be executed right after build process.


---

Discussion: https://github.com/shvchk/padavan-builder-workflow/discussions/categories/general
