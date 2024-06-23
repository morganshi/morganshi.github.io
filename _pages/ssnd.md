---
layout: blank
title: "SSND Speech Separation Demo"
permalink: /projects/ssnd/
excerpt: "Demonstration of the SSND Framework"
---

<style>
  body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 20px;
    background: #f9f9f9;
    color: #333;
  }
  h1, h2 {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin-bottom: 20px;
  }
  .container {
    max-width: 1200px;
    margin: auto;
    padding: 0 20px;
  }
  .demo-section {
    margin-bottom: 40px;
  }
  .demo {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 20px;
  }
  .audio {
    flex-basis: 30%;
    text-align: center;
  }
  img {
    max-width: 65%;
    height: auto;
  }
  footer {
    text-align: center;
    margin-top: 20px;
    padding-top: 20px;
    border-top: 1px solid #ccc;
  }

  .ieee-style {
    font-family: 'Times New Roman', Times, serif; 
    text-align: center;
    margin-top: 30px;

      border-top: 2px solid black;
  border-bottom: 2px solid black;
  padding: 10px 0;
  margin-bottom: 20px;
  text-align: center;
}

.ieee-title {
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 20px;
}

.ieee-author {
    font-size: 20px;
    margin-bottom: 10px;
}

.ieee-affiliation {
    font-size: 16px;
    font-style: italic;
}

  
.demo {
  display: flex;
  flex-direction: row;  /* default direction */
  align-items: center;
  justify-content: space-between;
  margin-bottom: 20px;
}

@media (max-width: 768px) {  /* Adjust as needed */
  .demo {
    flex-direction: column;  /* stack children vertically */
  }

  .audio, img {
    max-width: 100%;  /* adjust width for small screens */
  }
}
        .justified-text {
            text-align: justify;
        }
</style>


<div class="ieee-style">
    <h1 class="ieee-title">Multi-channel Conversational Speaker Separation via Neural Diarization</h1>
    <p class="ieee-author">Hassan Taherian, and DeLiang Wang</p>
    <p class="ieee-affiliation">
        Department of Computer Science and Engineering,<br>
        The Ohio State University, USA
    </p>
     <p> <a href="https://arxiv.org/pdf/2311.08630.pdf">Paper</a> </p>
</div>


<div class="container">
<!--   <h1>Speaker Separation via Neural Diarization (SSND) Demo</h1> -->
<!--   <p>We introduce the speaker separation via neural diarization (SSND) framework, a novel approach that seamlessly integrates speaker diarization with speaker separation. Our SSND framework achieves state-of-the-art performance for speaker-attributed ASR on LibriCSS dataset. Here, we showcase several examples taken from LibriCSS processed with SSND. In all examples, the entire segment is processed through the SSND framework without any chunking. -->


<p class="justified-text">We introduce a new framework, termed "speaker separation via neural diarization" (SSND), for multi-channel conversational speaker separation.  This approach employs a deep neural network (DNN) for speaker diarization to demarcate the speech activities of individual speakers. Leveraging the estimated utterance boundaries from neural diarization, we generate a sequence of speaker embeddings. These embeddings, in turn, facilitate the assignment of speakers to two output streams of the separation model. The SSND approach tackles the permutation ambiguity issue of talker-independent separation during the diarization phase, rather than during separation. This distinction permits non-overlapped speakers to be assigned to the same output stream, enabling the processing long recordings missing from standard CSS.  Another advantage of SSND lies in the inherent integration of speaker separation and diarization, enabling sequential grouping of the discontinuous utterances of the same talker.
Our SSND framework achieves state-of-the-art diarization and ASR results, surpassing all existing  methods on the open LibriCSS dataset.</p>
<div style="text-align: center;">
<img src="/images/diarSEP_diagram-01.png" alt="SSND diagram">
</div>

<div class="demo-section">
  <h2>Example 1</h2>
  <p class="justified-text">  This segment is from the "overlap_ratio_40.0_sil0.1_1.0_session1_actual39.7" recording of the LibriCSS dataset, spanning from 225s to 255s, with 40% overlap ratio.   </p>

<div class="demo">
    <div class="audio">
      <h4>Reverberant Mixed Audio</h4>
      <audio controls>
        <source src="/files/demo/example_3/segment_mixch0_15db.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </div>
    <img src="/files/demo/example_3/Spec_3.png" alt="Spectrogram of Mixed Audio">
  </div>
  
  <div class="demo">
    <div class="audio">
      <h4>Separated Audio Stream 1</h4>
      <audio controls>
        <source src="/files/demo/example_3/segment_0_15db.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </div>
    <img src="/files/demo/example_3/Spec_1.png" alt="Spectrogram of Stream 1">
  </div>
  
  <div class="demo">
    <div class="audio">
      <h4>Separated Audio Stream 2</h4>
      <audio controls>
        <source src="/files/demo/example_3/segment_1_15db.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </div>
    <img src="/files/demo/example_3/Spec_2.png" alt="Spectrogram of Stream 2">
  </div>

  <div class="demo">
    <div class="audio">
      <h4>Embedding Sequence Indices based on Diarization Estimates</h4>
    </div>
    <img src="/files/demo/example_3/plot.png" alt="Embedding Sequence Indices">
  </div>
  
</div>


<footer></footer>
<div class="demo-section">
  <h2>Example 2</h2>
  <p class="justified-text">  This segment is from the "overlap_ratio_0.0_sil0.1_0.5_session4_actual0.0" recording of the LibriCSS dataset, spanning from 320s to 345s, which encompasses speech from seven unique speakers with no speech overlap. Note that the estimated speakers boundaries extend slightly beyond the actual limits of their speech.   </p>

<div class="demo">
    <div class="audio">
      <h4>Reverberant Mixed Audio</h4>
      <audio controls>
        <source src="/files/demo/example_2/segment_mixch0_15db.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </div>
    <img src="/files/demo/example_2/Spec_mix.png" alt="Spectrogram of Mixed Audio">
  </div>
  
  <div class="demo">
    <div class="audio">
      <h4>Separated Audio Stream 1</h4>
      <audio controls>
        <source src="/files/demo/example_2/segment_0_15db.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </div>
    <img src="/files/demo/example_2/Spec_1.png" alt="Spectrogram of Stream 1">
  </div>
  
  <div class="demo">
    <div class="audio">
      <h4>Separated Audio Stream 2</h4>
      <audio controls>
        <source src="/files/demo/example_2/segment_1_15db.wav" type="audio/wav">
        Your browser does not support the audio element.
      </audio>
    </div>
    <img src="/files/demo/example_2/Spec_2.png" alt="Spectrogram of Stream 2">
  </div>

  <div class="demo">
    <div class="audio">
      <h4>Embedding Sequence Indices based on Diarization Estimates</h4>
    </div>
    <img src="/files/demo/example_2/plot.png" alt="Embedding Sequence Indices">
  </div>
  
</div>

<footer></footer>
<div class="demo-section">
    <h2>Example 3</h2>
    <p class="justified-text">This example, taken from the "overlap_ratio_40.0_sil0.1_1.0_session9_actual39.9" recording of the LibriCSS dataset (from 95s to 115s), presents a challenging scenario with 3-fold speech overlap. Although the SSND model is trained with examples containing only two-speaker overlap, it isolates one speaker in one stream while maintaining the remaining speakers in the other stream. Listen and observe the results below.</p>

 <div class="demo">
      <div class="audio">
        <h4>Reverberant Mixed Audio</h4>
        <audio controls>
          <source src="/files/demo/example_1/segment_mixch0_15db.wav" type="audio/wav">
          Your browser does not support the audio element.
        </audio>
      </div>
      <img src="/files/demo/example_1/Spec_mix.png" alt="Spectrogram of Mixed Audio">
    </div>
    <div class="demo">
      <div class="audio">
        <h4>Separated Audio Stream 1</h4>
        <audio controls>
          <source src="/files/demo/example_1/segment_0_15db.wav" type="audio/wav">
          Your browser does not support the audio element.
        </audio>
      </div>
      <img src="/files/demo/example_1/Spec_1.png" alt="Spectrogram of Stream 1">
    </div>
    <div class="demo">
      <div class="audio">
        <h4>Separated Audio Stream 2</h4>
        <audio controls>
          <source src="/files/demo/example_1/segment_1_15db.wav" type="audio/wav">
          Your browser does not support the audio element.
        </audio>
      </div>
      <img src="/files/demo/example_1/Spec_2.png" alt="Spectrogram of Stream 2">
    </div>
    <div class="demo">
      <div class="audio">
        <h4>Embedding Sequence Indices based on Diarization Estimates</h4>
      </div>
      <img src="/files/demo/example_1/plot.png" alt="Embedding Sequence Indices">
    </div>
    
  </div>




<footer>
  <p>&copy; 2023 Hassan Taherian</p>
</footer>
