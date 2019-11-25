# Recognizing Hands and Fingers

## Where is the documentation?
[First milestone](doc/Milestone%20I.md)

Other Documents (related papers, time sheets...) will be added to [this directory](doc) as well.

## Things done so far:
- found ways to separate hands from background
- found a suitable framework to work with
- can grab live video from camera
- [look here for more](doc/Milestone%20I.md)



## Git ignores your file?
This is a whitelist only `.gitignore` file. 
This keeps most of the local files out of the git.
To allow a new file to be added:

Edit the root `.gitignore`
and add an entry
```git
!/subfolder/your_file.txt
```
Then remove the already ignored file from the cache (file will stay in its place but is not ignored anymore)
```shell script
git rm -r --cached -f your_file_or_dir_here
```
then `git add` normally.
