# easyPlace
Reimplementation of the electrostatic-based VLSI placement algorithm: ePlace and ePlace-MS with clean C++ code. This code is for those who try to understand the electrostatics-based placement. 

Reimplementation of Abacus is applied for internal std cell legalization.

Independent set matching, local reordering and global swap are applied for internal detailed placement.

# How to Build
To build, go to the root directory.
```
mkdir build
cd build 
cmake .. 
cd main
make
```
# How to Run
sample command:
```
./ePlace -aux ./adaptec4.aux -targetDensity 1.0  -fullPlot -targetOverflow 0.1 -legalizerPath YOUR_LEGALIZERPATH -outputPath YOUR_OUTPUTPATH
```
# Options
* -aux: specify input aux file
* -targetDensity: specify target density
* -targetOverflow: specify target overflow
* -legalizerPath: specify the path of external legalizer (support ntuplace3 only for now) and call ntuplace3 to complete legalization and detailed placement
* -outputPath: specify the output path 
* -fullPlot: plot cell locations during the placement process
* -noQP: skip initial placement(quadratic placement)
* -nomGP: skip mixed-size global placement
* -nomLG: skip macro legalization and cell global placement
* -nocGP: skip cell global placement
* -noLegal: skip legalization
* -addNoise: add random noise before mGP

# References
### Global Placement:
* [ePlace](https://dl.acm.org/doi/10.1145/2699873)
* [ePlace-MS](https://ieeexplore.ieee.org/document/7008518)
* [RePlAce](https://ieeexplore.ieee.org/document/8418790)
* [Xplace](https://github.com/cuhk-eda/Xplace)

### Legalization:
* [Abacus](https://dl.acm.org/doi/10.1145/1353629.1353640)

### Detailed placement techniques:
* [NTUplace3](https://ieeexplore.ieee.org/document/4544855)
* [ABCDPlace](https://ieeexplore.ieee.org/document/8982049)
* [FastPlace](https://ieeexplore.ieee.org/document/1560039)

# Authors
Ziang Ge and Yikai Liu, supervised by Prof. [Pingqiang Zhou](https://faculty.sist.shanghaitech.edu.cn/faculty/zhoupq/home.html) at [ShanghaiTech University](https://www.shanghaitech.edu.cn/)
