Affected Version: mupdf 1.23.9

Vulnerability Description: The vulnerability is a memory leak issue, where a local variable named "menuEntry" in the glutAddMenuEntry function is allocated memory but not released.

mupdf download address: https://github.com/ArtifexSoftware/mupdf

Defect Location and Description: A memory leak exception issue was discovered in mupdf in functon glutAddMenuEntry() of /mupdf/thirdparty/freeglut/src/fg_menu.c in line 848.
![image](https://github.com/yinluming13579/mupdf_defects/blob/main/mupdf_detect_2.png)
