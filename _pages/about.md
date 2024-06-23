---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
    .project-content {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .project-content .project-text,
    .project-content .project-image {
        width: 100%;
    }
</style>
<style>
    @media screen and (min-width: 768px) { 
        .project-content {
            flex-direction: row; /* This reverses the order of flex items */
        }
        .project-content .project-text {
            flex: 1;
            padding-right: 20px; /* Adjust padding to the left of the text for separation */
        }
        .project-content .project-image {
            max-width: 300px;
          
        }
    }
           .justified-text {
            text-align: justify;
        }
</style>


I am Mohan Shi, an incoming Ph.D. student in Electrical and Computer Engineering at [University of California, Los Angeles (UCLA)](https://www.ucla.edu/), under the guidance of [Prof. Abeer Alwan](https://www.seas.ucla.edu/spapl/index.html). I obtain my master degree at the [University of Science and Technology of China (USTC)](https://en.ustc.edu.cn/) and had the pleasure of working under the guidance of [Prof. Li-Rong Dai](https://dblp.org/pid/48/6462-1.html) for three years. My research interests span a variety of domains in the world of speech processing:

<ul class='twocol' style="margin-top: -1%;" markdown='1'>
<li>Automatic Speech Recognition</li>
<li>Cocktail Party Problem</li>
<li>Large Language Models</li>
</ul>

<!-- <a id="research_highlights"></a>
## Research Highlights


### Conversational Speaker Separation via Neural Diarization
<div class="project-content">
    <div class="project-text">
       <p class="justified-text"> We introduce a new framework, termed ``speaker separation via neural diarization" (SSND), for multi-channel conversational speaker separation. The proposed SSND framework achieves state-of-the-art diarization and ASR results, surpassing all existing  methods on the open LibriCSS dataset.
      <a href="/projects/ssnd/">Read More</a>  </p>
    </div>
    <div class="project-image">
<img src='/images/diar_sep_small-02.png' style='width:300px;' alt='Project 0 Image Description'>
    </div>
</div>  
----
### Location-based Training (LBT)
<div class="project-content">
    <div class="project-text">
      <p class="justified-text">
 We have proposed two novel training criteria to address the permutation ambiguity problem for multi-channel
talker-independent speaker separation. Different from widely-used permutation invarient trainig (PIT), the new criteria organize DNN outputs on the basis of speaker azimuths and distances relative to a microphone array. 
      <a href="http://web.cse.ohio-state.edu/~wang.77/papers/TTW.taslp22.pdf">Read More</a>  </p>
    </div>
    <div class="project-image">
<img src='/images/lbt.png' style='width:300px;' alt='Project 1 Image Description'>
    </div>
</div>
---
### Microphone Array Geometry Agnostic Modeling
<div class="project-content">
    <div class="project-text">
      <p class="justified-text">
 We utilized spatial features along with speaker embeddings for personalized speech enhancement (PSE) and showed their combination significantly improved the performance for both ASR and signal quality. Furthermore, we proposed a new architecture and introduced the stream pooling layer to perform multi-channel PSE with any number and arrangement of microphones in a way where the output is invariant to the microphone order. Our proposed model consistently outperformed the geometry-dependent models. 
      <a href="https://arxiv.org/pdf/2110.10330.pdf">Read More</a>  </p>
    </div>
    <div class="project-image">
<img src='/images/stream_averaging.png' style='width:300px;' alt='Project 1 Image Description'>
    </div>
</div>
---


### Multi-input Multi-output Complex Spectral Mapping
<div class="project-content">
    <div class="project-text">
      <p class="justified-text">
  Current deep learning based multi-channel speaker separation methods produce a monaural estimate of speaker signals captured by a reference microphone. This work presents a new multi-channel complex spectral mapping approach that simultaneously estimates the real and imaginary spectrograms of all speakers at all microphones. Experimental results show that the proposed MIMO separation model outperforms a multi-input single-output (MISO) speaker separation model with monaural estimates. The proposed approach achieves the state-of-the-art speaker separation on the open LibriCSS dataset.
      <a href="http://web.cse.ohio-state.edu/~wang.77/papers/TPWXW.interspeech23.pdf">Read More</a>  </p>
    </div>
    <div class="project-image">
<img src='/images/MIMO.png' style='width:300px;' alt='Project 1 Image Description'>
    </div>
</div> -->


<a id="Publications"></a>
## Publications
----
1. **CASA-ASR: Context-Aware Speaker-Attributed ASR**, *Interspeech 2023* [[pdf](https://www.isca-archive.org/interspeech_2023/shi23d_interspeech.pdf)]
<i>**Mohan Shi**</i>, Zhihao Du, Qian Chen, Fan Yu, Yangze Li, Shiliang Zhang, Jie Zhang, and Li-Rong Dai

1. **Semantic VAD: Low-Latency Voice Activity Detection for Speech Interaction**, *Interspeech 2023 <font color="red">(Oral)</font>* [[pdf](https://www.isca-archive.org/interspeech_2023/shi23c_interspeech.pdf)]
<i>**Mohan Shi**</i>, Yuchun Shu, Lingyun Zuo, Qian Chen, Shiliang Zhang, Jie Zhang, and Li-Rong Dai

1. **A Comparative Study on Multichannel Speaker-Attributed Automatic Speech Recognition in Multi-party Meetings**, *APSIPA ASC 2023* [[pdf](https://arxiv.org/pdf/2211.00511)]
<i>**Mohan Shi**</i>, Jie Zhang, Zhihao Du, Fan Yu, Qian Chen, Shiliang Zhang, and Li-Rong Dai

1. **The Second Multi-Channel Multi-Party Meeting Transcription Challenge (M2MeT 2.0): A Benchmark for Speaker-Attributed ASR**, *ASRU 2023* [[pdf](https://arxiv.org/pdf/2309.13573)]
Yuhao Liang, <i>**Mohan Shi**</i>, Fan Yu, Yangze Li, Shiliang Zhang, Zhihao Du, Lei Xie, Yanmin Qian, Jian
Wu, Zhuo Chen, Kong Aik Lee, Zhijie Yan, and Hui Bu

1. **Non-autoregressive End-to-End Speaker-Attributed ASR**, *ASRU 2023* [[pdf](https://arxiv.org/pdf/2310.04863)]
Yangze Li, Fan Yu, Yuhao Liang, Pengcheng Guo, <i>**Mohan Shi**</i>, Zhihao Du, Shiliang Zhang, and Lei Xie


<!-- <a id="Patents"></a>
## Patents
----

0. Hassan Taherian, Jonathan Huang and Carlos M. Avendano, <i>Method and System for Detecting Sound Event Liveness Using a Microphone Array</i>, U.S. Patent No. 11,533,577. 20 Dec. 2022. [[Google Patents](https://patents.google.com/patent/US11533577B2/en)]

0. Hassan Taherian, Sefik Emre Eskimez, Takuya Yoshioka, Huaming Wang, Zhuo Chen and Xuedong Huang, <i>Array Geometry Agnostic Multi-channel Personalized Speech Enhancement</i>, U.S. Patent App. No. US20230116052A1, Dec 2021. 
{: reversed="reversed"} -->

   

<a id="Experience"></a>
## Research Experience
----
###  <img src='/images/ustc.jpeg' style='width:38px'> University of Science and Technology of China 
<ul class='twocol' markdown='1'>
<li>Research Assistant, Sep 2021 – Jun 2024</li>
</ul>

###  <img src='/images/damo.png' style='width:40px' >  Alibaba Damo Academy
<ul class='twocol' markdown='1'>
<li>Research Intern, Speech Lab, Jul 2022 – May 2023</li>
</ul>

### <img src='/images/tencent.jpeg' style='width:50px'  >   Tencent AI Lab
<ul class='twocol' markdown='1'>
<li>Research Intern, Seattle Speech Lab, Sep 2023 – August 2024</li>
</ul>

<!-- Teaching Experience
----
### <img src='/images/osu_small.jpeg' style='width:38px'> Ohio State University
Instructor of CSE 1222 - Programming in C++
Responsible for teaching, grading and holding office hours
Offered in Spring 2018, and Fall 2017 (~40 enrollment) -->



