
+++
abstract = "Implicit shape representations, such as Level Sets, provide a very elegant formulation for performing computations involving curves and surfaces. However, including implicit representations into canonical Neural Network formulations is far from straightforward. This has consequently restricted existing approaches to shape inference, to significantly less effective representations, perhaps most commonly voxels occupancy maps or sparse point clouds. To overcome this limitation we propose a novel formulation that permits the use of implicit representations of curves and surfaces, of arbitrary topology, as individual layers in Neural Network architectures with end-to-end trainability. Specifically, we propose to represent the output as an oriented level set of a continuous and discretised embedding function. We investigate the benefits of our approach on the task of 3D shape prediction from a single image and demonstrate its ability to produce a more accurate reconstruction compared to voxel-based representations. We further show that our model is flexible and can be applied to a variety of shape inference problems."
abstract_short = ""
authors = ["Mateusz Michalkiewicz", "**Jhony K. Pontes**", "Dominic Jack", "Mahsa Baktashmotlagh", "[Anders Eriksson](https://ando.000webhostapp.com/)"]
date = "2019-07-22"
image_preview = "headers/deeplevelsets.png"
math = true
publication_types = ["1"]
publication = "In *ICCV 2019*"
publication_short = "*ICCV 2019*"
selected = false
title = "Implicit surface representations as layers in neural networks"
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
