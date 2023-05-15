# pie-smash
Minimal local package manager.

I've got bored of manually coping my apps so decided to create my own minimal
package manager so whevener I develop some application I can easily add
it to my desire bin path.

## Installation
**__this was only tested on FreeBSD 13.2 but should be working also with linux__**

### Step 0:
Create manually 2 file in your HOME path: ```.config/pie-smash/pie-smash.conf``` and ```.config/pie-smash/user-apps-data.json```.
> mkdir -p ~/.config/pie-smash
> touch .config/pie-smash/pie-smash.conf .config/pie-smash/user-apps-data.json

### Step 1:
Add bin_path entry to pie-smash.conf, this is the path where manager will create symlinks.
> echo " { \"bin_path\": \"__YOUR/DESIRED/BIN/PATH__\" }" >> .config/pie-smash/pie-smash.conf
Also add brackets to database.
> echo "{}" >> .config/pie-smash/user-apps-data.json

### Step 2:
Clone this to your desired path using https or ssh.
> cd /DESIRED/PATH/
> git clone https://github.com/Challmymind/pie-smash.git pie-smash

### Step 3:
Add this package manager using itself. Run this in your cloned pie-smash directory.
> chmod +x pie-smash
> ./pie-smash add pie-smash

### Check your installation.
Run list option and check output.
> pie-smash list
If you have seen pie-smash entry then everything is correct.

## Currectly working commands.
```pie-smash add APPLICATION``` adds APPLICATION
```pie-smash delete APPLICATION``` deletes APPLICATION
```pie-smash list``` lists all database entries
```pie-smash --version``` prints current pie-smash version
