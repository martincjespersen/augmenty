<a href="https://github.com/kennethenevoldsen/augmenty"><img src="https://github.com/KennethEnevoldsen/augmenty/blob/master/img/icon.png?raw=true" width="200" align="right" /></a>
# Augmenty: The cherry on top of your NLP pipeline

[![PyPI version](https://badge.fury.io/py/augmenty.svg)](https://pypi.org/project/augmenty/)
[![pip downloads](https://img.shields.io/pypi/dm/augmenty.svg)](https://pypi.org/project/augmenty/)
[![python version](https://img.shields.io/badge/Python-%3E=3.7-blue)](https://github.com/kennethenevoldsen/augmenty)
[![Code style: black](https://img.shields.io/badge/Code%20Style-Black-black)](https://black.readthedocs.io/en/stable/the_black_code_style/current_style.html)
[![spacy](https://img.shields.io/badge/built%20with-spaCy-09a3d5.svg)](https://spacy.io)
[![github actions pytest](https://github.com/kennethenevoldsen/augmenty/actions/workflows/pytest-cov-comment.yml/badge.svg)](https://github.com/kennethenevoldsen/augmenty/actions)
[![github actions docs](https://github.com/kennethenevoldsen/augmenty/actions/workflows/documentation.yml/badge.svg)](https://kennethenevoldsen.github.io/augmenty/)
![github coverage](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/KennethEnevoldsen/2d5c14e682c3560240fe05cc7c9f4d2d/raw/badge-augmenty-pytest-coverage.json)
[![CodeFactor](https://www.codefactor.io/repository/github/kennethenevoldsen/augmenty/badge)](https://www.codefactor.io/repository/github/kennethenevoldsen/augmenty)
<!-- [![Demo](https://img.shields.io/badge/Try%20the-Demo-important)](https://huggingface.co/chcaa/da_augmenty_medium_trf?text=augmenty+er+en+pipeline+til+anvendelse+af+dansk+sprogteknologi+lavet+af+K.+Enevoldsen%2C+L.+Hansen+og+K.+Nielbo+fra+Center+for+Humanities+Computing.) -->


Augmenty is an augmentation library based on spaCy for augmenting texts. Besides a wide array of highly flexible augmenters, Augmenty provides a series of tools for working with augmenters, including combining and moderating augmenters. Augmenty differs from other augmentation libraries in that it corrects (as far as possible) the assigned labels under the augmentation, thus making many of the augmenters valid for training more than simply sentence classification.

## 🔧 Installation
To get started using augmenty simply install it using pip by running the following line in your terminal:

```
pip install augmenty
```

Do note that this is a minimal installation. As some augmenters requires additional packages please the following line to install all dependencies.

```
pip install augmenty[all]
```

For more detailed instructions on installing augmenty, including specific language support, see the [installation instructions](https://kennethenevoldsen.github.io/augmenty/installation).

## 📖 Documentation

| Documentation              |                                                                              |
| -------------------------- | ---------------------------------------------------------------------------- |
| 📚 **[Usage Guides]**      | Guides and instruction on how to use augmenty and its features.              |
| 🍒 **[Augmenters]** | Contains a full list of current and planned augmenters in augmenty.         |
| 📰 **[News and changelog]** | New additions, changes and version history.                                 | 
| 🎛 **[API Reference]**      | The detailed reference for augmenty's API. Including function documentation |

<!-- | ⭐️ **[augmenty 101]**        | New to spaCy? Here's everything you need to know!              | -->

[usage guides]: https://kennethenevoldsen.github.io/augmenty/
[api reference]: https://kennethenevoldsen.github.io/augmenty/
[Augmenters]: https://kennethenevoldsen.github.io/augmenty/
[News and changelog]: https://kennethenevoldsen.github.io/augmenty/
[List of augmenters]: https://github.com/kennethenevoldsen/augmenty/augmenters.md

## 💬 Where to ask questions

| Type                            |                                 |
| ------------------------------- | --------------------------------------- |
| 🚨 **Bug Reports**              | [GitHub Issue Tracker]                  |
| 🎁 **Feature Requests & Ideas** | [GitHub Issue Tracker]                  |
| 👩‍💻 **Usage Questions**          | [GitHub Discussions]                    |
| 🗯 **General Discussion**       | [GitHub Discussions]                    |
| 🍒 **Adding an Augmenter**       | [Adding an augmenter]                    |

[github issue tracker]: https://github.com/kennethenevoldsen/augmenty/issues
[github discussions]: https://github.com/kennethenevoldsen/augmenty/discussions
[Adding an augmenter]: https://github.com/kennethenevoldsen/augmenty/discussions


## 🤔 FAQ


<details>
  <summary>How do I test the code and run the test suite?</summary>


augmenty comes with an extensive test suite. In order to run the tests, you'll usually want to clone the repository and build augmenty from the source. This will also install the required development dependencies and test utilities defined in the requirements.txt.


```
pip install -r requirements.txt
pip install pytest

python -m pytest
```

which will run all the test in the `augmenty/tests` folder.

Specific tests can be run using:

```
python -m pytest augmenty/tests/test_readability.py
```

**Code Coverage**
If you want to check code coverage you can run the following:
```
pip install pytest-cov

python -m pytest--cov=.
```


</details>


<br /> 


<details>
  <summary>Does augmenty run on X?</summary>

  augmenty is intended to run on all major OS, this includes Windows (latest version), MacOS (Catalina) and the latest version of Linux (Ubuntu). Below you can see if augmenty passes its test suite for the system of interest. Please note these are only the systems augmenty is being actively tested on, if you run on a similar system (e.g. an earlier version of Linux) augmenty will likely run there as well, if not please create an issue.

| Operating System | Status                                                                                                                                                                                                                  |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Ubuntu/Linux (Latest)  | [![github actions pytest ubuntu](https://github.com/kennethenevoldsen/augmenty/actions/workflows/pytest-cov-comment.yml/badge.svg)](https://github.com/kennethenevoldsen/augmenty/actions/workflows/pytest-cov-comment.yml)     |
| MacOS (Catalina) | [![github actions pytest catalina](https://github.com/kennethenevoldsen/augmenty/actions/workflows/pytest_mac_catalina.yml/badge.svg)](https://github.com/kennethenevoldsen/augmenty/actions/workflows/pytest_mac_catalina.yml) |
| Windows (Latest) | [![github actions pytest windows](https://github.com/kennethenevoldsen/augmenty/actions/workflows/pytest_windows.yml/badge.svg)](https://github.com/kennethenevoldsen/augmenty/actions/workflows/pytest_windows.yml)            |

  
</details>

<br /> 

<details>
  <summary>How is the documentation generated?</summary>

  augmenty uses [sphinx](https://www.sphinx-doc.org/en/master/index.html) to generate documentation. It uses the [Furo](https://github.com/pradyunsg/furo) theme with a custom styling.

  To make the documentation you can run:
  
  ```
  # install sphinx, themes and extensions
  pip install sphinx furo sphinx-copybutton sphinxext-opengraph

  # generate html from documentations

  make -C docs html
  ```
  
</details>


<br /> 

<details>
  <summary>Many of these augmenters are completely useless for training?</summary>

  That is true, some of the augmenters are rarely something you would augment with during training. For instance randomly adding or removing spacing. However, augmentation can just as well be used to test whether a model is robust to certain variations.
  
</details>

<br /> 



<br /> 

<details>
  <summary>Can I use augmenty without using spacy?</summary>

  Indeed augmenty contains convenience functions for applying augmentation directly to raw texts. Check out the [getting started guide](https://kennethenevoldsen.github.io/augmenty/introduction.html) to learn how. 
  
</details>

<br /> 


### 🎓 Citing this work

If you use this library in your research, please cite:

```bibtex
@inproceedings{augmenty2021,
    title={Augmenty, the cherry on top of your NLP pipeline},
    author={Enevoldsen, Kenneth and Hansen, Lasse},
    year={2021}
}
```
