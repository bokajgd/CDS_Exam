# Introduction to Cultural Data Science - Analysing Højskolesangbogen

 
# Overview 

**Jakob Grøhn Damgaard, Januray 2021** <br/>
This repository contains the full exam project for the course Introduction Cultural Data Science at the Faculty of Arts at Aarhus University.  

## Project Abstract
Comprising more than 600 songs and hymns, the Danish Højskolesangbog could provide a fruitful insight into the historic evolution of Danish song culture. However, in order to perform robust quantitative research on this data using modern language processing techniques a digital, tidy data set must be available.  As this is currently not the case, this study aims to assemble a digital corpus of the songs by web scraping højskolesangbogen.dk. This data set is then utilized to analyse and visualise the historic development in the use of religious language in the songs. The study concludes that there has been a general decline in the frequency of words tied to Christianity, however, with a few notable offshoots.

## Animation of development in use of religious language
 ![](interval_plot.gif)

# Software
All data operations were performed on a 2020 MacBook Pro 13’’, 2 GHz Quad-Core Intel Core i5, 16 GB Ram running macOS Catalina (10.15.6). <br/>
Following software was used: 
<br/><br/>
1. Python (3.8.5)<br/>
2. R (4.0.02)<br/>
3. RStudio (1.3.1093)<br/>
4. Visual Studio Code (1.52.1)<br/>
5. Jupyter Extension (1.0.0) for  Visual Studio Code <br/>
<br/><br/>
Chrome extension software<br/>
1. SelectorGadget (1.1.1) <br/>
2. Link Clipper (2.4.1)
<br/>
<br/>

# Files 
<br/>This repository is structured as follows:
<br/><br/>

1. **Data** folder:<br/>
<ul>
<li>*clean_song_data_with_word_counts.csv* - CSV file containing the full, cleaned data frame outputted from the Python script</li>
<li>*song_urls.csv* - CSV file containing list of URLs linking to web pages for each individual song</li>
<li>*song_vocabulary.csv* - CSV file containing a list of all unique tokens in the song lyrics</li>
<li>*song_vocabulary.pkl* - Pickle file containing a list of all unique tokens in the song lyrics</li>
</ul>
2. **Visualisations** folder:<br/>
<ul>
</li>
<li>*aggregated_15.png* - Plot showing development in religious language use when songs have been grouped and aggregated across 15 songs</li>
<li>*aggregated_songs_15_religious_intensity.gif* - GIF showing unsmoothed development in religious 
language use when songs have been grouped and aggregated across 15 songs</li>
<li>*interval_plot.gif* - GIF showing  development in religious language use when songs have been grouped and aggregated across 6 time intervals</li>
</ul>
</li>
3. *analysing_hojskolesangbogen.ipynb* - Jupyter notebook script containing code for autmated web scraping and preprocssing of the scraped data into a tidy data set<br/>
4. *analysing_hojskolesangbogen.rmd* - RMarkdown script containing analysis and visualisations of development in religious language use <br/>
5. *requirements.txt* - TXT file containing requirements for running  *analysing_hojskolesangbogen.ipynb* script locally:
<br/>
</ul>

## Metadata
<br/>
Following metadata list provides an explanation of the columns in the full cleaned data set, *clean_song_data_with_word_counts.csv*, produced by the *analysing_hojskolesangbogen.ipynb*:

<ul>
<li>*songwriter* - This column contains the name of the primary songwriter - Type: string</li>
<li>*year_written* - This column contains the year the song was written - Type: numeric </li>
<li>*cinoiser* - This column contains the name of the primary composer - Type: string</li>
<li>*year_composed* - This column contains the year the song was composed - Type: numeric </li>
<li>*lyrics* - This column contains the song lyrics- Type: string</li>
<li>*title* - This colummn contains the song title - Type: string </li>
<li>*columns numbered 9-13326* - These columns contain words counts and each represent a unique word in the vocabulary - Type: numeric </li>
</ul>


# Execution and requirements
The RMarkdown 'analysing_hojskolesangbogen.rmd' file can be directly executed in the desktop version RStudio (1.3.1093) as long as base R (4.0.02) has been installed. All packages are installed, loaded and managed using the package manager 'pacman'. 
<br/><br/>
The 'analysing_hojskolesangbogen.ipynb' file Package requirements are found in the 'requirements.txt' file. Alternatively, the code can be executed more easily using Google Colab which means no packages have to be installed locally. This only demands that one has an active Google account. You can access the script using the following link:<br/>
https://colab.research.google.com/drive/1DggRL25M4LWOkSxmtHa7Mlqv9c010Hv0#scrollTo=dhG1vgE54K1-
<br/>

# Package and software references

Bird, S., Klein, E., & Loper, E. (2009). Natural language processing with Python: analyzing text with the natural language toolkit. " O'Reilly Media, Inc.".
<br/><br/>
Chandra, R. V., & Varanasi, B. S. (2015). Python requests essentials. Packt Publishing Ltd.
<br/><br/>
Van Rossum, G., & Drake Jr., F. L. (1995). Python Reference Manual. Centrum voor Wiskunde en Informatica Amsterdam.
<br/><br/>
R Core Team (2020). R: A language and environment for statistical computing. R Foundation for Statistical Computing, Vienna, Austria. URL https://www.R-project.org/.
<br/><br/>
Richardson, L. (2019). Beautiful Soup Documentation. 84.
<br/><br/>
Ooms, J. (2018). gifski: Highest Quality GIF Encoder. R package version 0.8.6.
https://CRAN.R-project.org/package=gifski
<br/><br/>
Pedersen, T. L. & Robinson, D. (2020). gganimate: A Grammar of Animated
Graphics. R package version 1.0.7. https://CRAN.R-project.org/package=gganimate
<br/><br/>
Pedregosa, F., Varoquaux, G., Gramfort, A., Michel, V., Thirion, B., Grisel, O., ... & Vanderplas, J. (2011). Scikit-learn: Machine learning in Python. the Journal of machine Learning research, 12, 2825-2830.
<br/><br/>
Rinker, T. W. & Kurkiewicz, D. (2017). pacman: Package Management for R. version 0.5.0.
Buffalo, New York. http://github.com/trinker/pacman
<br/><br/>
Varoquaux, G., & Grisel, O. (2009). Joblib: running python function as pipeline jobs. packages. python. org/joblib.
<br/><br/>
Walt, S. V. D., Colbert, S. C., & Varoquaux, G. (2011). The NumPy array: a structure for efficient numerical computation. Computing in science & engineering, 13(2), 22-30.
<br/><br/>
Wickham, H., Francois, R., Henry, L., & Müller, K. (2015). dplyr: A grammar of data manipulation. R package version 0.4, 3.
<br/><br/>
Wickham et al., (2019). Welcome to the tidyverse. Journal of Open Source Software,
  4(43), 1686, https://doi.org/10.21105/joss.01686
  <br/>
  
# License
Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg

