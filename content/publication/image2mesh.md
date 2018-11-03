+++
abstract = "A challenge that remains open in 3D deep learning is how to efficiently represent 3D data to feed deep neural networks. Recent works have been relying on volumetric or point cloud representations, but such approaches suffer from a number of issues such as computational complexity, unordered data, and lack of finer geometry. An efficient way to represent a 3D shape is through a polygon mesh as it encodes both shape's geometric and topological information. However, the mesh's data structure is an irregular graph (i.e. collection of vertices connected by edges to form polygonal faces) and it is not straightforward to integrate it into learning frameworks since every mesh is likely to have a different structure. Here we address this drawback by efficiently converting an unstructured 3D mesh into a regular and compact shape parametrization that is ready for machine learning applications. We developed a simple and lightweight learning framework able to reconstruct high-quality 3D meshes from a single image by using a compact representation that encodes a mesh using free-form deformation and sparse linear combination in a small dictionary of 3D models. In contrast to prior work, we do not rely on classical silhouette and landmark registration techniques to perform the 3D reconstruction. We extensively evaluated our method on synthetic and real-world datasets and found that it can efficiently and compactly reconstruct 3D objects while preserving its important geometrical aspects."
abstract_short = ""
authors = ["**Jhony K. Pontes**", "[Chen Kong](http://www.cs.cmu.edu/~chenk/)", "[Sridha Sridharan](http://staff.qut.edu.au/staff/sridhara/)", "[Simon Lucey](http://www.simonlucey.com/)", "[Anders Eriksson](https://ando.000webhostapp.com/)", "[Clinton Fookes](http://staff.qut.edu.au/staff/fookes/)"]
date = "2017-11-29"
image_preview = "headers/image2mesh_small.png"
math = true
publication_types = ["1"]
publication = "In *ACCV 2018*"
publication_short = "*ACCV 2018*"
selected = false
title = "Image2Mesh: A learning framework for single image 3D reconstruction"
url_code = "https://github.com/jhonykaesemodel/image2mesh"
#url_dataset = "#"
url_pdf = "papers/image2mesh-accv2018-camera_ready.pdf"
url_arxiv = "papers/ArXiV_image2mesh2017.pdf"
#url_project = "project/deep-learning/"
#url_slides = "#"
url_bibtex = "papers/image2mesh2017.html"
url_sup = "papers/Supplementary_Material_image2mesh_accv2018.pdf"

#[[url_custom]]
#name = "Custom Link"
#url = "https://www.example.org"

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/overview_image2mesh.png"
#caption = "My caption :smile:"

+++
### Overview
Given a single image, our framework employs a convolutional autoencoder to extract the image's latent space, $\mathbf{z}$, that is used to classify it to an index, $c$, using a multi-label classifier and regress it to a compact shape parametrization using a feedforward network. We use a graph embedding, $\mathcal{G}$, that compactly represents 3D mesh objects to reconstruct the 3D model. Firstly, the estimated index, $c$, selects the closest 3D model to the image from the graph. Secondly, the selected model is deformed through the estimated parameters - free-form deformation (FFD), $\mathbf{\Delta P}$, and sparse linear combination parameters (i.e. $\alpha$'s). In this example, model 1 is selected (arrows 1 and 2), FFD is then applied (arrows 3 and 4), and finally the linear combination with the nodes 3, 4, 5, 6, and 7 (blue arrows on the graph that indicates the models in dense correspondence with node 1) are performed (arrow 5) to reconstruct the final 3D mesh model (arrow 6).
<img src="/overview_image2mesh.png" alt="Drawing" style="width: 850px;"/>

### Results
Qualitative results for the synthetic dataset. Column (a) shows the input image. Column (b) shows the selected model from the graph. Column (c ) shows the selected model with the FFD parameters applied. The final 3D model reconstructed by applying the linear combination parameters is shown in column (d) and the ground truth in (e).

<div align="center">
<video width="100%" height="100%" autoplay loop>
  <source src="/1_video_synthetic_results.mp4"
  type="video/mp4" />
  Your browser does not support the video tag.
</video>
</div>

Qualitative results for the real-world dataset. Column (a) shows the input image. Column (b) shows the selected model. Column (c ) shows the selected model deformed by the FFD parameters. The final 3D model reconstructed by applying the linear combination parameters is shown in column (d). We compare with [18] in column (e) and the ground truth is shown in column (f).

<video width="100%" height="100%" autoplay loop>
  <source src="/2_video_pascal_results.mp4"
  type="video/mp4" />
  Your browser does not support the video tag.
</video>

A closer look at the 3D reconstruction.

<video width="100%" height="100%" autoplay loop>
  <source src="/3_video_details_synthetic_pascal.mp4"
  type="video/mp4" />
  Your browser does not support the video tag.
</video>

### More static examples
Qualitative results for the synthetic dataset. Column (a) shows the input image. Column (b) shows the selected model from the graph. Column (c ) shows the selected model with the FFD parameters applied. The final 3D model reconstructed by applying the linear combination parameters is shown in column (d). The voxelized final model is shown in column (e) and the ground truth in column (f). In the success cases (blues), one can see that the final models are similar to the ground truth with slightly differences that can be hard to point it out. A failure case is shown on the last row in red where a "wrong" model was selected from the graph.

<img src="/image2mesh_1_header.png" alt="Drawing" style="width: 850px;"/>
<img src="/image2mesh_1.png" alt="Drawing" style="width: 900px;"/>

Qualitative results for the real-world dataset. Column (a) shows the input image. Column (b) shows the selected model. Column (c ) shows the selected model deformed by the FFD parameters. The final 3D model reconstructed by applying the linear combination parameters is shown in column (d). We compare with [18] in column (e) and the ground truth is shown in column (f).

<img src="/image2mesh_2_header.png" alt="Drawing" style="width: 850px;"/>
<img src="/image2mesh_2.png" alt="Drawing" style="width: 900px;"/>

**Please check the supplementary material out for more examples.**

[[18] J.K. Pontes, C. Kong, S. Sridharan, S. Lucey, A. Eriksson, and C. Fookes, Compact Model Representation for 3D Reconstruction, 3DV 2017.](https://jhonykaesemodel.com/publication/3dv2017/)
