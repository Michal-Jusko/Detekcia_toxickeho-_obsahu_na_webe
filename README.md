# Detekcia_toxickeho-_obsahu_na_webe
Repository for notebooks for BP
# Detekcia toxického obsahu na webe – Experimenty k bakalárskej práci

Tento repozitár obsahuje Jupyter notebooky, ktoré som vytvoril počas riešenia svojej bakalárskej práce
na tému **„Detekcia toxického obsahu na webe“** (Michal Jusko, 2025, FEI TUKE).

Cieľom bolo otestovať viacero prístupov na klasifikáciu komentárov ako toxických alebo netoxických –
a to v rôznych jazykoch (slovenčina, angličtina) a pomocou rôznych typov modelov
(monojazyčné, multilingválne, aj LLM modely ako ChatGPT).

## Prehľad notebookov

### Slovenský model
- `final-slovak-bert.ipynb`: Tréning a vyhodnotenie SlovakBERT modelu na slovenskom datasete (binárna klasifikácia)

### Anglické modely
- `final-toxic-bert-binar.ipynb`: ToxicBERT trénovaný na anglických dátach (binárna klasifikácia)
- `final-toxic-bert-miltilabel.ipynb`: Multilabel klasifikácia anglických komentárov (okrem severe_toxicity)

###  Multilingválny model
- `final-xml-roberta.ipynb`: Tréning modelu XLM-RoBERTa na kombinovaných EN+SK dátach


### Modely ChatGPT
- `chatgpt-zero-shot.ipynb`: Zero-shot klasifikácia komentárov cez OpenAI ChatGPT
- `chatgpt-few-shot.ipynb`: Few-shot klasifikácia s niekoľkými príkladmi v promptoch

## Spustenie a knižnice
Všetky notebooky sú kompatibilné s Google Colab, Kaggle alebo bežným Python prostredím (odporúčaný Python 3.10+).

Použité knižnice:
- `transformers`, `datasets`, `scikit-learn`
- `pandas`, `matplotlib`, `seaborn`
- `openai` (pre ChatGPT časť)

Niektoré notebooky využívajú Hugging Face datasets alebo OpenAI API – je potrebné mať vlastný API kľúč.

## Výstupy
Vo väčšine notebookov sú súčasťou aj:
- klasifikačné metriky (F1, precision, ...),
- vizualizácie (lossy, accuracy,...),
- exporty do CSV alebo PNG (`./results/` priečinok),
- zakomentované pokusy alebo poznámky počas ladenia

## Poznámky autora
Počas práce som testoval viacero nastavení modelov (napr. rôzne prahy, sampling, veľkosť dávok pri trénovaní),
skúšal som aj veľké modely (napr. `xlm-roberta-large`), ale kvôli výpočtovým obmedzeniam som ostal pri základných verziách.
Komentáre v notebookoch by mali vysvetliť moje rozhodnutia a testované alternatívy.

## Licencia
Notebooky a skripty sú určené výhradne pre akademické účely (FEI TUKE, 2025).
