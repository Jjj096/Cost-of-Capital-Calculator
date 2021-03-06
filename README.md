# Cost-of-Capital-Calculator
Cost-of-Capital-Calculator is a model that can be used to evaluate the effect of US federal taxes on the investment incentives of corporate and non-corporate businesses.  Specifically, Cost-of-Capital-Calculator uses data on the business assets and financial policy, as well as microdata on individual tax filers, to compute marginal effective tax rates on new investments.  In modeling the effects of changes to the individual income tax code, Cost-of-Capital-Calculator works with [Tax-Calculator](https://github.com/open-source-economics/tax-calculator), another open source model of US federal tax policy.  Cost-of-Capital-Calculator is written in Python, an interpreted language that can execute on Windows, Mac, or Linux.

## Disclaimer
Results will change as the underlying models improve. A fundamental reason for adopting open source methods in this project is so that people from all backgrounds can contribute to the models that our society uses to assess economic policy; when community-contributed improvements are incorporated, the model will produce different results.


## Using/contributing to Cost-of-Capital-Calculator

There are two common ways to get started with Cost-of-Capital-Calculator:

The **first way** to use Cost-of-Capital-Calculator is to download the source code and install the model on your machine.  To do this, follow the following instructions:
* Install the [Anaconda distribution](https://www.anaconda.com/distribution/) of Python
* Clone this repository to a directory on your computer
* From the terminal (or Conda command prompt), navigate to the directory to which you cloned this repository and run `conda env create -f environment.yml`
* Then, `source activate ccc-dev` (or `activate ccc-dev` if using a Windows machine)
* Then install by `pip install -e .`
* Navigate to `./run_examples`
* Run the model with an example reform from terminal/command prompt by typing `python run_ccc_example.py`
* You can adjust the `./run_examples/run_ccc_example.py` by adjusting the individual income tax reform (using a dictionary or JSON file in a format that is consistent with [Tax Calculator](https://github.com/open-source-economics/Tax-Calculator)) or other model parameters specified in the `business_tax_adjustments` dictionary.
* Model outputs will be saved in the following files:
  * `./run_examples/baseline_byasset.csv`
    * Cost of capital, marginal effective tax rates, effective average tax rates, and other model output for the baseline policy, organized by asset.
  * `./run_examples/baseline_byindustry.csv`
    * Cost of capital, marginal effective tax rates, effective average tax rates, and other model output for the baseline policy, organized by production industry.
  * `./run_examples/reform_byasset.csv`
    * Cost of capital, marginal effective tax rates, effective average tax rates, and other model output for the reform policy, organized by asset.
  * `./run_examples/reform_byindustry.csv`
    * Cost of capital, marginal effective tax rates, effective average tax rates, and other model output for the refrom policy, organized by production industry.
  * `./run_examples/changed_byasset.csv`
    * Differences in cost of capital, marginal effective tax rates, effective average tax rates, and other model output between the baseline and reform reform policies, organized by asset.
  * `./run_examples/changed_byindustry.csv`
    * Differences in cost of capital, marginal effective tax rates, effective average tax rates, and other model output between the baseline and reform reform policies, organized by production industry.

The CSV output files can be compared to the `./run_examples/*_expected.csv` files that are checked into the repository to confirm that you are generating the expected output.  If you run into errors running the example script, please open a new issue in the Cost-of-Capital-Calculator repo with a description of the issue and any relevant tracebacks you receive.


The **second way** to use Cost-of-Capital-Calculator is through a web
application, [Cost of Capital Calculator](http://www.ospc.org/ccc).  This way
allows you to generate estimates of marginal effective tax rates and the cost of capital
across production industries, type of asset, and separately for corporate and non-corporate
entites and different forms of financing.  The web application is limited in that you cannot consider policy reforms to the individual income tax code.

Of course, you can get started with Cost-of-Capital-Calculator both ways.

## Citing the Cost-of-Capital-Calculator Model
Cost-of-Capital-Calculator (Version 0.1.5)[Source code], https://github.com/open-source-economics/Cost-of-Capital-Calculator
