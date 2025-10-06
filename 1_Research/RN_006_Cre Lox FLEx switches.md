---
Established: 2025-03-09
Last Updated: 2025-03-09
Description: A summary about cre lox flex switch technique
---
# Terminology
Cre-Lox Recombination = utilize the principle that cre recombinase bind to the sequence between two LoxP sites.
Cre recombinase
- Stands for **Cre**ates recombination, an enzyme derive from P1 bacteriophage, and is designed to cut out genetic sequences between two LoxP sites.
- Only binds to the lox
LoxP
- A DNA sequence 
- **L**ocus **O**f **X**(cross)-Over **P**1 Bacteriophage
- LoxP is a site on P1 bacteriophage consisting of 34 bps. This includes two symmetric 13 bp sequences (ATAACTTCGTATA <-> TATACGAAGTTAT, the recognition sites) and an asymmetric 8 bp sequence (GCATACAT, spacer).
- Because the asymmetry of the 8 bp, LoxP sites are directional.
- Deletion, Inversion, Translocation can be done based on the orientation of these LoxP sites.
	- same direction => deletion
	- opposite direction => inversion (reversible, because LoxP sites remain the same. But not useful because it continuously flipping) => FLEx
	- interchromosomal recombination => translocation
FLEx
- Stands for **FL**ip **Ex**cision
- The Cre will only recombine two LoxP sites if they have the same spacer sequence.
- Scientists developed Lox sites with different asymmetric spacer so that the Lox sites are not cross compatible.
DIO
- **D**ouble-floxed with **I**nverted **O**rientation (note: flox = Flip Lox sites)
DO
- Double-floxed with in Orientation

Tet-On System:
- The gene is activated (turned **on**) in the presence of **tetracycline** or its derivative (like doxycycline).
- This happens because a modified protein called **rtTA (reverse tetracycline-controlled transactivator)** binds to a specific DNA sequence (TRE - tetracycline-responsive element) **only when tetracycline is present**.
- **Example**: You add doxycycline to a cell culture, and the gene of interest (like GFP) starts being expressed (produced).

Tet-Off System:
- The gene is activated (turned **on**) in the absence of **tetracycline** or its derivative.
- A protein called **tTA (tetracycline-controlled transactivator)** binds to the TRE **only when tetracycline is NOT present**. If tetracycline is added, it prevents binding, thus turning the gene off.
- **Example**: You remove doxycycline from a cell culture, and the gene of interest becomes active and starts being expressed.    

Key Difference:
- In **Tet-On**, the presence of tetracycline activates gene expression.
- In **Tet-Off**, the absence of tetracycline activates gene expression.
# Prerequisite Knowledge
## Amino acids
Amino acids are organic compounds that contain both **amino** and **carboxylic acid** functional groups. ^3cbedd

Amino functional group: $－NH_2、－NHR、－NR_2、NH_3^+$
Carboxylic group: $COO^-$

R means side chain
structure of amino acids #addFigure
## 蛋白質
1. 組成: C,H,O,N,S
2. 基本構造單位: 胺基酸 Amino acid
	1. 胺基酸組成: 銨基 $NH_2$ , R 基, 羧基 $COOH^-$
	2. 不同胺基酸 R基不同, 共有20種胺基酸
	3. 不同種類、數目、順序構成不同蛋白質
	4. 銨基的H可以接羧基OH的O

酵素 (enzyme) 也是蛋白質
## 五碳醣 (單醣的一種、構成核苷酸的要素之一)
- 核醣 (Ribose)
- 去氧核醣 (Deoxyribose)

## 核酸 (Nucleic acids)
1. 組成: C,H,O, N, P (organic)
2. 基本構造單位: 核苷酸 (nucleotide)
	1. Nucleotide: 磷酸根($PO^{4+}$) + 五碳醣(ribose or deoxyribose) + 含氮鹼基 nitrogenous base
	2. Nitrogenous base in RNA (Ribonucleic acid)
		1. A, Adenine (腺嘌呤)
		2. G, Guanine (鳥糞嘌呤)
		3. C, Cytosine (胞嘧啶)
		4. U, Uracil(脲嘧啶)
	3. Nitrogenous base in DNA (AT, CG) (Deoxyribonucleic acid)
		1. A
		2. G
		3. C
		4. T, Thymine (胸腺嘧啶)

碳環編號，以核醣的氧原子作為0，右邊第一個碳為1' (one-prime)，順時針依序編號。
3'接OH基，5'接CH2OH
去氧核醣是2'的OH被去掉一個氧原子變成H

## ATP
ATP (Adenosine triphosphate) 內的醣是核糖 A是腺嘌呤 是核苷酸(nucleotide)的一種
ATP 產生能量方式: 水解打斷其中一個磷酸根鍵結並釋放出能量 產物為ADP跟水

基因是DNA片段

中心法則(Central Dogma): DNA -> Transcription (by RNA polymerase) -> RNA -> Translation (by Ribosome) -> Protein

細菌(原核生物)沒有細胞核膜包圍的細胞核只有核區，核區內沒有組織蛋白只有DNA構成的染色體，雖然也是雙股但卻是環狀的。細菌仍然遵守分子生物學的中心法則來合成蛋白質。合成蛋白質的地方叫做質體(Plasmid, 真核生物是在核糖體)，是獨立於核區染色體外的一段環狀的DNA，上面也有基因(有意義的DNA片段)，所以可以透過抗藥性來knock out。

重組DNA (Recombinase)
剪刀: DNA 限制酶 (Restriction endonucleases), 找在核區與質體的特定核苷酸序列剪下，ex: AATT
膠水: DNA 連接酶 (DNA ligase)

剪刀打開質體環 剪下來的基因透過DNA連接酶連到開環的質體DNA並再次形成閉環，將重組過的質體DNA植入E-coli便可以產生需要的蛋白質

## Promoter
A promoter is a region of DNA that controls the expression of a gene. It is located near the start of the gene (toward the 5' end) and contains specific sequences of DNA that are recognized by proteins called transcription factors. These transcription factors bind to the promoter and help to initiate the process of transcription, which is the first step in the synthesis of a protein from a gene.

讓RNA聚合酶辨認要轉錄的一段DNA序列，不是基因

基因是一段有意義的DNA片段，也就是能夠合成特定蛋白質的基因序列

add content: about ChAT, hSyn as promoter means they use the promoter part of theses genes
ihSyn: improved human synapsin
選擇promotor來決定sensor expression的專一性還是不如cre-lox系統，因為不同neuron或cell可能都帶有同一promotor的基因序列，像這裡提到的human synapsin便是所有neuron都有帶的一段序列。

## Serotype
A serotype is a subtype of a microorganism (such as a bacterium or virus) that is defined based on the specific proteins present on its surface. These proteins are called antigens, and they are used by the immune system to identify and attack the microorganism.

add more about AAVs and serotype, tropisms
## Expression
add definition

# Survey
Two ways to introduce Cre recombinase
1. Use virus to introduce Cre recombinase into the cell
2. Generate transgenic mice that insert gen for cre recombinase after a specific promotor. Because this promotor can be expressed in certain cell types, the expression of cre recombinase can also be limited to these cells.

The technique is basically uses the property of Cre recombination to turn on or turn of a gene of interest for research. 

Tet-off (tTA-TRE) induces over expression
- If tTA gene is placed under the control of a strong promotor, it can lead to high levels of tTA protein production, which might results over expression.

[Source:: Youtube, Conditional gene expression using the Cre Lox FLEx vector switch!](https://www.youtube.com/watch?v=I21NmFq4F8A)
[Source:: Youtube, Cre-LoxP Recombination](https://www.youtube.com/watch?v=oLPjiwM0G7A))