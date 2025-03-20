---
layout: single
toc: false
classes: wide
sidebar:  
  - title: " "   
    image: /assets/images/logo.png
    image_alt: "image"
    nav: "docs"
---


# Program 

## Saturday, 15th March, 2025
<table>
    <tr>
        <td width="180">08:45 – 09:00</td>
        <td><b>Registration</b></td>
    </tr>
    <tr>
        <td>09:00 – 10:30</td>
        <td><p><b>Session 1 (Session Chair: TBD)</b></p>
          <il>
          <li> <b> Emanuele Bellini </b> (Technology Innovation Institute, UAE)  <br />  <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Bellini_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a>     
            <i> Hands-on cryptanalysis - The DojoCrypt platform and an introduction to CLAASP </i>
            <details>
    <summary> Abstract </summary>
    In this tutorial, we introduce DojoCrypt, an experimental cloud-based platform designed to streamline cryptography and cryptanalysis research and development. Offering a pre-configured environment with powerful tools—including cryptanalysis frameworks (e.g. CLAASP, TAGADA, CASCADA, CryptoSMT), hacking utilities (e.g. John-the-Reaper, Hashcat), mathematical libraries (e.g. SageMath), and AI-powered solutions—DojoCrypt eliminates the complexity of software setup and resource management. 
To showcase DojoCrypt’s capabilities for both teaching and research, we demonstrate its integration with the CLAASP library—a SageMath-based suite designed to simplify the analysis of symmetric primitives. After a brief overview of CLAASP, we implement a basic toy cipher and execute various cryptanalysis routines, such as statistical testing, linear/differential trail searches, algebraic modeling, and result visualization, all achieved in a few lines of code.
            </details> <br /> 
            </li>               
          <li> <b> Juan Grados </b> (Technology Innovation Institute, UAE) <br />  <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Grados_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a> 
            <i> CLAASP 3.0: automated search of impossible differential, differential-linear and algebraic distinguishers </i>
            <details>
    <summary> Abstract </summary>
    The search for algebraic, impossible differential, and differential-linear distinguishers is a key topic in symmetric cryptanalysis. Existing automated tools are often highly specialized or lack support for one of these types of distinguishers. In this talk, we will demonstrate through practical examples how the latest version of CLAASP can automatically search for impossible differential and differential-linear distinguishers using state-of-the-art techniques. Specifically, we will showcase methods that use truncated deterministic differentials to find these kind of distinguishers. Additionally, we will show how CLAASP can automatically search for algebraic distinguishers through the use of techniques based on the three-subset division property. 
            </details> <br /> 
            </li>                
          <li> <b> David Gerault </b> (Technology Innovation Institute, UAE) <br />  <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Gerault_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a> 
            <i> Automating Neural Cryptanalysis  </i>
            <details>
    <summary> Abstract </summary>
    At CRYPTO 2019, Aron Gohr proposed neural networks as a tool for the cryptanalysis of block ciphers. His neural distinguishers are trained to learn to recognize the distribution induced by the encryption of plaintext pairs with a given XOR difference from that of random pairs. In his seminal work, these distinguishers were used to build state-of-the-art, practical key recoveries on round-reduced SPECK32.
At FSE 2023, we presented the AutoND framework, which aims at automating the process of neural cryptanalysis, by eliminating the tedious process of hyperparameters tuning and other cipher-specific optimizations. In this talk, we present the tool, how to unleash its full potential through CLAASP, and how to integrate it with other similar libraries.
            </details> <br /> 
            </li>
          </il>
        </td>
    </tr>
    <tr>
        <td>10:30 – 11:00</td>
        <td><b>Coffee Break</b></td>
    </tr>
      <tr>
        <td>11:00 – 12:30</td>
        <td><p><b>Session 2 (Session Chair: TBD) </b></p>
          <il>
          <li> <b> Loïc Rouquette </b> (EPITA Research Laboratory - LRE, France) <br />  <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Rouquette_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a> 
            <i> TAGADA, an automated tool for differential cryptanalysis </i>
            <details>
            <summary> Abstract </summary>
            When designing new symmetric block ciphers, assessing their resistance against differential attacks is crucial. A common modern approach is to evaluate truncated differential characteristics (TDCs) and differential characteristics (DCs) to bound the probability of differential distinguishers. Traditionally, these TDCs (or DCs) are computed using declarative models—via CP, SAT, or ILP—whose manual design is complex, error-prone, and demands deep expertise in both cryptography and solver technologies. In this talk, we will discuss Tagada (Tool for Automatic Generation of Abstraction-based Differential Attacks), a generic tool that automatically generates these models from an operational description of the cipher using a bipartite Directed Acyclic Graphs (DAGs) representation. Tagada provides a set of built-in functionalities that allows one to compute TDCs and DCs by giving only the description of the cipher. The talk will be focused on the operation and usage of Tagada, the results we previously had, the strengths and limitations of the library, and the possible improvements.
            </details> <br /> 
            </li>
          <li> <b> Hosein Hadipour </b> (Ruhr University Bochum, Germany) <br />  <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Hadipour_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a> 
            <i> Automating Cryptanalysis: Automated Reasoning and Structural Links Between Attacks </i>
            <details>
            <summary> Abstract </summary>
  In this talk, I will discuss how automated reasoning techniques can be applied to efficiently explore cryptanalytic attacks. As an example, I will demonstrate how the guess-and-determine problem can be formulated as a constraint satisfaction or optimization problem. I will then examine the structural links between different cryptanalytic techniques and how these relationships can be leveraged to enhance the efficiency of attack discovery. In particular, I will illustrate how the connection between zero-correlation (resp. boomerang) and integral (resp. differential-linear) attacks enables the use of more efficient methods from one technique to identify the other.
            </details> <br /> 
          </li>
          </il>
        </td>
    </tr>
      <tr>
        <td>12:00 – 13:00</td>
        <td><b>Lunch </b></td>
    </tr>
      <tr>
        <td>13:00 – 15:00</td>
        <td><p><b>Session 3 (Session Chair: TBD) </b></p>
          <il>
          <li> <b> María Naya-Plasencia </b> (Inria, France) <br />  <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Naya_Plasencia_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a> 
            <i>Symmetric Cryptanalysis State-of-the-Art and Future: Towards a Generalization of Cryptanalysis techniques </i>
            <details>
            <summary> Abstract </summary>
  We will briefly present an overview of the context of symmetric cryptanalysis and its development in the last few years. We will discuss how a reference algorithmic framework for the different attacks and techniques would be very useful, and some of the works that have been done in this direction, plus some of the main many open problems yet to solve.
            </details> <br /> 
          </li>
          <li>  <b> Ling Song </b> (Jinan University, China) <br />  <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Song_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a> 
            <i> The key recovery in differential attacks and the automated models </i>
            <details>
            <summary> Abstract </summary>
  In differential cryptanalysis, we identify three critical factors influencing the efficiency of key recovery attacks. First, permitting misaligned boundaries of the distinguisher can expand the search space for the attack, thereby potentially enhancing its effectiveness. Second, probabilistic extensions of the distinguisher—specifically, allowing forward/backward propagation with probabilities below 1 during key recovery—can yield comparable advantages. Third, the strategy of pre-guessing key bits has a significant impact on time complexity, necessitating an optimized guessing strategy to minimize computational costs. To enhance differential cryptanalysis, we propose an automated search framework for byte-oriented block ciphers. This framework simultaneously determines the optimal attack complexity, identifies the used distinguisher, and configures attack parameters in a unified process. We validate our approach by applying it to Deoxys-BC-384 and AES-256, achieving significantly improved results compared to prior works.
            </details>  <br /> 
          </li>
          <li>  <b> Léo Perrin </b> (Inria, France) <br />   <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Perrin_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a> 
            <i>What happens when you *don't* have tools? The case of algebraic cryptanalysis </i>
            <details>
            <summary> Abstract </summary>
  Generic tools are a necessity if we are to ever provide convincing and simple security arguments. In this talk however, we will discuss another crucial use case for cryptanalysis tools : prototyping. During the design phase of a primitive, it is necessary to be able to quickly check if a design direction is promising. Similarly, when attempting a first cryptanalysis, we need to be able to easily test cryptographic properties. This discussion will be greatly informed by a specific case : that of "algebraic attacks", at least the Gröbner basis-based kind. We will see that the absence of convenient tools to investigate them is a problem, and sketch some ideas for what such tools might provide.
            </details>  <br /> 
          </li>
          <li>  <b> Patrick Derbez </b> (Centre Inria de l'Université de Rennes, France) <br /> <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Derbez_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a> 
                      <i> Minimalist model for Impossible Differentials </i>
                      <details>
                      <summary> Abstract </summary>
            In this talk I will present a new MILP modelling to find impossible differential (ID) distinguishers and attacks. Standard models for ID are negative models, in the sense that a differential is impossible if and only if the model has no solution. Our new modelling technique focuses on probable ID, differentials that are probably impossible. While this might lead to false positive, the main advantage is that searching for such probable ID can be achieved through a positive model. This facilitates the search for the best impossible differential attacks without first exhausting all possible ID distinguishers on a target.
            </details>  <br /> 
          </li>
          </il>
        </td>
    </tr>
      <tr>
        <td>15:00 – 15:30</td>
        <td><b>Coffee Break </b></td>
    </tr>
      <tr>
        <td>15:30 – 17:30</td>
        <td><p><b>Session 4 (Session Chair: TBD) </b></p>
          <il>
          <li>  <b> Shaowei Cai </b> (Institute of Software, Chinese Academy of Sciences, China) <br /> <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Cai_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a> 
            <i> Progress on SAT and MILP Solving </i>
            <details>
            <summary> Abstract </summary>
  Solvers for Boolean Satisfiability (SAT) and Mixed Integer Linear
Programming (MILP) are key tools for Symmetric-Key
Cryptanalysis Automation. In this talk, I will introduce our recent
progress on SAT solving and MILP solving, including hybrid solvers for
SAT, local search for MILP, and finally parallel solvers for both SAT
and MILP. The SAT solvers based on these techniques have won several
gold medals in SAT competitions and the Best Paper award in SAT 2021,
while the MILP solver has established the latest record for many
challenging instances in MIPLIB and the Best Paper in CP 2024.
            </details>   <br /> 
          </li>
          <li>  <b> Maria Eichlseder </b> (Graz University of Technology, Austria) <br /> <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Eichlseder_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a> 
            <i> Challenges in tool-based cryptanalysis </i>
            <details>
            <summary> Abstract </summary>
  We will take a bird's-eye view on the progress made in automated, 
tool-based cryptanalysis in the last years, and identify challenges for 
the area going forward.
We will discuss how (and why) different tools model ciphers as well as 
attack flows, and what this means for efforts towards a more uniform 
platform for automated cryptanalysis.
            </details>  <br /> 
          </li>
          <li>  <b> Yosuke Todo </b> (NTT Social Informatics Laboratories, Japan) <br /> <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Todo_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a> 
            <i>Improved Cryptanalysis of ChaCha: Beating PNBs with Bit Puncturing </i>
            <details>
            <summary> Abstract </summary>
  ChaCha is one of the most important stream ciphers.
ChaCha has been actively analysed, but most of the attacks are based on PNBs, which was proposed at FSE 2008.
Although some improvements have been proposed within the framework of PNBs, no fundamental alternative has been proposed that replaces PNBs.
We emphasize that PNBs are a kind of experimentally blackbox analysis.
In other words, so far, cryptographers' in-depth analysis has not been able to produce results that surpass experimental blackbox analysis due to the complex behaviour of ARX.
In this talk, we propose the first successful alternative to PNBs to our knowledge.
Inspired by a puncturing technique proposed at Eurocrypt 2024, we propose a new theory and tools for analysing ChaCha.
Unlike PNBs, our method can provide theoretical evaluation without relying on experimental blackbox analysis.
As a result, we improve the state-of-the-art cryptanalysis against ChaCha (and Salsa).
We also discuss what is the room of further improvements.
            </details>  <br /> 
          </li>
          <li>  <b> Thomas Peyrin </b> (Nanyang Technological University, Singapore) <br />  <a href="https://skcamworkshop.github.io/skcam2025/assets/docs/slides/Peyrin_slides.pdf"><img src="https://thomaspeyrin.github.io/web/assets/images/pdf_icon_small.png" alt="slides"></a> 
            <i> Open Cryptanalysis Platform (OCP) -  A New Collaborative Effort for Automated Cryptanalysis </i>
            <details>
            <summary> Abstract </summary>
  In this talk, we will present an open-source tool to conduct automated cryptanalysis, named Open Cryptanalysis Platform (OCP). The goal of OCP is to provide a common platform for the community to implement/test/use/benchmark automated cryptanalysis techniques, with a focus on ease-of-use and modularity for future usages.  We will explain the basic architecture of OCP and its rationale, as well as currently implemented functionalities. Finally, we will review future short-term and long-term plans and how the community can contribute to OCP. The goal of the platform is to be collaborative, so we welcome all comments on what part of OCP should be modified, or what crucial functionality is needed in priority.
            </details>  <br /> 
          </li>  
          </il>
        </td>
    </tr>
    <tr>
        <td>17:30 – 18:15</td>
        <td><b>Discussions </b></td>
    </tr>
</table>




