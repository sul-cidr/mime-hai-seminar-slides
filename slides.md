# Decoding Directorial Style: Using Pose and Action Estimation to Analyze Theater Performances

<!-- .slide: data-background-video="assets/vis_fondly_phalp_coco.mp4" -->
<!-- .slide: data-background-size="contain" -->
<!-- .slide: data-background-video-loop -->
<!-- .slide: class="main-title" -->


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

:::
This research project leverages machine learning and computer vision to analyze directorial styles and other aspects of theater performances through the lens of pose and action recognition. By applying these techniques to video recordings of theatrical performances, we compare multiple performances per director to identify distinctive patterns in choreography and staging. Our approach combines distant and close viewing methodologies, allowing for a nuanced understanding of theatrical gestures and movements. By comparing different directors’ uses of pose, we aim to quantify the elusive concept of directorial style.

This interdisciplinary project bridges the gap between performing arts, computer science and digital humanities, offering new insights into theatrical analysis and refining our understanding of directorial signatures in live performance.


---


# The Problem

:::
Examining pose and staging in theater can be tricky since it sits at the heart of artistic expression in the theater. Pose and staging lies at the intersection of authorial intent, directorial vision, and is mediated by the performer, and now, we’re adding computational analysis. At its core, our problem revolves around a fundamental question: How can we quantify and analyze the physical arrangements and movements of actors on stage in a way that reveals something meaningful about the director's creative contribution?

In traditional theater studies, the concept of pose is often taken for granted. Directors, performers and audiences intuitively understand the power of a well-crafted tableau or a precisely choreographed sequence of movements.  In theater, iconic poses or choreography can define productions, like Brecht’s silent scream choreography in Mother Courage, or Bob Fosse’s shoulder roll and arm pops in The Pajama Game or the collective poses of the ensemble in "A Chorus Line.” These production’s indelible poses helped make the work memorable, and are a signature of a particular director’s contribution to the production, and serve as a shorthand for identifying a director’s style.

However, these individual, memorable poses are just the tip of the iceberg. Our challenge lies in understanding the aggregate effect of all poses throughout a production, and even more ambitiously, across multiple productions by the same director. This is where we begin to approach the notion of a director's signature or style.

In film studies, auteur theory provides a framework for understanding a director's unique imprint on their work. Film directors have a range of tools at their disposal – camera angles, editing techniques, lighting choices – that make their stylistic signatures more readily apparent. In theater, however, the director's expressive capabilities are more constrained, and their contribution can be more elusive to pin down. In the theater, a director is constrained far more by the physical space that they’re staging in, and the fact that they can’t edit their work. Their main tool for expression lies in the way that they create stagings  with the actors.

This is where the computational analysis of pose in theater becomes interesting. By leveraging technologies like pose estimation and action recognition, we can begin to quantify aspects of theatrical performance that were previously left to subjective interpretation. We can analyze not just individual poses, but patterns of movement, spatial relationships between performers, and even the rhythm and flow of a production.

The question that you might be asking yourself, is “A purely data-driven analysis might pick up on patterns and consistencies in a director's work, but can it capture the nuanced, thematic use of pose that a trained theater scholar might recognize immediately?” This is the delicate balance we must strike. On one hand, we have the potential to uncover patterns and stylistic elements that might not be apparent to the naked eye, especially when analyzing a director's body of work as a whole. On the other hand, we risk reducing the rich, complex art of theater direction to a series of data points.

The solution, it seems, lies in a synthesis of approaches. By combining the insights of traditional theater scholarship with the analytical power of computational methods, we can begin to develop a more comprehensive understanding of pose in theater. We can use data to support and enhance our qualitative analyses, and we can use our human understanding of theatrical context to guide our interpretation of the data.

Ultimately, the problem of pose in theater is not just about understanding physical arrangements on stage. It's about decoding the language of movement that directors use to communicate their artistic vision. It's about recognizing patterns across productions that might reveal deeper truths about a director's style or preoccupations. And perhaps most excitingly, it's about opening up new avenues for creativity and analysis in the world of theater.


---


# Methodology

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


# The MIME Platform

---


## Platform Demonstration

<video controls muted src="assets/mime-hai-seminar-demo-video.mp4"></video>

---


# Results & Analysis


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


# Implications

:::
The computational analysis of pose and action in theatrical performances, as presented in this research, opens up new avenues for understanding directorial styles and signatures. However, the implications of this research extend far beyond the realm of theater studies.

First, this methodology could be readily adapted to analyze performances in film, opera, dance, and other forms of visual arts involving human bodies. By quantifying patterns of movement and pose across different mediums, we may uncover new insights into the nature of performance itself, potentially bridging gaps between traditionally separate disciplines. There is also the possibility of applying this type of analysis to political speech to biomechanics of physiology and sports.

One of the most promising aspects of this research lies in its potential for comparative studies. By analyzing pose across a director's entire body of work, we can identify recurring patterns and evolving styles that might not be apparent when examining individual performances. Furthermore, this method allows for objective comparisons between different directors' interpretations of the same material, potentially revealing new dimensions of artistic interpretation.

However, it's crucial to acknowledge the ethical considerations and limitations inherent in this approach. The use of video analysis raises valid concerns about surveillance and privacy. Moreover, the application of these methods to archived performances without explicit consent from the directors and all involved performers presents a complex ethical landscape that requires careful navigation.

From an analytical standpoint, we must also recognize the limitations of focusing solely on pose. Theater is a multifaceted art form, and pose represents only one aspect of a rich tapestry that includes dialogue, set design, lighting, and more. While our analysis provides valuable insights, it should be viewed as a narrow view of a performance that is a complement to, rather than a replacement for, traditional methods of artistic analysis.

Finally, t's important to note that this computational approach cannot definitively determine directorial intent. The patterns we observe may result from conscious directorial choices, actor contributions, or even unintentional recurring elements. As such, these findings should serve as a starting point for deeper, more nuanced investigations rather than definitive conclusions.

In conclusion, while this research presents exciting possibilities for quantitative analysis in the arts, its true value lies in its potential to complement and enhance, rather than replace, traditional scholarly approaches. By combining computational methods with expert human interpretation, we can develop a more comprehensive understanding of theatrical performance and directorial style.


---


# Questions & Discussion


---


# Thank You

<div class="logos">

![TAPS](assets/logos/taps.png)
![CIDR](assets/logos/CIDR_on_dark.1237x677.png)
![SUL](assets/logos/sul_white.png)

</div>

