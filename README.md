# naikaOS - Android 13
![](https://i.imgur.com/LyE9EfX.png)

## **Downloading Source Code:**

To get started with the building naikaOS for your device, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

To initialize your local repository, use a command like this:


```bash

repo init -u https://github.com/Naika-DAO/android_manifest.git -b naika-1.0

```

  

then to sync up:

  

```bash

repo sync -c -j$(nproc --all)

```

  

> To speed syncs, pass the -c (current branch) and -jthreadcount flags.

> Also to suppress output, pass the -q (quiet) flag.

  
  

## Compilation of naikaOS:

  

From root directory of Project, perform following commands in terminal to start Compilation.

```bash

# Initialize the environment with the envsetup.sh script:

source build/envsetup.sh

# lunch your device (codename)

lunch naika_<devicecodename>-userdebug

# start compilation for your device

make bacon # Recovery Package
# or
make scramble # Fastboot Package

```

-----------------------------------------------------------------------------