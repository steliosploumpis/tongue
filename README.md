# [3D human tongue reconstruction from single ''in-the-wild'' images](https://arxiv.org/pdf/2106.12302.pdf)

 [Stylianos Ploumpis](https://www.imperial.ac.uk/people/s.ploumpis)<sup> 1,2 * </sup>, [Stylianos Moschoglou](https://www.doc.ic.ac.uk/~sm3515/)<sup> 1,2 * </sup>, Vasileios Triantafyllou <sup> 2</sup>, & [Stefanos Zafeiriou](https://wp.doc.ic.ac.uk/szafeiri/)<sup> 1,2</sup>
 <br/>
 <sup>1 </sup>Imperial College London, UK
 <br/>
 <sup>2 </sup> Huawei Techologies co. ltd
 <br> 
 <sup>* </sup> Indicates equal contribution




<br/>

<p align="center"><img width="100%" src="figures/teaser_fig_new.png" /></p>

<br/>

<p align="center"><img width="60%" src="figures/com_animate.gif" alt="Logo"></p>



## Abstract

3D face reconstruction from a single image is a task that has garnered increased interest in the Computer Vision community, especially due to its broad use in a number of applications such as realistic 3D avatar creation, pose invariant face recognition and face hallucination. Since the introduction of the 3D Morphable Model in the late 90’s, we witnessed an explosion of research aiming at particularly tackling this task. Nevertheless, despite the increasing level of detail in the 3D face reconstructions from single images mainly attributed to deep learning advances, finer and highly deformable components of the face such as the tongue are still absent from all 3D face models in the literature, although being very important for the realness of the 3D avatar representations. In this work we present the first, to the best of our knowledge, end-to-end trainable pipeline that accurately reconstructs the 3D face together with the tongue. Moreover, we make this pipeline robust in ''in-the-wild'' images by introducing a novel GAN method tailored for 3D tongue surface generation. Finally, we make publicly available to the community the first diverse tongue dataset, consisting of 1,800 raw scans of 700 individuals varying in gender, age, and ethnicity backgrounds. As we demonstrate in an extensive series of quantitative as well as qualitative experiments, our model proves to be robust and realistically captures the 3D tongue structure, even in adverse ''in-the-wild'' conditions.  

## Approach

<p align="center"><img width="100%" src="figures/method.png" /></p>
An illustration of our tongue reconstruction framework. First we train the point-cloud AE on its own to get meaningful 3D features (y) of our collected point-cloud tongues. After this is done the rest of the pipeline is trained in an end-to-end fashion. We use as input to the encoder a 2D tongue image from our dataset. The encoder output is then translated through an MLP. The output of the MLP corresponds to the PCA parameters of our rigged head model. We then reconstruct the tongue expression based on the PCA model and these parameters. Finally, the tongue expression is optimised based on the ground-truth 3D tongue point-cloud (which corresponds to the input image). The optimisation is carried out by back-propagation using a number of different 

<br/>

## TongueGAN
<p align="center"><img width="90%" src="figures/net_diagram_narrow.png" /></p>
TongueGAN architecture. Symbol c stands for row-wise concatenation along the channel dimension. Symbol o stands for element-wise (i.e., Hadamard) product. The Generator inputs are: i) a Gaussian noise sample z and ii) a label ~y corresponding to a particular tongue, from which we want to sample a 3D point. The Discriminator input pairs are: i) (y,x), y is a label corresponding to a specific tongue and x a real 3D point belonging to the aforementioned tongue point-cloud, ii) (~y, G(z,~y)), where ~y is a label corresponding to a tongue and G(z,~y) a generated point belonging to this tongue. The Discriminator is asked to distinguish the real from the fake (i.e., generated) pair.


<br/>

## Tongue Reconstruction Results from single images

<p align="center"><img width="100%" src="figures/qual_fig_new.png" /></p>

<br/>

## Citation
If you find this work is useful for your research, please cite our [paper](https://arxiv.org/pdf/2106.12302.pdf):

```


```

<br/>

## Public release Tongue dataset

<p align="center"><img width="60%" src="figures/raw_point_cloud_dataset_2.png" /></p>

<br/>

## Code

TBA



