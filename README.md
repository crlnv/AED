# AED
Frequência de Altura dos personagens de sexo.


install.packages("ggplot2")
install.packages("dplyr")
library(ggplot2)
library(dplyr)

starwars



g <- ggplot(starwars, aes(x = height, colour = sex, fill = sex)) +
  geom_histogram(colour = "grey", fill = "grey", binwidth = 10) + 
  facet_grid(~sex)
freq <- g + labs(x="Altura",y="Frequência")
freq
