# **lex-lookup**

This script looks up lexical properties of words in text documents based on normed ratings and summarizes (and, if wanted, analyzes) them across documents and any other variables (continuous or categorical). Technically, some calculated variables are not entirely lexical (e.g., sentiment), but I couldn't think of a better name. *Problem for future me, I guess.*

The norms that are currently included are:

* Brysbaert, M., Mandera, P., McCormick, S. F., & Keuleers, E. (2019). Word prevalence norms for 62,000 English lemmas. *Behavior Research Methods*, *51*, 467-479. [https://doi.org/10.3758/s13428-018-1077-9](https://doi.org/10.3758/s13428-018-1077-9){target="_blank"}
* Brysbaert, M., Warriner, A. B., & Kuperman, V. (2014). Concreteness ratings for 40 thousand generally known English word lemmas. *Behavior Research Methods*, *46*, 904-911. [https://doi.org/10.3758/s13428-013-0403-5](https://doi.org/10.3758/s13428-013-0403-5){target="_blank"}
* Clark, J. M., & Paivio, A. (2004). Extensions of the Paivio, Yuille, and Madigan (1968) norms. *Behavior Research Methods, Instruments, & Computers*, *36*(3), 371-383. [https://doi.org/10.3758/bf03195584](https://doi.org/10.3758/bf03195584){target="_blank"}
* Diveica, V., Pexman, P. M., & Binney, R. J. (2022). Quantifying social semantics: An inclusive definition of socialness and ratings for 8388 English words. *Behavior Research Methods*, 1-13. [https://doi.org/10.3758/s13428-022-01810-x](https://doi.org/10.3758/s13428-022-01810-x){target="_blank"}
* Kuperman, V., Stadthagen-Gonzalez, H., & Brysbaert, M. (2012). Age-of-acquisition ratings for 30,000 English words. *Behavior Research Methods*, *44*, 978-990. [https://doi.org/10.3758/s13428-012-0210-4](https://doi.org/10.3758/s13428-012-0210-4){target="_blank"}


## **Gettting Started**

[Fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo) and [clone](https://docs.github.com/en/get-started/quickstart/fork-a-repo#cloning-your-forked-repository) this repository to get a copy of this project locally on your machine.


## **Installation**

The first chunk in the script uses the `pacman` package to download any necessary packages that are not currently installed. As such, `pacman` needs to be installed for this to run (`install.packages("pacman")`). 


## **Usage**

Text data (and any associated variables of interest) should be included in a CSV file in the `data` folder. Make sure the `Import Data` chunk in the script points to that file.

Data should include a column named `text` and each document should be assigned a unique identifier in a column named `doc_id`. 

If in doubt, check the example `text_data.csv` file provided. Example texts are excerpts from Proust's *In Search of Lost Time* (1913-1927/1992) and James's *The Principles of Psychology* (1890), because it turns out I'm a very predictable person (and also because the books are in the public domain now, but mostly the former).


## **Contributing**

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


## **Authors and Acknowledgment**

Author: [Ryan Yeung](https://ryancyeung.github.io)

Adapted from [Make a README](https://www.makeareadme.com/) template and [Best-README-Template](https://github.com/othneildrew/Best-README-Template).


## **License**

Distributed under the [GNU GPLv3](https://www.gnu.org/licenses/gpl-3.0.en.html) license. See `LICENSE` for more information.