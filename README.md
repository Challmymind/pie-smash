# pie-smash
Minimal local package manager.

I've got bored of manually coping my apps so decided to create my own minimal <br>
package manager so whevener I develop some application I can easily add <br>
it to my desire bin path. <br>

## Installation
**__this was only tested on FreeBSD 13.2 but should be working also with linux__**

### Step 0:
Create manually 2 files in your HOME path: ```.config/pie-smash/pie-smash.conf``` and ```.config/pie-smash/user-apps-data.json```. <br>
> mkdir -p ~/.config/pie-smash <br>
> touch .config/pie-smash/pie-smash.conf .config/pie-smash/user-apps-data.json <br>

### Step 1:
Add bin_path entry to pie-smash.conf, this is the path where manager will create symlinks. <br>
> echo " { \\"bin_path\\": \\"__YOUR/DESIRED/BIN/PATH__\\" }" >> .config/pie-smash/pie-smash.conf <br>


Also add brackets to database. <br>
> echo "{}" >> .config/pie-smash/user-apps-data.json <br>

### Step 2:
Clone this to your desired path using https or ssh. <br>
> cd /DESIRED/PATH/ <br> 
> git clone https://github.com/Challmymind/pie-smash.git pie-smash <br>

### Step 3:
Add this package manager using itself. Run this in your cloned pie-smash directory. <br>
> chmod +x pie-smash <br> 
> ./pie-smash add pie-smash <br> 

### Check your installation. 
Run list option and check output. <br> 
> pie-smash list <br>


If you have seen pie-smash entry then everything is correct. <br> 

## Currectly working commands.
```pie-smash add APPLICATION``` adds APPLICATION <br> 
```pie-smash delete APPLICATION``` deletes APPLICATION <br> 
```pie-smash list``` lists all database entries <br> 
```pie-smash --version``` prints current pie-smash version <br>
