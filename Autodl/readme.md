### This is only for people who wish to use this platform https://www.autodl.com/home

1. Start a new instance with the ```Gromacs``` image

2. Clone this repo by ```git clone```

3. create a new environment with ```env.yml``` provided in this repository.

4. switch to this new env, and create a new kernel for Jupyter notebook with ```python -m ipykernel install --user --name=pl3_mmpbsa ```

5. Double-click on ```wemd,ipynb``` and you are almost set to run a simulation.

6. change the path to amber tools if you encounter any issue in the execution of the code, for example, there are lines like ```tleap_command = "/root/miniconda3/envs/pl3_mmpbsa/bin/tleap -f " + str(tleap)```
7. If the path may not be the same as you created, use ```conda env list``` to print the correct path and replace it with the correct path.

The ```wemd.ipynb``` contains a piece of code that allows you to do the MMPBSA calculation and per-residue decomposition on the fly directly in the notebook

```
MMPBSA能量分解预处理
https://plip-tool.biotec.tu-dresden.de/plip-web/plip/index
下载/上传 prot_lig_prod_1.pdb，点击分析
抄录所有的口袋氨基酸序号

！ 注意，请展开这段代码修改口袋氨基酸序号
每个氨基酸序号以英文逗号隔开
请同时输入小分子的数字编号 （PLIF 左上角可查看）
"""&decomp """  + "\n"
""" idecomp=2, dec_verbose=3, """ + "\n"
""" print_res="84, 87, 91, 99, 111, 118, 165" """ + "\n"
```
You also need to modify the 

```
amberhome = "source /root/miniconda3/envs/pl3_mmpbsa/amber.sh"
```
to the previously created new env path.
