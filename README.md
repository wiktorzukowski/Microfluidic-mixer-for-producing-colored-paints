# Microfluidic-mixer-for-producing-colored-paints

This project was developed as part of my Engineering Thesis at **Wrocław University of Science and Technology**. The goal was to design and implement a microfluidic system capable of precise mixing of primary color pigments to achieve specific paint shades at the microscale.

## 1. Project Overview
The objective of this thesis was to develop a **passive microfluidic mixer** capable of precise color formulation by mixing primary pigments. The project bridges the gap between theoretical microfluidics and practical industrial applications in the coating and paint industry.

**Motivation**
* Acrylic paints are produced by mixing a base (white, transparent) with colorants (pigment).
* In industry, production occurs in large volumes (min. 100 mL).
* **Problem:** Difficulties in producing small-volume, precise samples.
* **Solution:** Applying microfluidic technology for integration, miniaturization, and automation.

**Project Goals**
* Designing a microfluidic chip tailored for mixing high-viscosity paint components.
* Fabricating the chip using high-resolution **3D DLP printing technology**.
* Utilizing commercial components provided by **Jeger.pl**.
* Analyzing mixing efficiency and color consistency at the microscale.

**Challenges**
* High fluid viscosity and a lack of existing literature dedicated to paint micro-mixing.
* Necessity for real-time colorimetric analysis.

## 2. Inspiration and Theoretical Background
The base and colorants used in this project exhibit high viscosity, presenting a significant challenge for standard microfluidic applications. For this study, two micro-mixer designs were selected based on established literature, though they were adapted here specifically for the requirements of paint production.

![1st geometry](https://github.com/user-attachments/assets/dc82f98c-e8db-4afd-8e49-99b929fe599d)

**Description:** Schematic representation of various channel geometries used to enhance mixing. These designs aim to trigger chaotic advection to overcome laminar flow dominance.
*Source: Yulong Yang et al., "Micro- and nanofluidic mixers," Micromachines, 2016.*

![Microfluidic mixer geometry](https://github.com/user-attachments/assets/d3581e00-1eff-45d3-ad82-fc26971a11c8)

**Description:** Structural design of a mixer generating "turbulent-like" fluid motion, engineered for wide viscosity ratio applications.
*Source: Jonghun Lee et al., "A microfluidic mixer with self-excited ‘turbulent’ fluid motion," Lab on a Chip, 2010.*

## 3. Design and Fabrication
The project involved the manufacturing of **14 distinct prototypes**, categorized into two primary architectures: **Version 1 (Segmented Mixing Units)** and **Version 2 (Circular/Loop Structures)**. Channel dimensions ranged from **0.8 mm to 1.7 mm**.

<img width="1168" alt="3dmodels" src="https://github.com/user-attachments/assets/00efd5da-3e74-47b3-b807-ddad6883449b" />
**Description:** 3D CAD models of the designed micro-mixers featuring integrated observation chambers and microfluidic connectors.

### Fabrication and Post-processing
The micromixers were fabricated using **Digital Light Processing (DLP)** technology. A **transparent, biocompatible resin** (standardized for the dental industry) was selected to ensure optical clarity for flow analysis. 

Following the printing process, the chips underwent:
1. **Solvent Cleaning:** Ultrasonic bath in IPA to clear microchannels.
2. **Purging:** Compressed air to ensure geometry integrity.
3. **UV Post-curing:** Full polymerization to enhance mechanical properties.
4. **Surface Finishing:** Polishing of observation windows for camera monitoring.

## 4. Experimental Setup
The procedures were conducted using a specialized **measuring station developed by Wojciech Kubicki, PhD, Eng.**

**Station Components:**
* Electropneumatic pressure regulators for precise flow control.
* High-resolution camera and LED illumination for real-time monitoring.
* Liquid tanks for Base and Colorant.
* **DAQ Card** integrated with **LabVIEW** for automated data acquisition.

<img width="1190" alt="irlchips" src="https://github.com/user-attachments/assets/1561532c-b942-4e6f-b348-c9d1834adcab" />
**Description:** Fabricated micro-mixers ready for the experimental phase.

## 5. Paint Production and Measurement
To test the limits of the micro-geometries, materials with significant viscosity and density gradients were used:

| Material Component | Density ($\rho$) | Dynamic Viscosity ($\mu$) |
| :--- | :--- | :--- |
| **Base A** | 1.30 g/cm³ | 8,000 cP |
| **Colorant VT** | 2.01 g/cm³ | 500 – 1,500 cP |

**Process Optimization:** Base A was diluted with water in an **80:20 volumetric ratio (V/V)** to improve fluid flow characteristics.

### Color Measurement Method
1. **Visual Validation:** Real-time monitoring of the fluidic interface stability in the chamber.
2. **Quantitative Analysis:** Collecting droplets from the outlet onto a neutral white substrate.
3. **Digital Processing:** Scanning and decomposing data into **RGB components**.

## 6. Experimental Results

Measurement results were compiled for both designs while maintaining a **constant base pressure of 120 mbar** and varying the colorant pressure (90–140 mbar).

<table border="0" style="width: 100%; border-collapse: collapse;">
  <tr>
    <td align="center" style="width: 50%; padding: 10px; vertical-align: top; border: none;">
      <img width="454" alt="version1table" src="https://github.com/user-attachments/assets/9accc5d7-6415-4a22-9558-ee6e1aab28ef" />
      <br><br>
      <strong>Fig 1.</strong> Sample visualization for <strong>Version 1</strong>.
    </td>
    <td align="center" style="width: 50%; padding: 10px; vertical-align: top; border: none;">
      <img width="512" alt="2versionrgb" src="https://github.com/user-attachments/assets/79a02596-916a-4cbb-b2d1-7d132032b5af" />
      <br><br>
      <strong>Fig 2.</strong> Sample visualization for <strong>Version 2</strong>.
    </td>
  </tr>
</table>

### Data Normalization
Raw RGB data was transformed into a **normalized color value** ($\text{RGB}_{\text{norm}}$) on a scale of **0 to 1**. 

For **Version 1**, a clear **linear correlation** was observed in the 90–110 mbar range, indicating a predictable response where pigment concentration increases proportionally with inlet pressure.

<table border="0" style="width: 100%; border-collapse: collapse;">
  <tr>
    <td align="center" style="width: 50%; padding: 5px; border: none;">
      <img width="100%" alt="tab1" src="https://github.com/user-attachments/assets/b60a407a-c542-4ce1-906f-2be92c7744be" />
      <br><strong>Plot 1:</strong> Results for Version 1.
    </td>
    <td align="center" style="width: 50%; padding: 5px; border: none;">
      <img width="100%" alt="tab2" src="https://github.com/user-attachments/assets/ef99cf4c-019e-4aa4-9736-5ee25bee31e0" />
      <br><strong>Plot 2:</strong> Results for Version 2.
    </td>
  </tr>
</table>

## 7. Summary and Conclusions
* **Success Criteria:** Both micro-mixer architectures successfully produced homogeneous colored paints across various proportions.
* **Industrial Compatibility:** Commercial-grade components were successfully applied, confirming the viability of the designed geometries for industrial-scale materials.
* **Novelty:** No existing literature specifically addresses micro-mixing for these high-viscosity architectural coatings. This study establishes a foundational reference for miniaturized paint production.
* **Future Work:** Expanding the testing matrix to include a wider range of pigments and automating the pressure-color feedback loop.
