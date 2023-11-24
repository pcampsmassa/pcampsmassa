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


