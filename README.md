# SCAPE - Semantically Context-Aware Password Generation using Word Embeddings

## About
Password guessing is a fundamental activity of cybersecurity specialists. Being able to effectively guess passwords has profound implications for IT forensics and IT security. In this study, we propose and evaluate a novel password-guessing method, SCAPE. 

We extend existing Probabilistic Context-Free Grammar (PCFG)-based approaches by adding context awareness by means of word embeddings. Leveraging real-world datasets, including a subset of the RockYou leak and leaks from topical forums, we compare SCAPE with state-of-the-art methods like PCFG, OMEN, and SemanticPCFG. Our experiments demonstrate that SCAPE outperforms existing methods, achieving higher hit rates and efficiency. Furthermore, we analyze the influence of different word embeddings and the number of neighbors on method performance to find optimal configurations. These findings highlight the effectiveness of SCAPE in password guessing, offering promising avenues for real-world applications in cybersecurity.

----

## Installation + Requirements
This tool is based on the PCFG Cracker by Weir et al. [GitHub](https://github.com/lakiw/pcfg_cracker)

Before downloading our tool you need Python3(.10) installed on your machine.
All package requirements are listed in the requirements.txt file.

Note: Windows users might have problems installing fasttext, as this is only tailored to Linux and Unix systems (according to their [webseite](https://fasttext.cc/docs/en/support.html)
Use [this link](https://www.lfd.uci.edu/~gohlke/pythonlibs/#fasttext) or [this link](https://pypi.tuna.tsinghua.edu.cn/simple/gensim/) to find and download the correct wheel file for you system and restart your programm.
We included our used version in this git, you can locally install it by using pip.

## Quick Start Guide
After downloading and installing all requirements, simply execute the 'executeSCAPE.py' file.
This file calls the two subprocesses to first run the PCFG trainer with all necessary parameters. 
You might want to adjust the parameters before executing the (sub)processes.

Trainer:
* t: input data - the path to the training data list
* c: parameter to adjust OMEN vs PCFG generation strength
* r: name of the rule set to be created 
* m: word embedding to semantically enhance the list (i.e. Glove Twitter 200)
* l: max length (required for OMEN)
* k: the number of nearest neighbors in the embedding - best chosen between 100-500
* n: ngram (required for OMEN) 

Guesser:
* s: Session saved TBC
* r: name of the rule set to be used in creation
* n: number of password candidates the programm will create

## Known Issues

* Installation problems on Windows (WIP)

## Contact

TBA