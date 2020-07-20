# BIOME-z-Project

TODO: Write project summary/notes/howto here.

## Meetings 

Prior to each meeting, make a note under each goal with your name/handle/initials and a note about what you did or worked on to address that goal

### 7/20/2020
- When using CUDA through pytorch in hpcl, run on a workstation:
CUDA is deployed to the HPCL. I believe installing PyTorch with pip's --user flag should work, but if they run into trouble that way I can deploy it to the system image. All of the workstations have GPUs in them. hpcl1-[1-5] and hpcl[2-5]-[1-6] have workstation cards in them, and hpcl6-[1-4] have a standard graphics card in them. I haven't done any performance tests between the two cards so I don't really have any advice on which to choose.

SSH is working between hslinux and all of the cluster machines, the hostnames are:

hpcl1-1.salisbury.edu
hpcl1-2.salisbury.edu
hpcl1-3.salisbury.edu
hpcl1-4.salisbury.edu
hpcl1-5.salisbury.edu
hpcl2-1.salisbury.edu
hpcl2-2.salisbury.edu
hpcl2-3.salisbury.edu
hpcl2-4.salisbury.edu
hpcl2-5.salisbury.edu
hpcl2-6.salisbury.edu
hpcl3-1.salisbury.edu
hpcl3-2.salisbury.edu
hpcl3-3.salisbury.edu
hpcl3-4.salisbury.edu
hpcl3-5.salisbury.edu
hpcl3-6.salisbury.edu
hpcl4-1.salisbury.edu
hpcl4-2.salisbury.edu
hpcl4-3.salisbury.edu
hpcl4-4.salisbury.edu
hpcl4-5.salisbury.edu
hpcl4-6.salisbury.edu
hpcl5-1.salisbury.edu
hpcl5-2.salisbury.edu
hpcl5-3.salisbury.edu
hpcl5-4.salisbury.edu
hpcl5-5.salisbury.edu
hpcl5-6.salisbury.edu
hpcl6-1.salisbury.edu
hpcl6-2.salisbury.edu
hpcl6-3.salisbury.edu
hpcl6-4.salisbury.edu


### 7/13/2020
- Work with different hyperparameters (batch size, dimensions, n-grams, etc.) to see different training/testing performance
- Start thinking about poster format and content

### 6/29/2020
- Load data with TorchText
- Experiment with different learning rates, optimizes, other hyperparameters
  - Account for different testing, training, and validation datasets
- Start data training and testing framework for BIOMEz data

### 6/15/2020
- Next steps: integrate RDF-pulled data into text-classification framework demonstrated in [https://pytorch.org/tutorials/beginner/text_sentiment_ngrams_tutorial.html](https://pytorch.org/tutorials/beginner/text_sentiment_ngrams_tutorial.html).
  - D.S: Created a .py file using the above tutorial. Wrote down a bunch of comments reflecting how we would setup our text classification with respect to our dataset.
- In addition to abstract text, use the article tags/subjects/keyword as well (remove "correct" ones before training).
- Start with "top-level" tags first.

### 6/8/2020
- When parsing RDF, sub-collection is captured by "foreign-key" style within the RDF (collections have a "hasPart" with collection id of subcollection)
- Dr. Maier will be heading the conversion to hyphenated tags within the BIOMEz library
- **Goals**
  - Upload notes, code, comments to repository for future discussion
    - D.S: Added another pytorch neural network for *convolutional* datasets - different type of dataset processing, but explores different functions in Pytorch nonetheless.
  - Continue to data imported from `.rdf` file working into python objects, capture structure. Start getting into pytorch data format.
    - D.S: Jack & I are considering only using the abstract text as input data for Pytorch.

### 6/1/2020
- Data flow: RDF format -> Python objects -> PyTorch classifier -> RDF format to organize
  - RDF parsing library: [https://rdflib.readthedocs.io/en/stable/index.html](https://rdflib.readthedocs.io/en/stable/index.html)
  - Python bibtex library: [https://bibtexparser.readthedocs.io/en/master](https://bibtexparser.readthedocs.io/en/master)
- Data labeling changes (in future): move from "Biological Distal Psychological Intermediate" to "Biological-Distal Psychological-Intermediate" tag format
- Existing library uploaded as `BIOMEz.rdf`
  - The ADMIN ONLY... folder is unclassified articles
- **Goals**
  - Get data import from `.rdf` file working into python objects
  - Begin finding data format requirements for PyTorch
