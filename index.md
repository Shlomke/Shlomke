<!DOCTYPE html>
<html lang="en">

  <head>

    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <meta name="description" content="">
    <meta name="author" content="">

    <title>Voice Separation with an Unknown Number of Multiple Speakers</title>

    <!-- Bootstrap core CSS -->
    <link href="src/vendor/bootstrap/css/bootstrap.min.css" rel="stylesheet">

    <!-- Custom styles for this template -->
    <link href="src/css/scrolling-nav.css" rel="stylesheet">

  </head>

  <body id="page-top">

    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top" id="mainNav">
      <div class="container">
        <!--<a class="navbar-brand js-scroll-trigger" href="#page-top">Drums & Tech</a>-->
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarResponsive">
          <ul class="navbar-nav ml-auto">
            <li class="nav-item">
              <a class="nav-link js-scroll-trigger" href="#into">Intro</a>
            </li>
            <li class="nav-item">
              <a class="nav-link js-scroll-trigger" href="#samples">Samples</a>
            </li>
            <!--<li class="nav-item">-->
              <!--<a class="nav-link js-scroll-trigger" href="#Comparison">Comparison</a>-->
            <!--</li>-->
            <li class="nav-item">
              <a class="nav-link js-scroll-trigger" href="#References">References</a>
            </li>
            <!-- <li class="nav-item">
              <a class="nav-link js-scroll-trigger" href="#contact">Contact</a>
            </li> -->
          </ul>
        </div>
      </div>
    </nav>

    <header class="bg-dark text-white">
      <div class="container text-center">
        <h1>Voice Separation with an Unknown Number of Multiple Speakers</h1>
      </div>
    </header>

    <br>  </br>


    <section id="intro">
      <div class="container">
        <div class="row">
          <div class="col-md-15 mx-auto">
            <!--<h2>Course Details</h2>-->
            <p class="lead" align="justify">
            This post presents <a href="https://arxiv.org/abs/1902.03083">"Voice Separation with an Unknown Number of Multiple Speakers"</a>,
                a deep model for multi speaker voice separation with single microphone.
                </p><p class="lead" align="justify">
                We present a new method for separating a mixed audio sequence, in which multiple voices speak simultaneously.
                The new method employs gated neural networks that are trained to separate the voices at multiple processing steps, while maintaining the speaker in each output channel fixed.
                A different model is trained for every number of possible speakers, and a the model with the largest number of speakers is employed to select the actual number of speakers in a given sample.
                Our method greatly outperforms the current state of the art, which, as we show, is not competitive for more than two speakers.
            <!--<br><img src="arch.png" alt="Italian Trulli" width="750px">-->
            <!--<br>-->
            <!--<br><img src="mul_concat.png" alt="Italian Trulli" width="750px">-->
            <!--<br>-->

              <!--<div class=”gallery”>-->
              <!--<figure class="gallery__item gallery__item&#45;&#45;1">-->
              <!--<center>-->
                <!--<img src="arch.png" class="gallery__img" alt="Image 1"  width="250px">-->
              <!--</center>-->
              <!--</figure>-->
              <!--<figure class="gallery__item gallery__item&#45;&#45;2">-->
              <!--<center>-->
                <!--<img src="mul_concat.png" class="gallery__img" alt="Image 2"  width="250px">-->
              <!--</center>-->
              <!--</figure>-->
              <!--<figure class="gallery__item gallery__item&#45;&#45;3">-->
                <!--<img src="results_table_2.png" class="gallery__img" alt="Image 3"  width="250px">-->
              <!--</figure>-->
            <!--</div>-->
    <br>  </br>
            <div class="container">
              <div class="row">
                <div class="col-md-8">

                    <h3>Architecture</h3>

                    <img src="src/arch.png" alt="Italian Trulli" width="750px">
                    <br>  </br>
                    <img src="src/mul_concat.png" alt="Italian Trulli" width="750px">
                </div>
                <div class="col-md-4">
                    <h3>Results</h3>
                    <img src="src/results_table_2.png" alt="Italian Trulli" width="400px">
                </div>

              </div>
            </div>

        </div>
      </div>
    </section>

    <section id="samples" class="bg-light">
      <div class="container">
        <div class="row">
          <div class="col-lg-13 mx-auto">
            <p class="lead" align="justify">
                <!--Here are some samples from our model for you to listen. "Mixture input" refers to the original mixed audio.-->
                <!--Conv-TasNet<sup>[1]</sup> refers to the method "Conv-TasNet: Surpassing Ideal Time–Frequency-->
                <!--Magnitude Masking for Speech Separation", DPRNN<sup>[2]</sup>-->
                <!--refer to the method "Dual-path RNN: efficient long sequence modeling for time-domain single-channel speech separation". "Ours" refer to our method. "Ground Truth" refer to the original samples.<br><br>-->
                Here are some samples from our model for you to listen:
                <ul class="lead" align="justify" >
                  <li>Mixture input - original mixed audio</li>
                  <li>Ground Truth - original separated samples</li>
                  <li>Ours - our proposed method</li>
                  <li>DPRNN<sup>[1]</sup> - refer to the method "Dual-path RNN"</li>
                  <li>Conv-TasNet<sup>[2]</sup> - refer to the method "Surpassing Ideal Time–Frequency
                Magnitude Masking for Speech Separation" </li>
                </ul>
            </p>
            <style type="text/css">
                .tg  {border-collapse:collapse;border-spacing:0;}
                .tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
                .tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
                .tg .tg-oe15{background-color:#f8f9fa;border-color:#f8f9fa;text-align:center;vertical-align:top}
                audio { width: 130px; }
            </style>


              <br>  </br>

            <center>
            <h3>WSJ-2mix DB Samples</h3>
            <p></p>
            <p></p>
            <table>
              <thead>
                <tr>
                  <th>Mixture input</th>
                  <th>Ground Truth</th>
                  <th>Ours</th>
                  <th>DPRNN</th>
                  <th>Conv-TasNet</th>
                </tr>
              </thead>
              <tbody>
                <tr style="border-top:1px solid black">
                  <td rowspan="2"><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn2/22go0106_0.742_440o030p_-0.742.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt2/22go0106_0.742_440o030p_-0.742_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours2/22go0106_0.742_440o030p_-0.742_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn2/22go0106_0.742_440o030p_-0.742_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv2/22go0106_0.742_440o030p_-0.742_s2.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt2/22go0106_0.742_440o030p_-0.742_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours2/22go0106_0.742_440o030p_-0.742_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn2/22go0106_0.742_440o030p_-0.742_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv2/22go0106_0.742_440o030p_-0.742_s1.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr style="border-top:1px solid black">
                  <td rowspan="2"><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn2/421c020j_1.394_444c020x_-1.394.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt2/421c020j_1.394_444c020x_-1.394_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours2/421c020j_1.394_444c020x_-1.394_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn2/421c020j_1.394_444c020x_-1.394_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv2/421c020j_1.394_444c020x_-1.394_s1.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt2/421c020j_1.394_444c020x_-1.394_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours2/421c020j_1.394_444c020x_-1.394_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn2/421c020j_1.394_444c020x_-1.394_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv2/421c020j_1.394_444c020x_-1.394_s2.wav"
                        type="audio/wav"></audio></td>
                </tr>
              </tbody>
            </table>



              <br>  </br>


            <h3>WSJ-3mix DB Samples</h3>
            <p></p>
            <p></p>
            <table>
              <thead>
                <tr>
                  <th>Mixture input</th>
                  <th>Ground Truth</th>
                  <th>Ours</th>
                  <th>DPRNN</th>
                  <th>Conv-TasNet</th>
                </tr>
              </thead>
              <tbody>
                <tr style="border-top:1px solid black">
                  <td rowspan="3"><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn3/422o030m_0.69126_442o030i_-0.69126_446o0312_0.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt3/422o030m_0.69126_442o030i_-0.69126_446o0312_0_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours3/422o030m_0.69126_442o030i_-0.69126_446o0312_0_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn3/422o030m_0.69126_442o030i_-0.69126_446o0312_0_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv3/422o030m_0.69126_442o030i_-0.69126_446o0312_0_s3.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt3/422o030m_0.69126_442o030i_-0.69126_446o0312_0_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours3/422o030m_0.69126_442o030i_-0.69126_446o0312_0_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn3/422o030m_0.69126_442o030i_-0.69126_446o0312_0_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv3/422o030m_0.69126_442o030i_-0.69126_446o0312_0_s1.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt3/422o030m_0.69126_442o030i_-0.69126_446o0312_0_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours3/422o030m_0.69126_442o030i_-0.69126_446o0312_0_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn3/422o030m_0.69126_442o030i_-0.69126_446o0312_0_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv3/422o030m_0.69126_442o030i_-0.69126_446o0312_0_s2.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr style="border-top:1px solid black">
                  <td rowspan="3"><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn3/422c0201_0.14718_441o0313_-0.14718_447o030u_0.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt3/422c0201_0.14718_441o0313_-0.14718_447o030u_0_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours3/422c0201_0.14718_441o0313_-0.14718_447o030u_0_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn3/422c0201_0.14718_441o0313_-0.14718_447o030u_0_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv3/422c0201_0.14718_441o0313_-0.14718_447o030u_0_s2.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt3/422c0201_0.14718_441o0313_-0.14718_447o030u_0_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours3/422c0201_0.14718_441o0313_-0.14718_447o030u_0_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn3/422c0201_0.14718_441o0313_-0.14718_447o030u_0_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv3/422c0201_0.14718_441o0313_-0.14718_447o030u_0_s3.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt3/422c0201_0.14718_441o0313_-0.14718_447o030u_0_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours3/422c0201_0.14718_441o0313_-0.14718_447o030u_0_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn3/422c0201_0.14718_441o0313_-0.14718_447o030u_0_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv3/422c0201_0.14718_441o0313_-0.14718_447o030u_0_s1.wav"
                        type="audio/wav"></audio></td>
                </tr>
              </tbody>
            </table>

              <br>  </br>


            <h3>WSJ-4mix DB Samples</h3>
            <p></p>
            <p></p>
            <table>
              <thead>
                <tr>
                  <th>Mixture input</th>
                  <th>Ground Truth</th>
                  <th>Ours</th>
                  <th>DPRNN</th>
                  <th>Conv-TasNet</th>
                </tr>
              </thead>
              <tbody>
                <tr style="border-top:1px solid black">
                  <td rowspan="4"><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s1.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s2.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s3.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv4/22go0107_2.411_440o030k_1.6598_446o030m_-1.6598_421o030r_-2.411_s4.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr style="border-top:1px solid black">
                  <td rowspan="4"><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s1.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s2.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s4.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv4/22ho010z_0.70341_053o020b_0.96111_444c0210_-0.96111_050c0107_-0.70341_s3.wav"
                        type="audio/wav"></audio></td>
                </tr>
              </tbody>
            </table>

              <br>  </br>


            <h3>WSJ-5mix DB Samples</h3>
            <p></p>
            <p></p>
            <table>
              <thead>
                <tr>
                  <th>Mixture input</th>
                  <th>Ground Truth</th>
                  <th>Ours</th>
                  <th>DPRNN</th>
                  <th>Conv-TasNet</th>
                </tr>
              </thead>
              <tbody>
                <tr style="border-top:1px solid black">
                  <td rowspan="5"><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s2.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s4.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s5.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s3.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s5.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s5.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s5.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv5/22gc010q_1.9223_052c010w_0.54576_445o0311_-0.54576_050o020d_-1.9223_447c0210_0_s1.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr style="border-top:1px solid black">
                  <td rowspan="5"><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s2.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s4.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s5.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s3.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s5.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s5.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/gt5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/ours5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/dprnn5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s5.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/conv5/443o030v_2.2076_441c020w_1.508_22hc010q_-1.508_053o020z_-2.2076_440o030x_0_s1.wav"
                        type="audio/wav"></audio></td>
                </tr>
              </tbody>
            </table>

              <br>

            <h3>WSJ-2mix DB Tested on WSJ-5mix Speakers Model</h3>
            <p align="justify">Results for model that train on WSJ-5mix and tested on WSJ-2mix. Results suggests that all model have managed to separate the two speakers. However, compared to DPRNN and ConvTasNet which output noise and mixed signals in the rest of the output channels, our model produce silence with significantly less artifacts.  </p>
            <p></p>
            <table>
              <thead>
                <tr>
                  <th>Mixture input</th>
                  <th>Ground Truth</th>
                  <th>Ours</th>
                  <th>DPRNN</th>
                  <th>Conv-TasNet</th>
                </tr>
              </thead>
              <tbody>
                <tr style="border-top:1px solid black">
                  <td rowspan="5"><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/mix/22gc010l_0.11746_444o030o_-0.11746.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/gt/22gc010l_0.11746_444o030o_-0.11746_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/ours/22gc010l_0.11746_444o030o_-0.11746_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/dprnn/22gc010l_0.11746_444o030o_-0.11746_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/convtasnet/22gc010l_0.11746_444o030o_-0.11746_s4.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/gt/22gc010l_0.11746_444o030o_-0.11746_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/ours/22gc010l_0.11746_444o030o_-0.11746_s5.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/dprnn/22gc010l_0.11746_444o030o_-0.11746_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/convtasnet/22gc010l_0.11746_444o030o_-0.11746_s3.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <!--<td><audio controls class="audio-player" preload="metadata" style="width: 180px;">-->
                      <!--<source src=-->
                        <!--type="audio/wav"></audio></td>-->
                  <td> </td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/ours/22gc010l_0.11746_444o030o_-0.11746_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/dprnn/22gc010l_0.11746_444o030o_-0.11746_s1.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/convtasnet/22gc010l_0.11746_444o030o_-0.11746_s1.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <!--<td><audio controls class="audio-player" preload="metadata" style="width: 180px;">-->
                      <!--<source src=-->
                        <!--type="audio/wav"></audio></td>-->
                  <td> </td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/ours/22gc010l_0.11746_444o030o_-0.11746_s2.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/dprnn/22gc010l_0.11746_444o030o_-0.11746_s4.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/convtasnet/22gc010l_0.11746_444o030o_-0.11746_s2.wav"
                        type="audio/wav"></audio></td>
                </tr>
                <tr>
                  <!--<td><audio controls class="audio-player" preload="metadata" style="width: 180px;">-->
                      <!--<source src=-->
                        <!--type="audio/wav"></audio></td>-->
                  <td> </td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/ours/22gc010l_0.11746_444o030o_-0.11746_s3.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/dprnn/22gc010l_0.11746_444o030o_-0.11746_s5.wav"
                        type="audio/wav"></audio></td>
                  <td><audio controls class="audio-player" preload="metadata" style="width: 180px;">
                      <source src="src/samples/crossdbs/convtasnet/22gc010l_0.11746_444o030o_-0.11746_s5.wav"
                        type="audio/wav"></audio></td>
                </tr>               
              </tbody>
            </table>
			</center>                        
          </div>
        </div>
      </div>
    </section>    
	</center>
    <section id="code" class="bg-light">
    	<center><h3>Code</h3></center>
    	<div class="container">
	    	<div class="row">
	    		<p class="lead" align="justify"> Code will be available under the following repo: </p>
	    	</div>
	    </div>
    </section>

    <section id="Reference" class="bg-white">
      <center><h3>References</h3></center>

      <div class="container">
        <div class="row">
          <div class="col-lg-13 mx-auto">
              <p class="lead" align="justify">
                    <p class="lead" align="justify">
                        [1]. Luo, Yi, and Nima Mesgarani. "Conv-tasnet: Surpassing ideal time–frequency magnitude masking for speech separation." IEEE/ACM transactions on audio, speech, and language processing 27.8 (2019): 1256-1266.
                    </p>
                    <p class="lead" align="justify">
                        [2]. Luo, Yi, Zhuo Chen, and Takuya Yoshioka. "Dual-path RNN: efficient long sequence modeling for time-domain single-channel speech separation." ICASSP (2019).
                    </p>
              </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="py-5 bg-dark">
      <div class="container">
        <!-- <p class="m-0 text-center text-white">Copyright &copy; Your Website 2017</p> -->
      </div>
      <!-- /.container -->
    </footer>

    <!-- Bootstrap core JavaScript -->
    <script src="src/vendor/jquery/jquery.min.js"></script>
    <script src="src/vendor/bootstrap/js/bootstrap.bundle.min.js"></script>

    <!-- Plugin JavaScript -->
    <script src="src/vendor/jquery-easing/jquery.easing.min.js"></script>

    <!-- Custom JavaScript for this theme -->
    <script src="src/js/scrolling-nav.js"></script>

  </body>
</html>