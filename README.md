# MiscStuffs
Some useful stuffs 

1. To find filenames with filters. ! -> NOT  -o -> OR
   ```
   find . -type f ! -name "*_mod*" ! -name "*.php" \( -name "*.png" -o -name "*.pdf" -o -name "*.eps" -o -name "*.root" \)  > deleteFile.txt
   ```

2. To delete a list of files whose paths are stored in a file.
   ```
   xargs --arg-file="deleteFile.txt" rm
   ```

### 3. Error installing MG5aMC_PY8_interface
   Solution was obtained from the forum [link](https://answers.launchpad.net/mg5amcnlo/+question/816173) \
   First add ```-pthread``` in the file ```./MG5aMC_PY8_interface/Makefile_mg5amc_py8_interface_static:	$(CXX) $@.cc -o $@ $(HEPMC2_INCLUDE) $(CXX_COMMON) $(HEPMC2_LIB) -pthread``` \
   then run the following:
   ```
   cd /home/shubhamdutta/Applications/Package_install/MG5_aMC_v3_5_3/HEPTools/MG5aMC_PY8_interface
   python3 compile.py ../pythia8/
   ```
