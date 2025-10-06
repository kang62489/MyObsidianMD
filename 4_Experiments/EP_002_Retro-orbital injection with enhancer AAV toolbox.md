# Tasks and Memos
The vectors I will use:
1. <mark style="background: #FF5582A6;">ChAT-enhancer-rACh1h-minWPRE</mark>
2. <mark style="background: #BBFABBA6;">ChAT-enhancer-GRAB_ACh 3.0-minWPRE</mark>
3. <mark style="background: #BBFABBA6;">ChAT-enhancer-iAChSnFR-minWPRE</mark>
4. <mark style="background: #BBFABBA6;">D2-enhancer-dLight 3.8-minWPRE</mark>
5. <mark style="background: #FF5582A6;">D2-enhancer-RdLight1-mineWPRE</mark>

ChAT-enhancer => For specifically select ChAT cells in striatum (striatal cholinergic interneurons)
D2-enhancer => For specifically select dopaminergic terminals in striatum
- D2 receptors are **autoreceptors** that regulates dopamine neuron activity and transmission [crossRef:: R_01 Figure 1 Short and long isoforms of the D2 receptor and the
identity of the autoreceptor, Ford, 2012_Neuroscience, @Line 9]
The combinations I will try
1. combination: <mark style="background: #FF5582A6;">1</mark> + <mark style="background: #BBFABBA6;">4</mark>
2. combination: <mark style="background: #BBFABBA6;">2</mark> + <mark style="background: #FF5582A6;">5</mark>
3. combination: <mark style="background: #BBFABBA6;">3</mark> + <mark style="background: #FF5582A6;">5</mark>

Preparation of 12 wild-type mice, aged 5-8 weeks. If the delivery is late, use my ChAT-cre mice first.
Each combination will be done on three mice.
The examination will apply the epifluorescence microscope system + CCD camera (PCO.panda) in Ephys room (D456 in D464) by Kang.


1. RO VS STEREO injections (use ChAT-cre mice): volume of each virus (100 ul x1 + 5ul x N)

| serotype | promotor/enhancer | cre-lox | tet-off | sensors/tools |           labeling           |   clone    | in stock? |
| :------: | :---------------: | :-----: | :-----: | :-----------: | :--------------------------: | :--------: | :-------: |
|  PHP.eb  |    ihSyn/hSyn     |    x    |    x    |  GRAB_ACh3.0  |              x               |   121922   |    no     |
|  PHP.eb  |    ihSyn/hSyn     |    x    |   yes   |   iAChSnFR    |              x               |    089     |    no     |
|  PHP.eb  |    ihSyn/hSyn     |   DIO   |    x    |   hM4D(Gi)    | mCherry (change to tdTomato) | 44362-AAV8 |    no     |
|  PHP.eb  |    ihSyn/hSyn     |    x    |   yes   |   RdLight1    |              x               |    137     |    no     |

2. Enhancer @ WT  VS Promotors @ ChAT-cre (only on stereotaxis): volume of each virus (5ul x N)

| serotype | promotor/enhancer | cre-lox | tet-off | sensors/tools |           labeling           |   clone    | in stock? |
| :------: | :---------------: | :-----: | :-----: | :-----------: | :--------------------------: | :--------: | --------- |
|   AAV1   |       ihSyn       |   DIO   |    x    |   hM4D(Gi)    | mCherry (change to tdTomato) | 44362-AAV8 | no        |
|   AAV1   |   ChAT-enhancer   |    x    |    x    |   hM4D(Gi)    |           mCherry            |    137     | no        |
