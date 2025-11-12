# LEAPS

![version](https://img.shields.io/badge/version-3.0.0-red.svg)
![stars](https://img.shields.io/github/stars/igem-tsukuba/leaps?color=yellow)
![commit-activity](https://img.shields.io/github/commit-activity/t/igem-tsukuba/leaps)
![license](https://img.shields.io/badge/license-MIT-green)

<br/>

## 📖 Overview
In this study, we developed a novel machine learning model named "LEAPS" that enables efficient protein function improvement from limited datasets. Conventional protein engineering requires large-scale experimental data, extensive expertise, and prolonged trial-and-error processes, making research execution heavily dependent on institutional funding and human resources. Consequently, significant barriers remain for student teams and small-scale laboratories attempting to engage in protein engineering. LEAPS substantially reduces these constraints and provides an accessible environment for researchers to perform multi-objective optimization of proteins. This model enables student teams participating in iGEM and researchers with limited resources to undertake functional improvements such as enzymatic activity enhancement and antibody affinity optimization, dramatically expanding research possibilities. This model has the potential to promote data-driven protein engineering and accelerate research and development across all fields of life sciences.

<br/>

## 📚 Background

### Importance of Protein Function Improvement and Multi-Objective Optimization
Proteins play a central role in governing biological phenomena at the molecular level. At the same time, they serve as fundamental tools in medical and biological research and are positioned as key components in the emerging fields of synthetic biology and biomanufacturing. Therefore, understanding protein function and engineering proteins for specific purposes represents an extremely important research challenge spanning from basic science to applied development.
Particularly in practical applications, it is necessary to simultaneously optimize multiple properties rather than a single characteristic, such as enzymatic activity, substrate specificity, and stability. For example, in industrially utilized enzymes, achieving both stability under high-temperature processes and high enzymatic activity directly contributes to the reduction of production costs. In therapeutic antibodies, the combination of high binding affinity to target antigens and thermodynamic stability required for long-term storage and predictable in vivo behavior is essential for ensuring therapeutic efficacy and quality. Thus, multi-objective optimization of proteins—improving multiple properties simultaneously-is indispensable for creating proteins suited to specific purposes.

<br/>

### Challenges in Existing Protein Improvement Methods
However, achieving efficient multi-objective optimization remains difficult with conventional protein engineering approaches. The major existing methods face the following challenges:

- Directed Evolution: 
This method obtains proteins with desired functions through repeated random mutagenesis and selection (screening). However, library construction and evaluation require enormous numbers of experiments, consuming substantial time and cost. Furthermore, reliance on sequential mutagenesis, such as single amino acid substitutions, makes it difficult to explore sequence spaces where multiple mutations cooperatively express function (epistatic interactions), leading to entrapment in local optima.

- Rational Design: 
This approach designs amino acid sequences based on protein structure information and knowledge of functional mechanisms. Its application is restricted due to the necessity of specialized knowledge and structural information. Moreover, precisely engineering a solution that simultaneously addresses factors influencing a plurality of properties presents a significant challenge.

To address these challenges, it is necessary to develop new methodologies for efficient and comprehensive multi-objective optimization.

<br/>

### The Barrier of Vast Sequence Space
A fundamental difficulty in protein improvement lies in the astronomically large sequence space to be explored. Even for a tripeptide, with 20 possible amino acids at each position, the number of combinations reaches 20^3 = 8,000. For a protein composed of 250 amino acid residues, the total number of theoretically possible sequences reaches 20^250 ≈ 1.81 × 10^325. This number far exceeds even the number of atoms in the observable universe, making exhaustive exploration of all sequences impossible.

<br/>

### Machine Learning in Protein Engineering
As an approach to efficiently explore this vast sequence space, machine learning applications have recently attracted significant attention. Machine learning models are expected to predict the function of unknown sequences or generate sequences with desired functions by learning complex relationships between amino acid sequences and functions from data. This capability holds great potential for achieving multi-objective optimization of proteins. However, many existing models still require large-scale experimental datasets for high-accuracy prediction and design. This "high data requirement" presents a new barrier to entry for student teams and small-scale laboratories attempting to utilize machine learning. Therefore, development of new machine learning methods that can effectively learn from small datasets and enable high-accuracy multi-objective optimization is necessary.

<br/>

## 💡 Solution

### Utilization of Protein Language Models (pLM)
To address this challenge, we focused on Protein Language Models (pLMs). pLMs are based on the same principles as Large Language Models (LLMs) typified by ChatGPT and Gemini. Just as LLMs learn word occurrence patterns and context from vast amounts of text data to intrinsically acquire natural language grammar, pLMs treat protein amino acid sequences as "language." Proteins are polymers (corresponds to sentences) in which 20 types of amino acids (corresponds to words) are linked with a clear direction from N-terminus to C-terminus. By learning from billions of known amino acid sequences, pLMs acquire universal "grammar" for protein viability—the rules governing amino acid combinations and inter-residue interactions.

<br/>

### Our Method: The LEAPS Workflow

We developed "LEAPS", a unique machine learning method integrating predictive and generative models to achieve multi-objective protein optimization from small datasets. LEAPS performs “in silico-complete” protein improvement through the following workflow:

1. Generate novel sequences using a generative model
2. Screen the output sequences for high-function variants using a predictive model
3. Train the generative model on the selected high-function sequences
4. Return to step 1, where the generative model generates high-function sequences

<br/>

## 🚀 Usage

1. Clone this repository

```bash
git clone https://github.com/igem-tsukuba/leaps.git
```

<br/>

2. Move to the directory

```bash
cd leaps
```

<br/>

3. Create a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate
```

<br/>

3. Install the packages

```bash
pip install -r requirements.txt
```

<br/>

> [!NOTE]
> Place [foldseek](https://github.com/steineggerlab/foldseek) and [plmc](https://github.com/debbiemarkslab/plmc) in the `bin` directory.


<br/>
<br/>

## ⚡️ Quick Start

```bash
$ python main.py
```

<br/>
<br/>

## 📂 Structure

```
leaps/
├── bin/
│   ├── foldseek
│   └── plmc
├── data/
│   └── input.csv
├── notebooks/
│   └── example.ipynb
├── runs/
├── src/
│   ├── config/
│   ├── early_stopper/
│   ├── evaluator/
│   ├── generator/
│   ├── predictor/
│   ├── runner/
│   ├── sampler/
│   └── state/
├── .gitattributes
├── .gitignore
├── .python-version
├── config.yaml
├── CONTRIBUTING.md
├── LICENSE     
├── main.py
├── pyproject.toml
├── README.md
├── requirements.txt
└── uv.lock
```

<br/>
<br/>

## 🤝 Contributer

<a href="https://github.com/yushin-ito">
  <img  src="https://avatars.githubusercontent.com/u/75526539?s=48&v=4" width="64px">
</a>

<br/>
<br/>

## 📜 LICENSE

[MIT LICENSE](LICENSE)
