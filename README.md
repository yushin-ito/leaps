# LEAPS

[![python](https://img.shields.io/badge/python-3.11-blue.svg)](https://www.python.org/)
![version](https://img.shields.io/badge/version-3.0.0-red.svg)
![stars](https://img.shields.io/github/stars/igem-tsukuba/leaps?color=yellow)
![commit-activity](https://img.shields.io/github/commit-activity/t/igem-tsukuba/leaps)
![license](https://img.shields.io/badge/license-MIT-green)

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
