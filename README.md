# MiscStuffs
Some useful stuffs 

1. To find filenames with filters. ! -> NOT  -o -> OR 
find . -type f ! -name "*_mod*" ! -name "*.php" \( -name "*.png" -o -name "*.pdf" -o -name "*.eps" -o -name "*.root" \)  > deleteFile.txt
