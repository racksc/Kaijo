# Kaijo PaperSpigot 1.7.10 Fork #
<p>This is the primary repository for the Kaijo PaperSpigot 1.7.10 software. PaperSpigot is a high performance 
Spigot fork that aims to fix gameplay and mechanics inconsistencies. I will not continue to update this, development is finished. This was created for kPractice and to be similar to Kohi.</p>

# Disclaimer #
This was originally the IPVP fork of PaperSpigot but I modified it more.
Modifications Include
- Hidden players being able to have their name tabbed and not having their name removed from the tablist upon vanish. 
- Players that are hidden can't see projectiles or receive potion splash effects from players that have them hidden. 
- Most of the command colors are changed to represent Kohi's aesthetic. 
- Console broadcast has been changed. 
- Version name is renamed to "Kaijo" (getVersionName). 
- Knockback is patched from prplz's code (https://gist.github.com/prplz/88058283059dd46c8208c8a918c65bb8).


## Installation Instructions ##
Install Kaijo:

1. Clone this repository to your computer via `git clone` or GitHub's download feature
2. Initialize git submodules: `git submodule update --init` 
3. Apply code patches to update submodules: `./applyPatches.sh`
4. Compile the code via [Maven 3](http://maven.apache.org/download.html): `mvn clean install`

The PaperSpigot server file will appear in the `PaperSpigot-Server/target/` directory as `paperspigot-1.7.10-R0.1-SNAPSHOT.jar`

**New to this?** <br />
Installation requires Git and Maven 3, if you do not have these please view the following links:

* [Maven 3 Download](http://maven.apache.org/download.html) and [Installation Instructions](https://maven.apache.org/install.html)
* For Windows: [Git Download](https://git-scm.com/downloads)


## Developers ##
Creation of a patch is simple and easy:

1. Follow the Installation Instructions and install our current patches
2. Navigate to `PaperSpigot-Server` or `PaperSpigot-API` and modify the code you need
3. Commit your changes to the `PaperSpigot-Server` or `PaperSpigot-API` subdirectories
4. Return to the parent directory and execute the `./rebuildPatches.sh` script
    * This will automatically generate your new patch files for your code
