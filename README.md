# PMSSpopularity
Spatial Popularity of Artists Sam Smith and Post Malone
https://heatherlynn97.github.io/PMSSpopularity/

This should show up on my website


<iframe src="https://open.spotify.com/embed/user/spotify/playlist/37i9dQZF1DX29brXfjEm5q" width="300" height="380" frameborder="0" allowtransparency="true"></iframe>

<iframe src="https://open.spotify.com/embed/user/spotify/playlist/37i9dQZF1DZ06evO1aBeik" width="300" height="380" frameborder="0" allowtransparency="true"></iframe>


<iframe width="100%" height="520" frameborder="0" src="https://heatherlynn97.carto.com/builder/03947126-a364-43b7-8389-598c8365b91a/embed" allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>

```{r include=FALSE}

ssTopCities <- read_csv("https://raw.githubusercontent.com/heatherlynn97/PMSSpopularity/master/SS_topcities.csv")
pmTopCities <- read_csv("https://raw.githubusercontent.com/heatherlynn97/PMSSpopularity/master/PM_topcities.csv")
```

```{r echo=FALSE}
SamSmithCities <-
hchart(ssTopCities, "column", hcaes(x = TopCity, y = Listeners, color = Country))%>%
  hc_add_theme(hc_theme_flat()) %>%
  hc_title(text = 'Top 5 Sam Smith Listening Cities', style = list(fontSize = "20px")) 

SamSmithCities
```

```{r echo=FALSE}
PostMCities <-
hchart(pmTopCities, "column", hcaes(x = TopCity, y = Listeners, color = Country)) %>%
  hc_add_theme(hc_theme_flat()) %>%
  hc_title(text = 'Top 5 Post Malone Listening Cities', style = list(fontSize = "20px"))

PostMCities
```



