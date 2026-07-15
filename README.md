# Welcome to Foto Flasher!

Foto Flasher allows you to chronologically rename entire folders and directories of pictures within just a few seconds. This was designed for photographers who need to rename large sets of pictures all at once but don't want to manually rename every file. This tool is incredibly useful for photographers needing to upload pictures to Bring A Trailer, RM Sotheby's, or Mecum for example. I personally use this tool to upload my pictures to Bring A Trailer, who require chronological order, and found no programs that could solve my issue. If this program helps your projects personally or professionally make sure to leave a star :) it means alot



https://github.com/user-attachments/assets/702bd161-b949-4326-9ac5-bc43220be70e




## Setup & Installation:

open a new session in your preferred terminal and run:

```sh
git clone https://github.com/ooofruitsnacks/foto_flasher.git
```

once it has finished downloading, run:

```sh
cd foto_flasher
```

after changing directory to foto_flasher, run:

```sh
cargo build --release
```

Once it has compiled you are free to use the program.

## How to use Foto Flasher:

Go to the foto flasher directory

```sh
cd foto_flasher
```

Set a new "string". The string must include all the proper "flags" like the target directory and the new name for the pictures. for example:

```sh
./target/release/foto_flasher --dir "/users/example/testing_pics" --name "testingforgithub.jpg" --dry-run
```

The entire "string" above is very simple to breakdown and understand what's happening. Below it is broken down.

The ``` ./target/release/foto_flasher``` is the program....duh.

The ``` --dir "/users/example/testing_pics" ``` is the target directory/sub-directory path you want to rename. You are telling the program to target the "testing_pics" sub directory within the "me" directory and to rename all the pictures within that directory, you aren't telling the program to rename the folder don't worry.

PLEASE NOTE: depending where you save the Foto Flasher program, it will change the path name and may not work if you copy the direct string. Make sure your path is correct to where you have it saved, if you are using a Mac this can be found by looking at the bottom of the finder view port. It will say "Macintosh HD > Users > etc. etc." This is your path.

The ``` --name "testingforgithub.jpg" --dry-run``` is the new name for the pictures. There is no need to add numbers or start it with "0" because the program automatically reorders everything in chronological order but if you need to start at a specific number, just add ```--start``` or ```-s``` at the end of your string. 

Remove the ```--dry-run``` flag from the string and it will execute, dry run mode is used to double check changes ahead of time without implementing them. A stadalone CSV document titled "rename_log.csv" with of all the changes are saved within Foto Finder for the user to have in case there is any error with 1 specific photo. You can use this document as reference for every change made.

## Flags

You can use the full name or an abbrievated version with just "-" and the beginning letter of the word. 

```--dir, -d``` :folder containing the photos, will always be in the string.

```--name, -n``` :new name for pictures, will always be in the string.

```--start, -s``` :starting number; if the user wants to start at a sepcific number, use at the very end of the string.

```--dry, -d``` :test run to verify the names ahead of any changes, use at the very end of the string. 

```--recursive, -r``` :include other photos within sub-folders/directories, use after the directory flag but before the newname flag in the string.

```--log``` :custom path for the recent changes CSV Log (default is rename_log.CSV)

## How it works: 

Input the string with the correct info:

<img width="809" height="405" alt="Screenshot 2026-07-14 at 6 40 06 PM" src="https://github.com/user-attachments/assets/85294b31-f431-45f6-9246-ecb4a5bcf4e3" />

The program automatically detects how many pictures are in a folder and how to structure renumbering:

<img width="665" height="92" alt="Screenshot 2026-07-14 at 6 40 30 PM" src="https://github.com/user-attachments/assets/726d2359-5bac-4dc8-8eb8-8e78db41c472" />

The files are renamed within just a few seconds. No hassle.

<img width="603" height="135" alt="Screenshot 2026-07-14 at 6 40 38 PM" src="https://github.com/user-attachments/assets/f70663e9-8d6a-45c9-aa63-7ab5afebcc91" />


