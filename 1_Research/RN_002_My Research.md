---
Established: 2024-12-08
Last Updated: 2025-03-09
Description: This note is used to re-organize my thoughts and questions to my research
---
# MEMO
- Research Topic
	- Spatial and Temporal Dimensions of Neurochemical Signaling by Striatal Cholinergic Interneurons
		- Motivation:
			- Neurochemical signaling is a critical process by which neurons used in central nervous system for intercellular communications. Except for the synaptic transmission (ST) which inspired in the pioneer studies of neuromuscular junctions, volume transmission (VT), a contrast type of ST were proposed to . The VT describes a diffusion-based, slow and spatially uniform neurochemical signaling. However, 
				- In this project, I'm interested if a specific type of neurons - cholinergic interneurons are able to control the release in time and space domain.
			- Traditional measuring approach either limited by temporal resolution or spatial resolution => now, novel genetically-encoded sensors
			- Through this project, I would like to study the problems:
				- Core: Is neuromodulation a spatiotemporally dynamic phenomenon shaped by firing patterns?
				- Do the firing patterns of a ChI encode its ACh signals’ spatial and temporal properties? ^7272e4
				- Sub-questions:
					- How does firing patterns of cholinergic interneurons encodes the spatial and temporal release patterns of ACh
					- The spatial characteristic of ACh release of single cholinergic interneurons
						- size, observability => should help us to understand if ACh is synaptic transmission or volume transmission
							- in current set up, we shall not able to see any thing change
							- if we can see, it must be volume transmission
					- The spatial dynamics of ACh distribution
						- does volume transmission confined in a large area? or propagate like waves?
		- Overarching aim:
			- Firing activities, or neuronal firing patterns, act as the clocking signals that are intricately linked to neurotransmitter release. This study aims to investigate the relationship between neuronal firing patterns and the temporal dynamics of acetylcholine (ACh) responses. Additionally, it seeks to explore the spatial characteristics of ACh in relation to these firing patterns.
		- 時間維度 (Temporal dimension):
			- What kinds of pattens generate releases (temporally observable)
			- What's the release pattern
		- 空間維度 (Spatial dimension):
			- Where does the release happen.
			- How large is the ACh release range.
			- Does the release spread (like a wave)?

- Hypothesis
	- Single action potential is enough to trigger single cholinergic interneurons to release.
	- The firing patterns of single cholinergic interneurons control the location and the range of the ACh releases
	- The releases of single cholinergic interneurons are confined in a certain place
- Targets
	- aim 1
		- Use different stimulation protocol of patch clamp to observe the releases by ACh sensors (iAChSnFR, GACh 3.0)
			- single pulse
			- continuous stimulation
			- certain frequency
		- To confirm the release come from targeted neurons, DREADD (inhibitory type) is also used
	- aim 2
		- analyze if spatial distribution (controlled by firing patterns)
	- aim 3
		- observe the spatial distribution of patched cholinergic interneurons at different magnification (10X, 60X)
		- check the spreading of the spatial release of ACh, if it is confined, try find if DA terminals are overlapped
		- if it is moving, try find if it is wave-like.

Experiments:
- Sensor comparison (iAChSnFR/GACh 3.0) X3
	- iAChSnFR: AAV1-ihSyn-tTA-sv40/TRE-iAChSnFR-minWPRE (Right, 2 sites, 300 nl/site)
	- GACh: AAV1-hSyn-GRAB_ACh3.0 (Left, 2 sites, 300 nl/site)
	- mCherry: AAV1-hSyn-DIO-mCherry
	- Animal:
- Sensor comparison (iAChSnFR/GACh 3.0) X2
	- - iAChSnFR: AAV1-ihSyn-tTA-sv40/TRE-iAChSnFR-minWPRE (Right, 2 sites, 300 nl/site)
	- GACh: AAV1-hSyn-GRAB_ACh3.0 (Left, 2 sites, 300 nl/site)
	- mCherry: AAV1-hSyn-DIO-mCherry
- For aim 1 X3
	- determined sensors (probably GACh 3.0)
	- DREADD: AAV8-hSyn-DIO-mCherry
- - For aim 1 X3
	- determined sensors (probably GACh 3.0)
	- DREADD: AAV8-hSyn-DIO-hM4D(Gi)-mCherry
	
### **1. Contradictory evidence about "uniform" modulation:**

- **Question**: "If ACh creates a uniform ambient tone, why do we see heterogeneous behavioral/physiological responses across the striatum?"
- **Observation**: Different striatal regions or cell populations showing varied responses to cholinergic manipulation despite the theoretical uniform distribution

### **2. Anatomical constraints on diffusion:**

- **Question**: "Can ACh from a single varicosity really create uniform distribution given the physical constraints of diffusion?"
- **Observation**: ChI axons have discrete varicosities with specific spatial arrangements - diffusion physics would predict concentration gradients, not uniform fields

### **3. Firing pattern diversity in ChIs:**

- **Question**: "Why do cholinergic interneurons show such diverse firing patterns (regular, irregular, bursting) if they just need to maintain a uniform ambient level?"
- **Observation**: ChIs exhibit behaviorally-relevant changes in firing patterns - this diversity suggests functional significance beyond just "maintaining background tone"

### **4. Temporal mismatch between behavior and ambient tone theory:**

- **Question**: "How can the slow ambient tone model explain rapid behavioral modulation by acetylcholine?"
- **Observation**: Behavioral responses to cholinergic manipulation can be quite rapid, inconsistent with slow ambient tone changes

### **5. Receptor distribution patterns:**

- **Question**: "Why are cholinergic receptors distributed heterogeneously if ACh distribution is uniform?"
- **Observation**: Non-uniform distribution of muscarinic and nicotinic receptors across striatal space suggests the system is designed for spatially specific signaling

### **6. Technical limitations of previous studies:**

- **Question**: "Are our current measurement techniques actually capable of detecting the spatial and temporal resolution of ACh signaling?"
- **Recognition**: Most studies measured ACh at relatively coarse spatial/temporal scales, potentially missing finer-grained heterogeneity

### **7. Single-cell stimulation experiments:**

- **Question**: "What actually happens when we stimulate a single cholinergic interneuron?"
- **Motivation**: Need to understand the elementary unit of cholinergic signaling before building theories about population effects

The core insight driving these hypotheses was likely: **"The uniform ambient tone model may be an oversimplification that emerges from technical limitations rather than biological reality."**

# Folder Structure (0 directories, 2 files)
RN_002
├── RN_002_info.md
├── RN_002_info_20241208.svg
└── RN_002_info_20250213.svg
