# PMSSpopularity
Spatial Popularity of Artists Sam Smith and Post Malone
https://heatherlynn97.github.io/PMSSpopularity/

This should show up on my website
<iframe width="100%" height="520" frameborder="0" src="https://heatherlynn97.carto.com/builder/03947126-a364-43b7-8389-598c8365b91a/embed" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

```{r}

ssTopCities <- read_csv("~/Downloads/SS_topcities.csv")
pmTopCities <- read_csv("~/Downloads/PM_topcities.csv")
```

```{r}
hchart(ssTopCities, "column", hcaes(x = TopCity, y = Listeners, color = Country))%>%
  hc_add_theme(hc_theme_flat()) %>%
  hc_title(text = 'Top 5 Sam Smith Listening Cities', style = list(fontSize = "20px"))

```
