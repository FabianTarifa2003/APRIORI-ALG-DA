# APRIORI ALG DA

## Përshkrimi
Ky projekt përmban një implementim të algoritmit Apriori për zbulimin e bashkësive të shpeshta në të dhëna transaksionale.

## Si ta ekzekutoni

### Përdorimi i GitHub dhe Binder

1. **Klono repository-n:**
   ```bash
   git clone https://github.com/username/repo-name.git
   cd repo-name
   ```

2. **Hap notebook-un në Jupyter:**
   - Sigurohuni që keni instaluar Jupyter Notebook. Nëse jo, instaloni me:
     ```bash
     pip install notebook
     ```
   - Hapni Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
   - Në shfletuesin që hapet, klikoni mbi `detyra.ipynb` për ta hapur dhe ekzekutuar.

3. **Përdorimi i Binder:**
   - Shko te [mybinder.org](https://mybinder.org/).
   - Vendos URL-në e repository-t tuaj të GitHub-it në fushën e duhur.
   - Kliko "Launch" dhe prit që Binder të përgatisë mjedisin për ekzekutimin e notebook-ut.
   - Pasi mjedisi të jetë gati, klikoni mbi `detrya.ipynb` për ta hapur dhe ekzekutuar.

## Algoritmi Apriori

Algoritmi Apriori është një metodë për zbulimin e bashkësive të shpeshta dhe rregullave të shoqërimit në të dhëna transaksionale. Më poshtë janë hapat kryesorë të algoritmit:

### Hapat e Algoritmit Apriori

1. **Gjetja e Bashkësive të Shpeshta:**
   - Fillimisht, identifikohen të gjitha bashkësitë e artikujve që kanë një mbështetje (support) të lartë, ku mbështetja është numri i transaksioneve që përmbajnë bashkësinë.
   - Këto bashkësi të shpeshta përdoren për të gjeneruar bashkësi më të mëdha që gjithashtu kanë mbështetje të lartë.

2. **Gjenerimi i Rregullave të Shoqërimit:**
   - Nga bashkësitë e shpeshta, gjenerohen rregullat e shoqërimit që plotësojnë një prag të caktuar për besueshmërinë (confidence), ku besueshmëria është probabiliteti që një bashkësi artikujsh të përmbajë një artikull të caktuar.

### Formula për Mbështetjen dhe Besueshmërinë

- **Mbështetja (Support):**
  Mbështetja e një bashkësie artikujsh \\( X \\) është përqindja e transaksioneve që përmbajnë \\( X \\).
  \\[
  \text{Support}(X) = \frac{\text{Numri i transaksioneve që përmbajnë } X}{\text{Numri total i transaksioneve}}
  \\]

- **Besueshmëria (Confidence):**
  Besueshmëria e një rregulli \\( X \rightarrow Y \\) është përqindja e transaksioneve që përmbajnë \\( Y \\) duke pasur parasysh që ato përmbajnë \\( X \\).
  \\[
  \text{Confidence}(X \rightarrow Y) = \frac{\text{Support}(X \cup Y)}{\text{Support}(X)}
  \\]

### Shembull

Në një dyqan, nëse shumë klientë që blejnë qumësht gjithashtu blejnë bukë, algoritmi Apriori mund të identifikojë këtë lidhje dhe të gjenerojë një rregull të shoqërimit si \\( \text{qumësht} \rightarrow \text{bukë} \\).

#### Hapi 1: Gjetja e Bashkësive të Shpeshta

- Supozojmë se kemi këto transaksione:
  ```
  T1: {qumësht, bukë, vezë}
  T2: {qumësht, bukë}
  T3: {bukë, birrë}
  T4: {qumësht, bukë, birrë}
  T5: {bukë, vezë}
  ```

- Me pragun e mbështetjes 60% (3 nga 5 transaksione):
  - Bashkësitë e shpeshta janë: {qumësht, bukë}, {bukë, vezë}, {bukë, birrë}

#### Hapi 2: Gjenerimi i Rregullave të Shoqërimit

- Nga bashkësitë e shpeshta, gjenerojmë rregullat:
  - \\( \text{qumësht} \rightarrow \text{bukë} \\)
  - \\( \text{bukë} \rightarrow \text{veze} \\)
  - \\( \text{bukë} \rightarrow \text{birrë} \\)

- Llogaritja e besueshmërisë:
  - \\( \text{Confidence}(\text{qumësht} \rightarrow \text{bukë}) = \frac{\text{Support}(\text{qumësht} \cup \text{bukë})}{\text{Support}(\text{qumësht})} \\)

---

Kjo është një përmbledhje e algoritmit Apriori që mund të përfshihet në README për projektin tuaj. Sigurohuni të zëvendësoni `username` dhe `repo-name` me emrin tuaj të përdoruesit dhe emrin e repository-t në GitHub.
