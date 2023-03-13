# **lex-lookup**

[![DOI](https://zenodo.org/badge/607434376.svg)](https://zenodo.org/badge/latestdoi/607434376)

This R script (`lex-lookup.qmd`) looks up lexical properties of words in text documents based on normed ratings, and then summarizes (and, if wanted, analyzes) them across documents or any other variables of interest (either continuous or categorical). Technically, some calculated variables are not entirely lexical (e.g., sentiment), but I couldn't think of a better name. *Problem for future me, I guess.*

Texts are parsed using `{udpipe}`[^wijffels2023].

The norms that are currently included are:

* age of acquisition (Kuperman et al., 2012)[^kuperman2012]
* assorted norms from Clark & Paivio (2004)[^clarkpaivio2004], too many to list here
* concreteness (Brysbaert et al., 2014)[^brysbaert2014]
* socialness (Diveica et al., 2022)[^diveica2022]
* word frequency (Brysbaert & New, 2009)[^brysbaertnew2009]
* word prevalence (Brysbaert et al., 2019)[^brysbaert2019]

Calculated variables include:

* number of syllables (Benoit, 2022)[^benoit2022]
* document length (number of words)
* sentence length (number of words)
* sentiment (Rinker, 2021)[^rinker2021]
* word length (number of characters)

For a full demo, open `lex-lookup.html`.


## **Gettting Started**

[Fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo) and [clone](https://docs.github.com/en/get-started/quickstart/fork-a-repo#cloning-your-forked-repository) this repository to get a copy of this project locally on your machine.


## **Installation**

The first chunk (`setup`) in the R script uses the `pacman` package to download any necessary packages that are not currently installed. As such, `pacman` needs to be installed for the rest be installed (`install.packages("pacman")`). 


## **Usage**

Text data (and any associated variables of interest) should be included in a CSV file in the `data` folder. Make sure the `Import Data` chunk in the script points to that file.

Data should include text data in a column named `text`, and each document should be assigned a unique identifier in a column named `doc_id`. 

Associated variables of interest (e.g., grouping variables) need to be in the CSV with the text data. Make sure the script points to the new variable(s) of interest instead of the default (`author`). 

If in doubt, check the example `text_data.csv` file provided. Example texts are excerpts from Proust's *In Search of Lost Time* (1913-1927/1992)[^proust1913-1927] and James's *The Principles of Psychology* (1890)[^james1890], because it turns out I'm a very predictable person (and also because the books are in the public domain now, but mostly the former).


## **Contributing**

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


## **Authors and Acknowledgment**

Author: [Ryan Yeung](https://ryancyeung.github.io)

Adapted from [Make a README](https://www.makeareadme.com/) template and [Best-README-Template](https://github.com/othneildrew/Best-README-Template).


## **License**

Distributed under the [GNU GPLv3](https://www.gnu.org/licenses/gpl-3.0.en.html) license. See `LICENSE` for more information.


## **References**

[^benoit2022]: Benoit, K. (2022). nsyllable: Count syllables in character vectors. R package version 1.0.1, [https://CRAN.R-project.org/package=nsyllable](https://CRAN.R-project.org/package=nsyllable)
[^brysbaert2019]: Brysbaert, M., Mandera, P., McCormick, S. F., & Keuleers, E. (2019). Word prevalence norms for 62,000 English lemmas. *Behavior Research Methods*, *51*, 467-479. [https://doi.org/10.3758/s13428-018-1077-9](https://doi.org/10.3758/s13428-018-1077-9)
[^brysbaertnew2009]: Brysbaert, M., & New, B. (2009). Moving beyond Kučera and Francis: A critical evaluation of current word frequency norms and the introduction of a new and improved word frequency measure for American English. *Behavior Research Methods*, *41*(4), 977-990. [https://doi.org/10.3758/BRM.41.4.977](https://doi.org/10.3758/BRM.41.4.977)
[^brysbaert2014]: Brysbaert, M., Warriner, A. B., & Kuperman, V. (2014). Concreteness ratings for 40 thousand generally known English word lemmas. *Behavior Research Methods*, *46*, 904-911. [https://doi.org/10.3758/s13428-013-0403-5](https://doi.org/10.3758/s13428-013-0403-5)
[^clarkpaivio2004]: Clark, J. M., & Paivio, A. (2004). Extensions of the Paivio, Yuille, and Madigan (1968) norms. *Behavior Research Methods, Instruments, & Computers*, *36*(3), 371-383. [https://doi.org/10.3758/bf03195584](https://doi.org/10.3758/bf03195584)
[^diveica2022]: Diveica, V., Pexman, P. M., & Binney, R. J. (2022). Quantifying social semantics: An inclusive definition of socialness and ratings for 8388 English words. *Behavior Research Methods*, 1-13. [https://doi.org/10.3758/s13428-022-01810-x](https://doi.org/10.3758/s13428-022-01810-x)
[^james1890]: James, W. (1890). *The principles of psychology, Vol. 1.* Henry Holt and Co. [https://doi.org/10.1037/10538-000](https://doi.org/10.1037/10538-000)
[^kuperman2012]: Kuperman, V., Stadthagen-Gonzalez, H., & Brysbaert, M. (2012). Age-of-acquisition ratings for 30,000 English words. *Behavior Research Methods*, *44*, 978-990. [https://doi.org/10.3758/s13428-012-0210-4](https://doi.org/10.3758/s13428-012-0210-4)
[^proust1913-1927]: Proust, M. (1913–1927/1992). *In search of lost time.* (C. K. Scott Moncrieff, T. Kilmartin, & A. Mayor, Trans.). The Modern Library. (Original work published 1913–1927)
[^rinker2021]: Rinker, T. W. (2021). sentimentr: Calculate text polarity sentiment. Version 2.9.1. [https://github.com/trinker/sentimentr](https://github.com/trinker/sentimentr)
[^wijffels2023]: Wijffels, J. (2023). udpipe: Tokenization, Parts of Speech Tagging, Lemmatization and Dependency Parsing with the UDPipe NLP Toolkit. R package version 0.8.11. [https://CRAN.R-project.org/package=udpipe](https://CRAN.R-project.org/package=udpipe)