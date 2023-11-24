# PECA
## Grafic model lineal

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
