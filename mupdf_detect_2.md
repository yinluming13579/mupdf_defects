Affected Version: mupdf 1.23.9

Vulnerability Description: The vulnerability is a memory leak issue, where a local variable named "menuEntry" in the glutAddMenuEntry function is allocated memory but not released.

mupdf download address: https://github.com/ArtifexSoftware/mupdf

Defect Location and Description: A memory leak exception issue was discovered in mupdf in functon glutAddMenuEntry() of /mupdf/thirdparty/freeglut/src/fg_menu.c in line 848.
![image](https://github.com/yinluming13579/mupdf_defects/blob/main/mupdf_detect_2.png)

A memory area is allocated for the variable menuEntry at line 846 of the program. When the macro defined at line 848 holds true (when fgStructure .CurrentMenu is empty), the function returns without releasing the allocated memory area.
