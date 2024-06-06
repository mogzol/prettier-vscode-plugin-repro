# Prettier VSCode Plugin Find & Replace Issue Reproduction

1. Clone this repo
2. Run `npm install` on all packages: `bash -c 'for d in ./*/ ; do (cd "$d" && npm i); done'`
3. In VSCode, search all files for `"1.0.0"` and replace with `"2.0.0"`
   - This should replace 3 occurrences across 3 `package.json` files
   - If there are more occurrences, make sure the "Use Exclude Settings and Ignore Files" option is enabled
4. Check the `package.json` files, verify that ONLY that string was replaced in each file (check that package name still matches folder name)
   - If the issue occurs, one or more of the files will have been completely replaced with the contents of one of the other files
   - This may take a few attempts
