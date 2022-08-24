# R合并不等长数据
marker数据：  
 <table width="1512" border="0" cellpadding="0" cellspacing="0" style='width:756.00pt;border-collapse:collapse;table-layout:fixed;'>
   <col width="108" span="14" style='width:54.00pt;'/>
   <tr height="28" style='height:14.00pt;'>
    <td height="28" width="108" style='height:14.00pt;width:54.00pt;' x:str>B_pan</td>
    <td width="108" style='width:54.00pt;' x:str>B_naive</td>
    <td width="108" style='width:54.00pt;' x:str>B_intermed<span style='display:none;'>iate</span></td>
    <td width="108" style='width:54.00pt;' x:str>B_memory</td>
    <td width="108" style='width:54.00pt;' x:str>B_Plasma</td>
    <td width="108" style='width:54.00pt;' x:str>Monocyte_p<span style='display:none;'>an</span></td>
    <td width="216" colspan="2" style='width:108.00pt;mso-ignore:colspan;' x:str>Monocyte_classical</td>
    <td width="108" style='width:54.00pt;'></td>
    <td width="108" style='width:54.00pt;'></td>
    <td width="108" style='width:54.00pt;'></td>
    <td width="108" style='width:54.00pt;'></td>
    <td width="108" style='width:54.00pt;'></td>
    <td width="108" style='width:54.00pt;'></td>
   </tr>
   <tr height="28" style='height:14.00pt;'>
    <td height="28" style='height:14.00pt;' x:str>MS4A1,CD78<span style='display:none;'>A,CD79B,BBNK1</span></td>
    <td x:str>IGHM,IGHD,<span style='display:none;'>IL4R,CXCR4,BTG1,TCL1A,YBX3</span></td>
    <td x:str>TNFRSF13C,<span style='display:none;'>IGHM,IGHD,AIM2,LI857,RALGPS2,BANK1</span></td>
    <td x:str>COCH,AIM2,<span style='display:none;'>BANK1,SSPN,TX9,RALGPS2,TNF7,LI781</span></td>
    <td x:str>IGHA2,MZB1<span style='display:none;'>,TNF17,DERL3,TC5,POU2AF1,CNE5,HRS2,NT5DC2</span></td>
    <td x:str>CD14,LYZ,S<span style='display:none;'>100A9,VCAN,S100A8,S100A12,LST1,FCGR3A,MS4A7,IFITM3</span></td>
    <td colspan="8" style='mso-ignore:colspan;' x:str>CD14,CD16,CD36,CCR2,CD64,CD62L,PU1,JN,FOS,IRF8,KLF4,VCN,CD163,CD63,SA12,SA8</td>
   </tr>
   <![if supportMisalignedColumns]>
    <tr width="0" style='display:none;'/>
   <![endif]>
  </table>

```
data <- as.matrix(strsplit(marker$B_pan,split = ",")[[1]])
data <- data.frame(id=c(1:nrow(data)),data)
names(data)[2] <-name[1]
name <- names(marker)
for (i in 2:length(name)) {
  a <- as.matrix(strsplit(as.character(marker[i]),split = ",")[[1]])
  a <- data.frame(id=c(1:nrow(a)),a)
  names(a)[2] <-name[i]
  data <- merge(data,a,all = T,by="id")
}
```
