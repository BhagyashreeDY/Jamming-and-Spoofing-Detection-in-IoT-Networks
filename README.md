# Jamming and Spoofing Detection in IoT Networks – Dataset

## Overview
This repository provides the dataset used in the research study entitled:

**“Jamming and Spoofing Detection in IoT Networks”**

The dataset supports the development and evaluation of machine learning models for detecting malicious interference in IoT communication systems. It captures representative traffic behavior corresponding to normal network operation as well as two prominent attack types—jamming and spoofing.

The dataset is shared to facilitate experimental reproducibility and to enable further research in the area of IoT security.

---

## Dataset Size and Composition
The dataset consists of a total of **15,000 network traffic instances**, evenly distributed across three classes:

- **Normal traffic**: 5,000 samples  
- **Spoofing attacks**: 5,000 samples  
- **Jamming attacks**: 5,000 samples  

Each instance represents a summarized network flow characterized by statistical, signal-level, and protocol-related features.  
The balanced class distribution ensures unbiased training and evaluation of machine learning classifiers.

---

## Feature Description
Each record in the dataset contains **18 attributes**, including one target label.  
The features are designed to reflect practical indicators commonly used in IoT network monitoring and wireless security analysis.

### Traffic and Flow Characteristics
- `flow_duration` – Duration of the communication flow  
- `packet_count` – Number of packets transmitted  
- `traffic_volume` – Total transmitted data volume  
- `packet_interarrival` – Average inter-arrival time between packets  

### Reliability and Error Metrics
- `packet_loss` – Packet loss ratio  
- `bit_error_rate` – Bit-level transmission errors  
- `pfr` – Packet failure rate indicator  
- `burst_loss_rate` – Indicator of burst packet loss  

### Signal and Physical-Layer Indicators
- `snr` – Average signal-to-noise ratio  
- `snr_std` – Variability of SNR  
- `signal_strength` – Received signal strength indicator (RSSI)  
- `location_jump` – Sudden spatial or positional change metric  

### Network and Protocol Attributes
- `port_number` – Destination port  
- `ttl` – Time-to-live value  
- `src_addr_valid` – Source address validity flag  
- `dst_addr_valid` – Destination address validity flag  
- `protocol` – Communication protocol (TCP, UDP, HTTP, DNS)

### Target Label
- `label` – Type of network behavior

---

## Class Labels
The target variable represents the following traffic categories:

- **Normal** – Legitimate IoT communication without interference  
- **Jamming** – Deliberate radio interference causing degradation of service  
- **Spoofing** – Identity or address manipulation to mislead the network  

For machine learning experiments, labels may be encoded numerically during preprocessing.

---

## Data Generation and Design Considerations
The dataset was generated using a **controlled simulation framework** that models realistic IoT communication patterns under varying network conditions.

Key design principles include:
- Use of statistically grounded distributions to reflect real-world variability  
- Distinct behavioral profiles for normal, spoofing, and jamming scenarios  
- Inclusion of cross-layer indicators (traffic, signal, and protocol features)  
- Reproducible generation process to ensure consistent experimental results  

Such simulation-based datasets are commonly adopted in IoT security research where large-scale, labeled attack data is difficult to obtain in real deployments.

---

## Preprocessing Notes
In typical experimental pipelines, the following preprocessing steps are applied:
- Handling of missing values using statistical imputation (if applicable)
- Encoding of categorical labels
- Feature normalization using Z-score standardization to ensure uniform scaling

---

## Intended Use
This dataset is intended for **academic and research purposes**, including:
- Machine learning–based intrusion and attack detection
- Evaluation of classification and ensemble learning models
- Comparative analysis of IoT security mechanisms

---

## Availability and Citation
This dataset is associated with a research paper that is currently under conference review.

If you use this dataset in your work, please cite it as:

*Dataset associated with the study “Jamming and Spoofing Detection in IoT Networks.”*

Updated citation details will be provided upon publication of the paper.

---

## License
This dataset is released for research and educational use only.  
Any other use requires permission from the authors.
