![Polyamory Bee-64](https://github.com/user-attachments/assets/def30933-327b-44cc-acc3-d27062fe67e5)
# PolyMC Client Instance
This is the user's client for playing the PolyMC modpack. This has everything you need to launch the game and get into the server, assuming you're whitelisted.

If you are installing this on a new computer or never used Minecraft prior, you will likely need Java installed. This modpack uses **Minecraft 1.20.1,** so please install **Java 17** with [Adoptium's OpenJDK](https://adoptium.net/temurin/releases/). 

If you've already installed Minecraft before using Minecraft's native launcher, look at the F.A.Q. for help if you run into issues.
## Requirements
### Prism Launcher
This modpack is specifically designed to be an import into Prism Launcher.

Download the latest version here: https://prismlauncher.org/download/
### GitHub Desktop
You will also need to download GitHub Desktop or some version of Git to clone the repo.
If you didn't get that last part, just download GitHub Desktop here: https://desktop.github.com/download/

## Installing the Client
### Using GitHub Desktop
Open Github Desktop and **sign into GitHub.**

<img width="1072" alt="Screenshot 2024-08-19 at 11 09 12 AM" src="https://github.com/user-attachments/assets/ddbf59b0-0bff-49b2-bc65-fed1985f15c5">

Click through until you get to the, **"Let's get started!"** screen.

<img width="1072" alt="Screenshot 2024-08-19 at 11 12 14 AM" src="https://github.com/user-attachments/assets/905df878-8812-4e6f-a170-df09cf3489c9">

Click, **"Clone a Repository from the internet..."**
> [!IMPORTANT]
> If you plan to offer mod suggestions in the future, I would recommend forking the repo and cloning that instead. This way you can make pull requests for QoL or server-side mods.
1. Select, "URL".
2. Add the repo URL, https://github.com/soleilfenley/polymc-instance.
3. Find your Prism Launcher `instances` directory. The, `polymc-instance` will add itself.
   * **Windows -** `C:\Users\[your name]\AppData\Roaming\PrismLauncher\instances`
   * **macOS -** `/Users/[your name]/Library/Application Support/PrismLauncher/instances`
   * If these directories are missing, finish the Prism Launcher setup and try again.
4. Finally, click, "Clone".

<img width="579" alt="Screenshot 2024-08-19 at 11 16 40 AM" src="https://github.com/user-attachments/assets/5d287bbd-8b36-4291-b605-002c8e0b0f2d">

After this, you can open Prism and see the instance appear! If not, add a blank instance and the PolyMC instance should populate.

### Using Git
Use the following commands to clone the directory:

**macOS**
```
cd ~/Library/Application\ Support/PrismLauncher/instances
git clone https://github.com/soleilfenley/polymc-instance
```

**Windows**
```
cd %USERPROFILE%\AppData\Roaming\PrismLauncher\instances
git clone https://github.com/soleilfenley/polymc-instance
```

## Updating the Pack
### Checking for Updates
Besides checking GitHub Desktop which I'll explain below, the server has a buillt-in way of telling you before you join it called BCC.

This is a simple version check I make back and forth with the server and the client to ensure you have the latest version.

Below is an example of how it works:

`[Now actually put the example here lol]`

### GitHub Desktop
This is as simple as clicking the, "Fetch origin" to check for updates. 

## F.A.Q.
### I accidentally cloned the client to the wrong directory. How do I delete it?
Click the current directory box on the header and right click the repo to remove it. Then follow the directions to clone it into the `PrismLauncher/instances` directory.
### It says incompatible Java version... what do I do??
This is simple as a Java version that's too old or too new.

**If it's older than Java 17,** 
[Download the latest version of Adoptium's OpenJDK.](https://adoptium.net/download/) As of writing, this is Java 21, compatible with Minecraft 1.21. Once it's installed, then keep reading.

**If it's newer than Java 17,** 
Go into Prism Launcher's settings and under the **Java** section, select, "Skip Java compatibility checks". 

### I keep running into "Out of memory" errors... what do I do?
This is likely during setup, no more than 4GB of memory was allocated to Minecraft. We'll apply two fixes to resolve this:

**Open Prism Launcher's settings and navigate to the Java Section.**
<img width="1081" alt="Screenshot 2024-08-20 at 10 05 45 AM" src="https://github.com/user-attachments/assets/1da4d8aa-2386-49a7-a438-f88a3f7a9a65">

Unlike what I have, you likely only have 128MiB at minimum and 4096MiB, or 4GiB, at max. We'll set this to both minimum and maximum at 8GiB or 8192MiB.

> [!NOTE]
> Setting these is the equivalent of adding `-Xms8192M -Xmx8192M` to your Minecraft Launcher!

<img width="758" alt="Screenshot 2024-08-20 at 10 08 18 AM" src="https://github.com/user-attachments/assets/cd700c04-fe83-463b-82a3-6e09b2a98621">

The second fix were doing is to handle the memory a little better. This is called garbage collection and it won't be difficult, just a copy and paste!

**Open a new tab to https://flags.sh/.** In here, we're just gonna specify how much memory we'll need. 

Pick the same amount you used in Prism Launcher and copy the following parts.

<img width="909" alt="Screenshot 2024-08-20 at 10 14 14 AM" src="https://github.com/user-attachments/assets/16cd42e9-ba97-4d16-ac1c-e87d649fc507">

Paste that into the text box that says JVM Args and you're good!

<img width="727" alt="Screenshot 2024-08-20 at 10 15 31 AM" src="https://github.com/user-attachments/assets/d74cedd8-5e5e-4d55-8f2e-ac58ee92bc19">

### I want to install a mod for myself!
That's awesome, and thanks for showing interest in adding mods to make this modpack personal!

Do your research into the mod and find out if it's Client-only or relies on any server elements.

**If it's client-only,**
great! Edit the instance and search for the mod using [Prism Launcher](https://prismlauncher.org/wiki/getting-started/download-mods/)! If you think this would benefit all players, keep reading.

**If there's server-side elements,** 
1. Make sure you forked the repo before cloning it on your computer. This makes it possible to publish pull requests.
2. Duplicate the instance and download your mods there. This way if things don't pan out, you don't have to re-clone.
3. Test out the mod in a Singleplayer server. Ensure the mod works as expected and has no bugs or severe downsides.
4. Make the same changes to the main instance And push it to your forked repo.
5. Open GitHub online and submit a pull request to this repo, and I'll review it before publishing it accordingly.
