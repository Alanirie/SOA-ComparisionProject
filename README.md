# SOA-ComparisionProject
## SOA_CompareAllModels.mlx
This file provides a comparsion of the Connelly, Khorrami, and Taleb SOA models. It acts as an overview and introduction to the key concepts in this project.

## MATLAB Live Scripts for Standard SOA and QD-SOA Analysis

These two MATLAB Live Scripts model and compare the performance of a Standard SOA versus a quantum-dot SOA (QD-SOA), and explore parameter-driven gain enhancement in QD-SOAs.

### 1. QDComparision.mlx  
- **Purpose**: Benchmarks a conventional bulk SOA against a QD-based SOA.  
- **Key Features**:  
  - Defines an input power sweep (–20 dBm to +20 dBm).  
  - Implements a saturation-based gain model.  
  - Plots:  
    1. Gain vs. input power  
    2. Saturation output power comparison  
    3. Noise figure comparison  
    4. Gain bandwidth comparison  
- **Typical Use**: Quickly visualize the advantages of QD active regions in gain, saturation, noise figure, and bandwidth.

### 2. QDMaxing.mlx  
- **Purpose**: Parametrically studies how QD-SOA performance scales with device design choices.  
- **Key Features**:  
  - Baseline small-signal gain, saturation power, and confinement factor.  
  - Loops over combinations of:  
    - Number of quantum-dot layers (1, 3, 5, 7)  
    - Confinement factors (0.4, 0.5, 0.6)  
    - Tunnel-injection boost factors (1.0, 1.1, 1.2)  
  - Generates an overlaid gain-vs-input-power plot, with legend entries for each configuration.  
- **Typical Use**: Map the design trade-space for maximizing QD-SOA gain and saturation performance.
