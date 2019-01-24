
+++
abstract = "Existing 3D surface representation approaches are unable to accurately classify pixels and their orientation lying on the boundary of an object. Thus resulting in coarse representations which usually require post-processing steps to extract 3D surface meshes. To overcome this limitation, we propose an end-to-end trainable model that directly predicts implicit surface representations of arbitrary topology by optimising a novel geometric loss function. Specifically, we propose to represent the output as an oriented level set of a continuous embedding function, and incorporate this in a deep end-to-end learning framework by introducing a variational shape inference formulation. We investigate the benefits of our approach on the task of 3D surface prediction and demonstrate its ability to produce a more accurate reconstruction compared to voxel-based representations. We further show that our model is flexible and can be applied to a variety of shape inference problems."
abstract_short = ""
authors = ["Mateusz Michalkiewicz", "**Jhony K. Pontes**", "Dominic Jack", "Mahsa Baktashmotlagh", "[Anders Eriksson](https://ando.000webhostapp.com/)"]
date = "2019-01-24"
image_preview = "headers/deeplevelsets.png"
math = true
publication_types = ["1"]
publication = "In *arXiv 2019*"
publication_short = "*arXiv 2019*"
selected = false
title = "Deep level sets: Implicit surface representations for 3D shape inference"
#url_code = ""
#url_dataset = "#"
#url_pdf = "papers/deeplevelsets.pdf"
url_arxiv = "papers/deeplevelsets_arxiv.pdf"
#url_project = "project/deep-learning/"
#url_slides = "#"
url_bibtex = "papers/deeplevelsets.html"

#[[url_custom]]
#name = "Custom Link"
#url = "https://www.example.org"

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/overview_levelsets.jpg"
#caption = "My caption :smile:"

+++
### Results
<img src="/deeplevelsets_2.png" alt="Drawing" style="width: 1000px;"/>
<img src="/deeplevelsets_1.png" alt="Drawing" style="width: 1000px;"/>
