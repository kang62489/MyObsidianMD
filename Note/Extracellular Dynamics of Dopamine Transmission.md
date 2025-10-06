1
==========================================================================
Changes in the Kinetics of Dopamine Release and Uptake Have Differential Effects on the Spatial Distribution of Extracellular Dopamine Concentration in Rat Striatum

探討在大鼠紋狀體中，DA的有限擴散距離是否能造成細胞外空間濃度分布在微米尺度範圍的異質性。

Spatial heterogeneity
由於空間上的條件差異所產生的不同特質

他們認為從空間濃度分布的差異可以反映受器上超微結構位置

用votammetry 量dopamine release
先用電刺激(黑質紋狀體迴路)產生DA release
再用藥物(nomifensine, L-Dopa, α-methyl-p-tyrosine)改變ECS中DA的kinetics (DA的後續的release和uptake)，主要看刺激後濃度的振幅改變

實驗結果會跟數學模擬算出的東西比較
數學模型是基於release和uptake的擴散方程式

他們的結果是說
Dopamine在微米範圍內具有空間異質性，也就是說濃度的空間分布是不均勻的

memo
還不清楚能否對描述我的問題有幫助，關聯是有的。在微米擴散範圍間的空間異質性是重點。Voltammetry電極附近的DA主要也是靠擴散的方式接近，空間分布上的差異以及對應的數學模型也許是我可以用作為解釋數學模型的參考內容

2
==========================================================================
Restricted Diffusion of Dopamine in the Rat Dorsal Striatum
還是先從rotation那時候比較相關的paper開始查起。
DA的空間擴散的確是了解我的科學問題中，Voltammetry的overshoot和hang-up的一個關鍵點，也許要找找看paper是專門探討有關DA diffusion跟voltammetry電極的

Q: 這篇是否有討論到overshoot 或 hang-up與EC DA diffusion的關聯?
A：似乎沒有，是另外一篇如下

3
==========================================================================
A Novel Restricted Diffusion Model of Evoked Dopamine
電刺激誘發DA release無法符合基於diffusion gap (假設電極與附近DA terminal間存在一層擴散區) 所建立的數值模型

最初的數學模型預測是限定DA只能濃度上升只限於刺激階段，當刺激結束後，濃度就馬上隨之下降，但這跟實際實驗的結果有出入。由於最早的模型是考慮電極周圍擴散間隔(diffusion gap)造成的影響，lag, overshoot跟hang-up只被認為是量測位置產生的誤差。

Q: 量測位置與現象之間關聯的推測說法是什麼?
參考本篇所提之文獻 [[memo_ Kawago_1992]]中，他們宣稱如果用DA擴散到電極所需的時間來解釋延遲(本文提到的lag)，在某些特定量測位置EC diffusion的影響小於Dopamine的濃度變化，可以觀測到觀測到DA濃度對刺激的即時反應。這樣的一個想法影響了後續研究中的量測，人們認為有一個假定的DA最佳量測熱點是受到最小的擴散效應影響

本文反駁的理由有
1. 在lag與overshoot的假設上太過特定導致常常與實驗觀察不一致
2. 如果電極與量測區域間真的存在一個實體擴散間，那lag與overshoot應該在每次量測都會同時出現且個別每次持續時間長度也會相似
3. 此外，這層擴散間隔所造成的影響應該要與電刺激條件、給藥條件無關
4. 此一理論並無解釋產生hang-up現象的原因
5. 上述所提的三種主要現象lag, overshoot and hang-up的出現，變化率在實際實驗觀察中經常性的可以觀察到不同時出現及受到電刺激、藥物影響

因此，diffusion gap的假設存在漏洞，而本文的主要解決方法是想透過修正數學模型的方式來解釋。在此提出的概念為restricted diffusion

我研究的點是，在顯微鏡+dLight sensor觀察evoked DA release的實驗中，並沒有出現overshoot的現象或是delay的現象，如果可以做出類似的光纖探針並coat sensor, 是否可以再現voltammetry因擴散所產生之特殊結果。藉由此一研究，我們想確定由genetic encoded sensor + fiber photometry所量測出的訊號是否能夠充分代表ECS中DA的dynamics，同時也希望能夠了解擴散對量測產生的影響

Q: 什麼是restricted diffusion model?
- 需要先了解 Q: What are DA domains (fast, slow)? 因為本文提到restricted model是用來維持(定義)DA fast and slow domains
	- 參考文章 Domain-dependent effects of DAT inhibition in the rat dorsal striatum, 內容提到的domains似乎與是藥物的範圍效果有關係(key: domain-dependent actions of nomifensine)。在其中所提的參考文獻(Tonic autoinhibition contributes to the heterogeneity of evoked dopamine release in the rat striatum)說明了在DAergic terminal附近存在多種不同時序速度的動態，此文章基於刺激期間濃度上升速度變化將其分成快速型與慢速型，快速型為刺激期間release量一開始先快速上升然後下降，慢速型則為隨著刺激時間持續上升，特別的是這兩類動態都未出現overshoot的現象，也就是當刺激停止時，濃度會立即下降。此文獻以這點作為量測並未受到擴散效應影響的說明。
	- 除此之外，對於快速型與慢速型在連續電刺激下也會具有相反的跨區間消長。快速型的反應會隨著刺激的次數增加而降低峰值濃度，已有報告指出應該與EC DA的濃度過高而產生的自我抑制有關係。
- 所謂的fast and slow domains 指的是axon terminal在ES evoked 的DA release 跟 uptake有著這兩種主要特徵。在 Domain-dependent effects of DAT inhibition in the rat dorsal striatum這篇文章中, Taylor 等人進一步探討了藥物在這兩種主要的時域變化裡面會產生什麼樣的效果
