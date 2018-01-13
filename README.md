# PAG_2018
Interactive genome exploration. Poster examples.

In this repo you will find the code and data to reproduce the examples in Fig. 3 of the poster i presented at PAG 2018.

The web application created allows you to explore key details of variation extracted from the selected regions:

## App features

Cluster observations (graph): Principal component analysis of clusters extracted. Colors derive from a simple kmeans clustering at K == 9.

Likelihood density (graph): density plot of mean likelihood of each accessions for clusters of a given color.

Accessions - loadings (graph): Loadings plot of the above PCA. Reveals overall relationships between accessions given the clusters selected for this analysis. color-code: Blue= Japonica; yellow= circumAus; red= Indica; purple= Admix; green= cBasmati.

Selected accessions (table): Information on either all 948 CORE accessions included (select Full-colors in "Chose a color" dropdown), or those above a certain threshold when focusing on a particular cluster (select color "Chose a color", modulate threshold likelihood using slider).

## Use
**Online:**

Visit the [Application](https://pag18-plots.herokuapp.com/) hosted on Heroku servers.

**Offline:**
Because heroku servers have a limited number of dynos, the application can get crowded.
You will still need an internet connection to load the layout, but you will be runninng it locally.

Just run the script app.py, e.g. '$python app.py'

  Select a color in "Chose a color" dropdown: these refer to colors in "Cluster observations". A density plot of mean likelihood by accession across these clusters is drawn. Accessions whose mean exceeds the threshold in the above slider now appear in red in "Accessions - loadings", detailed information about them in the "selected accessions" table.
  
  Explore!

# python modules required (from dash-plotly):

pip install dash==0.19.0  # The core dash backend;
pip install dash-renderer==0.11.1  # The dash front-end;
pip install dash-html-components==0.8.0  # HTML components;
pip install dash-core-components==0.14.0  # Supercharged components;
pip install plotly --upgrade  # Plotly graphing library used in examples;
pip install pandas  # library for working with data;

