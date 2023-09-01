# MiscStuffs
Some useful stuffs 

1. To find filenames with filters. ! -> NOT  -o -> OR 
find . -type f ! -name "*_mod*" ! -name "*.php" \( -name "*.png" -o -name "*.pdf" -o -name "*.eps" -o -name "*.root" \)  > deleteFile.txt

2. To delete a list of files whose paths are stored in a file.
xargs --arg-file="deleteFile.txt" rm
