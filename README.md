# SOA-ComparisonProject
## SOA Model Comparison Script
This MATLAB script implements and compares three different semiconductor-optical-amplifier (SOA) models in a single run:
- **Michael Connelly Model**  
- **Yaser Khorrami Model**  
- **Hussein Taleb Quantum-Dot (QD) Model**

### Purpose  
Quickly benchmark output power predictions from three distinct SOA modeling approaches under the same input conditions.
### Key Features  
1. **Common Input Setup**  
   - Defines a single input power (–20 dBm → 10⁻⁵ W) for the Khorrami and Taleb models.  
2. **Connelly Model**  
   - Uses carrier-rate equations with parameters: electron charge, Planck’s constant, confinement factor, small-signal gain coefficient, carrier lifetime, effective area, and active length.  
   - Computes steady-state carrier density and clamps the gain exponent for realistic limits.  
3. **Khorrami Model**  
   - Simple saturation gain: \(G = G_0 / [1 + P_\text{in}/P_\text{sat}]\) with \(G_0=25\) dB and \(P_\text{sat}=5\) mW.  
4. **Taleb QD Model**  
   - Three‐level carrier population dynamics (wetting layer → excited state → ground state) solved over a 1 ns time grid.  
   - Applies a hyperbolic‐tangent scaling of the ground-state population to derive a saturated gain up to 30 dB.  
5. **Output & Visualization**  
   - Bar chart of final output powers (mW) for all three models.  
   - Command-window summary prints each model’s predicted output.

## MATLAB Live Scripts for Standard SOA and QD-SOA Analysis

These two MATLAB Live Scripts model and compare the performance of a Standard SOA versus a quantum-dot SOA (QD-SOA), and explore parameter-driven gain enhancement in QD-SOAs.

### 1. QDComparison.mlx  
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
  - Generates an overlaid gain vs. input power plot, with legend entries for each configuration.  
- **Typical Use**: Map the design trade-space for maximizing QD-SOA gain and saturation performance.
