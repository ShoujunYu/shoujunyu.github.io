---
permalink: /
title: "Biography"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<div id="biography"></div>

I am currently a Ph.D. student in Pattern Recognition and Intelligent Systems at the Shenzhen Institutes of Advanced Technology (SIAT), Chinese Academy of Sciences (CAS).

My research focuses on **medical image analysis, magnetic resonance imaging (MRI), and artificial intelligence**, with particular interests in diffusion MRI, brain microstructure imaging, and deep learning-based medical image reconstruction.

My current work involves developing computational methods for diffusion MRI analysis, neural fiber tractography, and fine-scale neuroanatomical imaging.

---

<h2 id="research">Research</h2>

### Research Interests

- Medical Image Analysis
- Diffusion MRI and Brain Microstructure Imaging
- Deep Learning for MRI Reconstruction
- Brain Tractography and Cranial Nerve Imaging
- Artificial Intelligence in Healthcare

### Research Areas

**Diffusion MRI and Brain Microstructure Imaging**

Developing computational methods for diffusion MRI reconstruction, microstructural characterization, and fine-scale neural imaging.

**Deep Learning for Fiber Tractography**

Investigating deep learning-based methods for reconstructing neural fiber trajectories from diffusion MRI.

**AI for Medical Image Analysis**

Developing artificial intelligence methods for medical image interpretation, segmentation, and quantitative analysis.

---

<h2 id="publications">Publications</h2>

<style>
.pub-entry {
  margin-left: 1.5rem;
  margin-bottom: 1.2rem;
  line-height: 1.55;
}

.pub-entry a {
  color: #07501b;
  text-decoration: underline;
}
</style>

<div class="pub-list">

{% assign sorted_pubs = site.publications | sort: "date" | reverse %}
{% assign current_year = "" %}

{% for pub in sorted_pubs %}
  {% assign pub_year = pub.date | date: "%Y" %}

  {% if pub_year != current_year %}
    <h3>{{ pub_year }}</h3>
    {% assign current_year = pub_year %}
  {% endif %}

  <p class="pub-entry">
    {{ pub.authors }}.
    <strong>{{ pub.title }}</strong>.
    <em>{{ pub.venue }}</em>.

    {% if pub.pdfurl %}
      <a href="{{ pub.pdfurl }}">[pdf]</a>
    {% endif %}

    {% if pub.paperurl %}
      <a href="{{ pub.paperurl }}">[paper]</a>
    {% endif %}

    {% if pub.codeurl %}
      <a href="{{ pub.codeurl }}">[code]</a>
    {% endif %}

    {% if pub.dataurl %}
      <a href="{{ pub.dataurl }}">[dataset]</a>
    {% endif %}

    {% if pub.dataseturl %}
      <a href="{{ pub.dataseturl }}">[dataset]</a>
    {% endif %}
  </p>
{% endfor %}

</div>

---

<h2 id="cv">Curriculum Vitae</h2>

### Education

**2023 – 2027 (Expected)**

Ph.D. in Pattern Recognition and Intelligent Systems  
University of Chinese Academy of Sciences (UCAS)  
Shenzhen Institutes of Advanced Technology (SIAT)

**2020 – 2023**

M.S. in Electronic Information Engineering  
Southern Medical University

**2016 – 2020**

B.S. in Biomedical Engineering (Medical Imaging Engineering)  
Southern Medical University

### Research Expertise

- **MRI Reconstruction:** k-space reconstruction, inverse problems, and image quality assessment.
- **Diffusion MRI:** Diffusion signal modeling, spherical harmonics, and microstructural analysis.
- **Deep Learning:** Generative modeling, rectified flow, and 3D medical image segmentation.
- **Neuroimaging:** Fiber tractography, brain connectivity analysis, and cranial nerve imaging.

---

<h2 id="contact">Contact</h2>

**Email:** [sj.yu1@siat.ac.cn](mailto:sj.yu1@siat.ac.cn)

**GitHub:** [ShoujunYu](https://github.com/ShoujunYu)

**ORCID:** [0000-0001-9865-8190](https://orcid.org/0000-0001-9865-8190)
