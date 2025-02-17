
### Càlcul de la mitjana
> Crear excels separats si volem fer anàlisi per grups
```
summary(metadataA)
summary(metadataB)
```

### Càlcul desviació estàndard
```
apply(metadata,2,sd,na.rm=TRUE)
```

### Per saber a quin working directory estem
```
getwd()
```
ens dona un *workingdirectory
i després posar-lo:
```
setwd(*workingdirectory)
```
