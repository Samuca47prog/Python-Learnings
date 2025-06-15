# 7 Tips To Structure Your Python Data Science Projects

- [ ] Use a commom structure
- [ ] Use existing libraries
- [ ] Log your results
- [ ] Use intermediate data representations
- [ ] Move reusable code to a shared package
- [ ] Move configuration settings out of the code
- [ ] Write unit tests


## 1. Use a commom structure for your projects

You might have many data projects going on at the same time.
Switching context makes you be less productive.

Having a commom structure at least reduces the effort to switch contexts.

[Coockiecutter](https://www.cookiecutter.io/) helps creating the structure.

Scpecifically for data science, there is [**Cookiecutter Data Science**](https://cookiecutter-data-science.drivendata.org/)

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see www.mkdocs.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for 
│                         {{ cookiecutter.module_name }} and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
```

## 2. Use existing libraries as much as possible

**USE LIBRARIES AS MUCH AS POSSIBLE**

Libs are better tested

Learn from the libs, read the docs, understand what are behind the functions.

Examples:
* scikit-learn
* PyTorch
* SQLAlchemy

## 3. Log your results

Log the various outputs

Examples:
* Log files
* Log servers

## 4. Use intermediate data representations

Do preprossecing, formatting, filters, results.

Don't be afraid to separate the steps.

CSV and JSON are good to share with humans.
But if query is needed, SQL is better
Data frames

> What data formats the code use?

## 5. Move reusable code to a shared package

Use imports inside Jupiter notebooks

## 6. Move configuration settings out of the code

settings outside of the code, or at worst in a single place.

Values, constants.

Use env variables

## 7. Write unit tests

