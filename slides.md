# Decoding Directorial Style: Using Pose and Action Estimation to Analyze Theater Performances

<!-- .slide: data-background-video="assets/vis_fondly_phalp_coco.mp4" -->
<!-- .slide: data-background-size="contain" -->
<!-- .slide: data-background-video-loop -->

---


## Introductions

<div class="headshots">

![Michael Rau](assets/people/michael_rau.jpeg) Michael Rau

![Peter Broadwell](assets/people/peter_broadwell.jpeg) Peter Broadwell

![Simon Wiles](assets/people/simon_wiles.jpeg) Simon Wiles

![Vijoy Abraham](assets/people/vijoy_abraham.jpeg) Vijoy Abraham

</div>

<div class="logos">

![TAPS](assets/logos/taps.png)
![CIDR](assets/logos/CIDR_on_dark.1237x677.png)
![SUL](assets/logos/sul_white.png)

</div>


---


## Defining the Problem (understanding pose in theater)


---


## A Breakthrough: Temporal-Convolutional vs. Transformer Models

<div class="img-row">

![OpenPifPaf not doing well](assets/methods/OpenPifPaf_bad.jpg "OpenPifPaf not doing well") Open PifPaf<br> (Temporal-Convolutional)

![PHALP doing well](assets/methods/PHALP_good.jpg "PHALP doing well") PHALP<br>(Transformers)

</div>


---


## A Breakthrough, Courtesy of the HAI Spring 2022 Conference

<div class="img-row">

![HAI Spring 2022 video grab](assets/methods/HAI_spring_2022_frame.png "HAI Spring 2022") HAI Spring Conference, April 12, 2022<br>“Key Advances in AI”

![HAI Spring 2022 program](assets/methods/HAI_spring_2022_program.png "HAI Spring 2022")

</div>


---


## PHALP: Predicting Human Appearance, Location and Pose

<img class="r-stretch" src="assets/methods/phalp_teaser.png" />

Jathushan Rajasegaran, Georgios Pavlakos, Angjoo Kanazawa, Jitendra Malik. “Tracking People by Predicting 3D Appearance, Location & Pose.” arxiv.org/abs/2112.04477 (2021)


---


## Vision Transformers (ViT): Attention Comes to Pixel Patches

<div class="img-row">

![A vision transformer](assets/methods/vision-transformer.png "Vision transformer diagram") Alexey Dosovitskiy, et al. “An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale.” In Proc. International Conference on Learning Representation 2021.

![Transformer self-attention diagram](assets/methods/transformer_self-attention_visualization.png "Transformer self-attention diagram") Multi-headed self-attention, but with image patches, rather than words<br>
(jalammar.github.io/illustrated-transformer/)

</div>


---


## How PHALP Uses Transformers for Detection and Tracking

<img class="r-stretch" src="assets/methods/4D-Humans.png" />

Shubham Goel, Georgios Pavlakos, Jathushan Rajasegaran, Angjoo Kanazawa, Jitendra Malik. “Humans in 4D: Reconstructing and Tracking Humans with Transformers.” arxiv.org/abs/2305.20091 (2023)


---


## LART: Lagrangian Action Recognition with Tracking

<img class="r-stretch" src="assets/methods/LART.png" />

Jathushan Rajasegaran, Georgios Pavlakos, Angjoo Kanazawa, Christoph Feichtenhofer, Jitendra Malik. “On the Benefits of 3D Pose and Tracking for Human Action Recognition.” arxiv.org/abs/2304.01199 (2023)


---


## View-Invariant ("2.5D") Pose Embeddings

<img class="r-stretch" src="assets/methods/view-invariant_embeddings.jpg" />

Sun, Jennifer J, Jiaping Zhao, Liang-Chieh Chen, Florian Schroff, Hartwig Adam and Ting Liu. “View-Invariant Probabilistic Embedding for Human Pose.” In Proceedings of the European Conference on Computer Vision, Springer, 2020, pp. 53-70.


---


## Building the MIME Platform / Live Demo


---


## Results & Analysis


---


## The Test Corpus: Assembling Multiple Works per Director

<img class="r-stretch" src="assets/results/31_performances.png" />


---


## Which Features Are Best for Differentiating between Directors?

<div class="img-row">

![Pose motion and distance confusion matrix](assets/results/LOO_motion_distance.png "Pose motion and distance confusion matrix") Pose motion and distance statistics

![View-invariant pose embeddings confusion matrix](assets/results/LOO_POEM_features.png "View-invariant pose embeddings confusion matrix") View-invariant pose embeddings

</div>


---


## Which Features Are Best for Differentiating between Directors?

<img class="r-stretch" src="assets/results/31_performances_hl.png" />


---


## Which Features Are Best for Differentiating between Directors?

<div class="img-row">

![3D coordinates confusion matrix](assets/results/LOO_3D_coords.png "3D coordinates confusion matrix") Body keypoint coords (3D)

![Action recognition embeddings confusion matrix](assets/results/LOO_action_features.png "Action recognition embeddings confusion matrix") Action recognition embeddings

</div>


---


## Which Features Are Best for Differentiating between Directors?

(Summary statistics of classification experiments go here)


---


## Which Features Are Best for Differentiating between Directors?

<div class="img-row">

![Pose motion and distance feature importances](assets/results/importances_motion_distance_nb.png "Pose motion and distance feature importances") Pose motion and distance

![Pose embedding importances](assets/results/importances_poem_nb.png "Pose embedding importances") View-invariant pose embedding elements

</div>


---


## Which Features Are Best for Differentiating between Directors?

<img class="r-stretch" src="assets/results/importances_keypoints_nb.png" />

Body keypoint coords (3D)


---


## Visualizing Directors' Pose "Repertoires"

<img class="r-stretch" src="assets/results/poem_umap_sampled_2.png" />


---


## Direct Comparison: Multiple Directors' Stagings of the Same Work

<div>

![Comparisons of performances of Don Giovanni](assets/results/dg_comparison_table.png "Comparisons of performances of Don Giovanni")

</div>

<div class="screenshots">

![Michael Hampe](assets/results/Viva_Hampe-Karajan.png) Michael Hampe

![Romeo Castellucci](assets/results/Viva_Castellucci.png) Romeo Castellucci

![Erik Söderblom](assets/results/Viva_Soderblom-Helsinki.png) Erik Söderblom

</div>


---


## Direct Comparison: Multiple Directors' Stagings of the Same Work

<div>

![Comparisons of performances of Don Giovanni](assets/results/dg_comparison_table.png "Comparisons of performances of Don Giovanni")

</div>

<div class="screenshots">

![Sven-Erik Bechtolf](assets/results/Viva_Bechtolf-Zurich.png) Sven-Erik Bechtolf

![Damiano Michieletto](assets/results/Viva_Michieletto.png) Damiano Michieletto

![Jean-François Sivadier](assets/results/Viva_Sivadier-Aix.png) Jean-François Sivadier

</div>


---


## Aligning Performances (by Music) to Get Average Pose "Consensus"

<div class="r-stack">
  <img
    src="assets/methods/Don_Giovanni-Soderblom-Helsinki_UzxYEVbOS5w.mp4_chroma_time_correspondences.png"
  />
  <img
    class="fragment"
    src="assets/methods/Don_Giovanni-Soderblom-Helsinki_UzxYEVbOS5w.mp4_chroma_comparison.png"
  />
  <img
    class="fragment"
    src="assets/methods/Don_Giovanni-Soderblom-Helsinki_UzxYEVbOS5w.mp4_chroma_warping_path.png"
  />
</div>


---


## Comparing Each Director's Poses to the "Consensus" Average

<section data-background-iframe="assets/bokeh/dg_poem_comparison.html"
         data-background-interactive>
</section>

---


## Implications and Future Directions


---


## Questions & Discussion


---


# Thank You

<div class="logos">

![TAPS](assets/logos/taps.png)
![CIDR](assets/logos/CIDR_on_dark.1237x677.png)
![SUL](assets/logos/sul_white.png)

</div>

