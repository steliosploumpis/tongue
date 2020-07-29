# [3D human tongue reconstruction with adversarial surface generation](https://arxiv.org/abs/1911.08008)

 [Stylianos Ploumpis](https://www.imperial.ac.uk/people/s.ploumpis)<sup> 1,2 * </sup>, [Stylianos Moschoglou](https://www.doc.ic.ac.uk/~sm3515/)<sup> 1,2 * </sup>, Vasileios Triantafyllou <sup> 2</sup>, & [Stefanos Zafeiriou](https://wp.doc.ic.ac.uk/szafeiri/)<sup> 1,2</sup>
 <br/>
 <sup>1 </sup>Imperial College London, UK
 <br/>
 <sup>2 </sup> Huawei Techologies co.ltd
 <br> 
 <sup>* </sup> Indicates equal contribution




<br/>

<p align="center"><img width="100%" src="figures/first_page_fig.png" /></p>

<br/>

<p align="center"><img width="65%" src="figures/head.gif" alt="Logo"></p>



## Abstract

3D face reconstruction from a single image is a task that has garnered increased interest in the Computer Vision community, especially due to its broad use in a number of applications such as realistic 3D avatar creation, pose invariant face recognition and face hallucination.  Since the introduction of the 3D Morphable Model in the late 90’s, we witnessed an explosion of research aiming at particularly tackling this task. Nevertheless, despite the increasing level of detail in the 3D face reconstructions from single images mainly attributed to deep learning advances, finer and highly deformable components of the face such as the tongue are still absent from all 3D face models in the literature, although being very important for the realness of the 3D avatar representations. In this work we present the first, to the best of our knowledge, method that: a) accurately reconstructs the tongue by utilizing a novel GAN framework which directly models the surface distribution of the tongue from raw data without any preprocessing, and b) seamlessly merges it with the existing state-of-the-art face and head models. Moreover, we make publicly available to the community the first diverse tongue dataset, consisting of $5,200$ raw scans of $1,500$ individuals varying in gender, age, and ethnicity backgrounds. Finally, as we demonstrate in an extensive series of quantitative as well as qualitative experiments, our model proves to be robust and realistically captures the 3D tongue structure, even in adverse ``in-the-wild'' conditions. 

## Approach

<p align="center"><img width="100%" src="figures/overview.png" /></p>
An illustration of our tongue reconstruction framework during inference.  The embedding network predicts a latent 3D feature ̃ywhich is later transformed to the corresponding parametersptof the synthetic expression PCAUtvia linear projection to theWt,ymatrix. The generator from Section 3 randomly predicts10Kpoints(z∼N(0, I))that belong to the distribution of the tongue surface.This point-cloud is later utilized in the tongue optimization pipe-line described in Section 4.1 which aims at refining the shape of the initialtongue expression.

<p align="center"><img width="50%" src="figures/triangles.png" /></p>



<br/>

## TongueGAN
<p align="center"><img width="70%" src="figures/eyes.png" /></p>

<p align="center"><img width="80%" src="figures/eye_ear.gif" alt="Logo"></p>

<br/>

## Tongue Reconstruction Results from single images

<p align="center"><img width="70%" src="figures/qual_1.png" /></p>

<br/>

## Citation
If you find this work is useful for your research, please cite our [paper](http://openaccess.thecvf.com/content_CVPR_2019/html/Ploumpis_Combining_3D_Morphable_Models_A_Large_Scale_Face-And-Head_Model_CVPR_2019_paper.html):

```


```

<br/>

## Public release Tongue dataset

