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

批量提取目标序列
```
seqkit grep --pattern-file id.txt test_genome.10contig.fna > output.fna
```

批量提取序列id(cut -f1)及序列长度(cut -f1-2)
```
samtools faidx all.324056.candidate.pc.representive.protein.faa
cut -f1-2 all.324056.candidate.pc.representive.protein.faa.fai > genome.id
```
