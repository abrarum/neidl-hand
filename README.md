# hand recognition goes here
opencv4nodejs cloned from [here](https://github.com/justadudewhohacks/opencv4nodejs)

## Run?
Open Intellij and open the `opencv4nodejs` folder. Run `npm install`.
Right click `opencv4nodejs/examples/handGestureRecognition0.js` and then `DEBUG`.
This creates a new run configuration. Open it.

Make sure that the working directory points to `opencv4nodejs/examples/`.

Launch.

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
