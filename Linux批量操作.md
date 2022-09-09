批量修改文件名
```
ls *oldname|xargs -I {} mv {} {}.newname
```

批量投递任务
```
ls split*.sh|xargs -I {} qsub -cwd  -l num_proc=1 -binding linear:1 -l vf=2g -q st.q -P P17Z10200N0246 {}
```

批量输出文件路径
```
find /path/to.file/ -name "*.filenname"  >test
```
