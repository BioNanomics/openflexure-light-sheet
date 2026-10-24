# OpenFlexure Light-Sheet Microscopy

**BioNanomics · Student project · Planning and recruitment**

Build a student team to reproduce, document, and evaluate an affordable light-sheet microscope based on [SPIM-DoMB](https://github.com/fluoimlab/SPIM-DoMB) and its modified [OpenFlexure Block Stage](https://github.com/fluoimlab/OpenFlexure-XYZR).

The goal is a reproducible instrument and an approachable learning project spanning 3D printing, optics, electronics, microscopy software, and quantitative imaging. This repository currently contains the project README; construction, software development, and experiments are future work.

**Related project:** [C. elegans NSPARC–diSPIM Benchmark](https://github.com/BioNanomics/celegans-nsparc-dispim-benchmark)

**Relationship ticket:** [Companion build: OpenFlexure-based student light-sheet microscope — benchmark #2](https://github.com/BioNanomics/celegans-nsparc-dispim-benchmark/issues/2)

## The idea in pictures

These are upstream reference images, not photographs or results from a BioNanomics build. Click an image to open its original source.

[![SPIM-DoMB overview showing the excitation path, sample handling, and detection path](https://raw.githubusercontent.com/fluoimlab/SPIM-DoMB/e4f41c6eafad02572f0afd2cba85b847c9b27828/img/overall_schematic.png)](https://github.com/fluoimlab/SPIM-DoMB/blob/e4f41c6eafad02572f0afd2cba85b847c9b27828/img/overall_schematic.png)

*SPIM-DoMB instrument overview. Source: fluoimlab / Department of Molecular Biophysics, Bogomoletz Institute of Physiology, Kyiv, Ukraine.*

<table>
  <tr>
    <th>OpenFlexure stage and joystick</th>
    <th>Light-sheet reference photo</th>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/fluoimlab/OpenFlexure-XYZR/blob/e7d1ba4b016e3b068eef118a99a042b03127c880/img/stand_alone_j.jpg"><img src="https://raw.githubusercontent.com/fluoimlab/OpenFlexure-XYZR/e7d1ba4b016e3b068eef118a99a042b03127c880/img/stand_alone_j.jpg" width="380" alt="Upstream assembled OpenFlexure Block Stage with joystick control"></a></td>
    <td align="center"><a href="https://github.com/fluoimlab/SPIM-DoMB/blob/e4f41c6eafad02572f0afd2cba85b847c9b27828/img/ls_side.jpg"><img src="https://raw.githubusercontent.com/fluoimlab/SPIM-DoMB/e4f41c6eafad02572f0afd2cba85b847c9b27828/img/ls_side.jpg" width="380" alt="Side view of the light sheet documented by SPIM-DoMB"></a></td>
  </tr>
  <tr>
    <td>Reference for printed mechanics, motor control, and student assembly.</td>
    <td>Reference for understanding illumination geometry and future optical validation.</td>
  </tr>
  <tr>
    <th>Sample-holder model</th>
    <th>Assembled sample stage</th>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/fluoimlab/OpenFlexure-XYZR/blob/e7d1ba4b016e3b068eef118a99a042b03127c880/img/00_of_sample_holder_v0_scad.png"><img src="https://raw.githubusercontent.com/fluoimlab/OpenFlexure-XYZR/e7d1ba4b016e3b068eef118a99a042b03127c880/img/00_of_sample_holder_v0_scad.png" width="380" alt="OpenSCAD thumbnail of the upstream syringe sample-holder model"></a></td>
    <td align="center"><a href="https://github.com/fluoimlab/OpenFlexure-XYZR/blob/e7d1ba4b016e3b068eef118a99a042b03127c880/img/of_bs_side.jpg"><img src="https://raw.githubusercontent.com/fluoimlab/OpenFlexure-XYZR/e7d1ba4b016e3b068eef118a99a042b03127c880/img/of_bs_side.jpg" width="380" alt="Side photograph of the upstream printed stage and sample holder"></a></td>
  </tr>
  <tr>
    <td>A concrete entry point for learning parametric CAD and sample mounting.</td>
    <td>The corresponding physical assembly, useful for connecting model to hardware.</td>
  </tr>
</table>

*Gallery credit: fluoimlab / Department of Molecular Biophysics. Images are embedded from the original repositories at fixed revisions; their source and licence links are recorded below.*

## What we are building toward

SPIM illuminates a thin plane in the specimen and images that plane from a different direction. Moving the specimen through the sheet produces a 3D image stack.

Our starting point is the existing SPIM-DoMB design, which combines openUC2-based optical modules with a modified OpenFlexure Block Stage for sample positioning. The OpenFlexure contribution here is the sample stage; this is a separate optical instrument from the standard OpenFlexure microscope.

The upstream projects remain in development. In particular, OpenFlexure-XYZR documents XYZ positioning while its rotary-axis arm is marked as in progress. Our first design review will establish which upstream revision and features to reproduce.

The intended outcome is a documented build, an understandable bill of materials, measured instrument performance, and a path for future student teams to reproduce the work. Budget and performance targets will be set after reviewing the optics, camera, filters, existing lab equipment, and sample requirements.

## Connection to the benchmark project

The [C. elegans NSPARC–diSPIM Benchmark](https://github.com/BioNanomics/celegans-nsparc-dispim-benchmark) asks whether an available NSPARC confocal system can support useful embryo imaging and lineage measurements relative to published diSPIM work. This companion project explores the instrument-building side: an accessible light-sheet platform that students can understand, reproduce, and characterize.

The projects can share measurement definitions, acquisition records, and evaluation methods where appropriate. The build would first be assessed with calibration samples and fixed specimens before considering suitable biological experiments. Suitability for live C. elegans imaging remains a question to evaluate.

SPIM-DoMB is not automatically a dual-view diSPIM instrument. No optical equivalence, live-imaging capability, or BioNanomics performance result is claimed at this stage. [Benchmark issue #2](https://github.com/BioNanomics/celegans-nsparc-dispim-benchmark/issues/2) tracks the connection between the two projects.

## Student opportunities

Students can contribute through a focused workstream and collaborate across disciplines. The first contribution can be a design review, documented question, or explanation of an upstream component.

| Workstream | Possible contributions |
| --- | --- |
| Mechanics and fabrication | Review printable parts, sample holders, assembly steps, and stage calibration. |
| Optics | Understand illumination and detection geometry, select compatible components, and plan measurements. |
| Electronics and motion | Review stage motors, control electronics, wiring documentation, and repeatability. |
| Acquisition software | Evaluate upstream Micro-Manager and Python integration; define acquisition and metadata needs. |
| Imaging and analysis | Plan bead-based characterization, image-quality measurements, and links to the benchmark methods. |
| Documentation and outreach | Improve the build narrative, photographs, diagrams, student onboarding, and reproducibility records. |

## Proposed milestones

These are planning milestones, not completed work.

1. **Review the reference design.** Choose an upstream revision; audit the bill of materials, licences, lab inventory, budget, and sample requirements.
2. **Assemble and measure the stage.** Document printing and assembly; measure travel, repeatability, and sample mounting.
3. **Review and integrate the optical system.** Establish the lab-approved enclosure, controls, and training before energized laser work; integrate illumination, detection, and the camera.
4. **Characterize with calibration samples.** Measure sheet thickness, point-spread function, field of view, motion, and acquisition cadence with documented methods.
5. **Evaluate fixed specimens.** Establish a reproducible mounting and imaging workflow; assess whether approved live-specimen studies are justified.
6. **Connect to the benchmark.** Report image quality, acquisition speed, and photobleaching under comparable conditions where possible, including failures and limitations.

## Reference projects and image credits

| Source | Role in this project | Reference revision and licence |
| --- | --- | --- |
| [SPIM-DoMB](https://github.com/fluoimlab/SPIM-DoMB) | Light-sheet instrument, optical modules, overview image, and light-sheet photograph. | [e4f41c6](https://github.com/fluoimlab/SPIM-DoMB/tree/e4f41c6eafad02572f0afd2cba85b847c9b27828) · [CERN-OHL-W-2.0](https://github.com/fluoimlab/SPIM-DoMB/blob/e4f41c6eafad02572f0afd2cba85b847c9b27828/LICENSE) |
| [OpenFlexure-XYZR](https://github.com/fluoimlab/OpenFlexure-XYZR) | Modified sample stage, stage photographs, and sample-holder model thumbnail. | [e7d1ba4](https://github.com/fluoimlab/OpenFlexure-XYZR/tree/e7d1ba4b016e3b068eef118a99a042b03127c880) · [CERN-OHL-W-2.0](https://github.com/fluoimlab/OpenFlexure-XYZR/blob/e7d1ba4b016e3b068eef118a99a042b03127c880/LICENSE) |
| [OpenFlexure Block Stage](https://gitlab.com/openflexure/openflexure-block-stage/) | Original flexure-stage design underlying the adaptation. | Upstream design and attribution. |
| [openUC2](https://github.com/openUC2/UC2-GIT) | Modular optical-system foundation acknowledged by SPIM-DoMB. | Upstream design and attribution. |

Credit for the reference hardware and gallery belongs to the upstream authors. The photographs illustrate their work and do not imply their involvement in or endorsement of this BioNanomics project. Future copied or modified hardware and software sources must retain their applicable upstream notices and licences.
