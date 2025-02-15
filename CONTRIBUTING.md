## Help us to help you!

Thank you for taking the time to contribute!

* [Suggesting a feature](#suggesting-a-feature)
* [Filing a bug report](#filing-a-bug-report)
* [Submitting a pull request](#submitting-a-pull-request)

## Suggesting a feature

We can't think of everything. If you've got a good idea for a feature, then please let us know!

Feature suggestions are embraced, but will often be filed for a rainy day. If you require a feature urgently it's best to write it yourself. Don't forget to share ;)

When suggesting a feature, make sure to:

* Check the code on repo to make sure it's not already hiding in an unreleased version ;)
* Considered if it's necessary in the library, or is an advanced technique that could be separately explained in an example
* Check existing issues, open and closed, to make sure it hasn't already been suggested

## Filing a bug report

If you're having trouble with `aydin`, reach us please.

Be as detailed as possible, and be ready to answer questions when we get back to you. Make sure you:

* Tell us which OS you're using
* List the steps you've taken so far,
* and any solutions you've tried
* And a paste/picture of the complete output from the fail might help, too!

## Submitting a pull request

If you've decided to fix a bug, even something as small as a single-letter typo then great! Anything that improves the code/documentation for all future users is warmly welcomed.

If you decide to work on a  requested feature it's best to let us (and everyone else) know what you're working on to avoid any duplciation of effort. You can do this by replying to the original Issue for the request.

When contributing a new example or making a change to a library please keep your code style consistent with ours. We try to stick to the pep8 guidelines for Python (https://www.python.org/dev/peps/pep-0008/).

### Submitting your code

Once you're ready to share your contribution with us you should submit it as a Pull Request.

* Be ready to receive and embrace constructive feedback.
* Be prepared for rejection; we can't always accept contributions. If you're unsure, ask first!

1. First, start with a new branch on your fork from the target branch
2. Submit changes to new branch of your fork
3. Wait for the review and merge.
4. Upon merge make sure you fetch upstream and update your master branch.

#### Do

* Do use pep8 style guidelines + our preferences with `black` formatter
* Use NumPy style docstrings
* Do comment your code where necessary
* Do submit only a single example/feature per pull-request
* Do include a description of what your example is expected to do
* Do add details of your example to README.md and CONTRIBUTING.md if it is needed

#### Don't

* Don't include any license information in your examples- our repositories are GPLv3 licensed
* Don't try to do too much at once- submit one or two examples at a time, and be receptive to feedback
* Don't submit multiple variations of the same example, demonstrate one thing concisely

#### How to setup development environment:

```bash
# Create a new environment
conda create -n aydin_env python=3.9

# Activate the environment
conda activate aydin_env

# Install Aydin
pip install -e .

# Install development specific dependencies
pip install -r requirements/development.txt

# Install pre-commit hooks
pre-commit install

# Before making a PR make sure tests are passing
# To run tests
python -m pytest . --disable-pytest-warnings

# Before making a PR also check if your branch
# passes style guidelines
black --check -S -t py36 .
flake8 --ignore E501,E203,E741,W503 aydin
```

##### For PyCharm users:

Go to `Settings | Tools | Python Integrated Tools | Docstring format`
and change it to `NumPy` style. So autogenerated docstrings will be 
in correct styling.


### Licensing

When you submit code to our libraries, you implicitly and irrevocably agree to adopt the associated licenses. 
You should be able to find this in the file named `LICENSE.txt`.

We use the BSD 3-Clause License.

## Thank you!

If you have any questions, concerns or comments about these guidelines, please get in touch.

Above all else, we hope you enjoy yourself, learn things and make and share great contributions.

Happy hacking!

-- `aydin` team
