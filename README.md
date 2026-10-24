# 🧬 Mutation Impact Simulator

DNA mein point mutation daalo → protein translate karo → impact classify karo (**Silent / Missense / Nonsense**), with a step-by-step trace.

> 🧠 Analogy: DNA = recipe book, mutation = typo.
> **Silent** = same meaning, **Missense** = ingredient badal gaya, **Nonsense** = recipe beech mein STOP.

## ✨ Features
- Pure-Python codon table (no Biopython needed)
- Random point-mutation simulation with reproducible `--seed`
- 🩸 **Sickle cell demo** on the real human HBB (beta-globin) gene: `GAG → GTG` (Glu → Val)
- 💥 **Frameshift demo**: 1-base deletion scrambles the whole downstream protein
- 📊 Text summary + optional bar chart (matplotlib)

## 🚀 Setup
```bash
git clone https://github.com/vighneshgaikwad59-web/mutation-impact-simulator.git
cd mutation-impact-simulator
uv pip install -r requirements.txt   # or: pip install -r requirements.txt
```

## ▶️ Usage
```bash
python mutation_simulator.py --sickle                    # sickle cell demo
python mutation_simulator.py --frameshift                # frameshift demo
python mutation_simulator.py -n 10 --seed 42             # 10 random mutations
python mutation_simulator.py -n 50 --chart impact.png    # + bar chart
python mutation_simulator.py --seq ATGGAATTTGGC -n 5     # your own sequence
```

## 🖨️ Sample output (`--sickle`)
```
Mutation
  Position   : 20 (codon 7, base 2 of 3)
  Base change: A -> T
  Codon      : GAG -> GTG
  Amino acid : Glu -> Val
  Impact     : MISSENSE ⚠️
```


## 🔮 Ideas for next version
- Load sequences from FASTA files
- Stop-loss and insertion mutations
- Streamlit sliders for live interactive mod
- e
