# A Lightweight Conditional Random Field

This is a modern Python library without any third-party dependencies and a backend written in C implementing conditional random fields for natural language processing tasks like named entity recognition or part-of-speech tagging.

You can install the latest stable version from [PyPI](https://pypi.org/project/chaine):

```
$ pip install chaine
```

If you are interested in the theoretical concepts behind conditional random fields, I can recommend the introducing paper by [Lafferty et al](https://repository.upenn.edu/cgi/viewcontent.cgi?article=1162&context=cis_papers).


## Example

```python
>>> import chaine
>>> crf = chaine.train(sequence, labels, max_iterations=100)
>>> crf.predict(sequence)
["B-PER", "I-PER", "O", "O"]
```

Check out the introducing [Jupyter notebook](https://github.com/severinsimmler/chaine/blob/master/notebooks/tutorial.ipynb).


## Disclaimer

This library makes use of and is partially based on:

- [CRFsuite](https://github.com/chokkan/crfsuite)
- [libLBFGS](https://github.com/chokkan/liblbfgs)
- [python-crfsuite](https://github.com/scrapinghub/python-crfsuite)
- [sklearn-crfsuite](https://github.com/TeamHG-Memex/sklearn-crfsuite)