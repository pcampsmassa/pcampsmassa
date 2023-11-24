# PECA
## Grafic model lineal
```
setwd("D:/PROYECTOS/PECA/ABSTRACT SEPAR 2024")
```


### CD73 esputo - Eosinofilia
```
prova1 <- ggplot(metadata_R_PECA_modificado, aes(x = Eos, y = sputum_CD73, color = Fase)) +
geom_point(size=2) + 
scale_y_continuous(name=expression(Sputum~CD73),limits=c(0,1500))+
scale_x_continuous(name=expression(Eos),limits=c(0,500))+
geom_labelsmooth(aes(label = Fase),
  method = "lm", formula = y ~ x,
  size = 3, linewidth = 1, boxlinewidth = 0.4) +
theme_bw() + guides(color = 'none')
```
```
ggsave(plot=prova1,"sputumCD73_Eos_lineal.svg", width = 20, height = 15, units = "cm")
```
![image](https://github.com/pcampsmassa/pcampsmassa/assets/144921804/bab644c9-16b3-4b80-9d36-e58730a3f93a)



### CD73 suero - Eosinofilia
```
prova2 <- ggplot(metadata_R_PECA_modificado, aes(x = Eos, y = serum_CD73, color = Fase)) +
geom_point(size=2) + 
scale_y_continuous(name=expression(Serum~CD73),limits=c(0,6000))+
scale_x_continuous(name=expression(Eos),limits=c(0,450))+
geom_labelsmooth(aes(label = Fase),
 method = "lm", formula = y ~ x,
 size = 3, linewidth = 1, boxlinewidth = 0.4) +
theme_bw() + guides(color = 'none')
```
```
ggsave(plot=prova2,"serumCD73_Eos_lineal.svg", width = 20, height = 15, units = "cm")
```
![image](https://github.com/pcampsmassa/pcampsmassa/assets/144921804/6d60dbfe-9970-415a-9878-a83722a3c161)

## Boxplot per grups amb puntets de colors per variable

### IL4 depenent de Eos150 diferenciat per grups
```
boxplot_IL4 <- ggplot(metadata_R_PECA_modificado,aes(x=Eos150,y=`IL-4`,fill=Eos150))+geom_boxplot(outlier.shape = NA)+
    scale_y_continuous(name=expression(IL-4),limits=c(0,50))+
    scale_x_discrete(name=expression(""),labels=c(expression("<150 eosinophils"),expression(">150 eosinophils")))+
    geom_jitter(position=position_jitter(0.3),size=3,aes(colour=Fase))+
    scale_fill_manual(name=c(""),values=c("#ffffff","#ffffff"),labels=c(expression("<150 eosinophils"),expression(">150 eosinophils")))+  scale_colour_manual(name="Fase",values=c("#FB4D3D","#FAC748","#2D93AD"),labels=c("EPOC aguditzador","EPOC estable","EPOC no aguditzador"))+ theme(panel.background = element_rect(fill ="#ffffff"))+
    theme(panel.border = element_rect(fill = "transparent", color = 1, linewidth = 1))+
    theme(plot.background = element_rect(fill = "#FFFFFF")); boxplot_IL4
```
![image](https://github.com/pcampsmassa/pcampsmassa/assets/144921804/a50f8c4e-d4b2-4226-a37b-5845c4fc01b3)
