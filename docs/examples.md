# Real-World Scientific Examples

This document provides comprehensive, practical examples demonstrating how to combine Claude Scientific Skills to solve real scientific problems across multiple domains.

---

## Table of Contents

1. [Drug Repurposing & Network Pharmacology](#drug-repurposing--network-pharmacology)
2. [Clinical Trial Analysis](#clinical-trial-analysis)
3. [Materials Science & Chemistry](#materials-science--chemistry)
4. [Experimental Physics & Data Analysis](#experimental-physics--data-analysis)
5. [Chemical Engineering & Process Optimization](#chemical-engineering--process-optimization)
6. [Scientific Illustration & Visual Communication](#scientific-illustration--visual-communication)
7. [Quantum Computing for Chemistry](#quantum-computing-for-chemistry)
8. [Research Grant Writing](#research-grant-writing)

---

## Drug Repurposing & Network Pharmacology

### Example 1: Drug Repurposing for Rare Diseases

**Objective**: Identify FDA-approved drugs that could be repurposed for treating a rare metabolic disorder.

**Skills Used**:
- `database-lookup` - Query DrugBank, Open Targets, STRING, KEGG, Reactome, ClinicalTrials.gov, FDA, and biological databases
- `paper-lookup` - Search OpenAlex, bioRxiv, PubMed
- `networkx` - Network analysis
- `literature-review` - Systematic review

**Workflow**:

```bash
Step 1: Define disease pathway
- Query KEGG and Reactome for disease-associated pathways
- Identify key proteins and enzymes involved
- Map upstream and downstream pathway components

Step 2: Find protein-protein interactions
- Query STRING database for interaction partners
- Build protein interaction network around key disease proteins
- Identify hub proteins and bottlenecks using NetworkX
- Calculate centrality metrics (betweenness, closeness)

Step 3: Query Open Targets for druggable targets
- Search for targets associated with disease phenotype
- Filter by clinical precedence and tractability
- Prioritize targets with existing approved drugs

Step 4: Search DrugBank for drugs targeting identified proteins
- Query for approved drugs and their targets
- Filter by mechanism of action relevant to disease
- Retrieve drug properties and safety information

Step 5: Query FDA databases for safety profiles
- Check FDA adverse event database (FAERS)
- Review drug labels and black box warnings
- Assess risk-benefit for rare disease population

Step 6: Search ClinicalTrials.gov for prior repurposing attempts
- Query for disease name + drug names
- Check for failed trials (and reasons for failure)
- Identify ongoing trials that may compete

Step 7: Perform pathway enrichment analysis
- Map drug targets to disease pathways
- Calculate enrichment scores with Reactome
- Identify drugs affecting multiple pathway nodes

Step 8: Conduct systematic literature review
- Search PubMed for drug name + disease associations
- Include bioRxiv for recent unpublished findings
- Document any case reports or off-label use
- Use literature-review skill to generate comprehensive review

Step 9: Prioritize candidates
- Rank by: pathway relevance, safety profile, existing evidence
- Consider factors: oral availability, blood-brain barrier penetration
- Assess commercial viability and patent status

Step 10: Generate repurposing report
- Create network visualization of drug-target-pathway relationships
- Generate comparison table of top 5 candidates
- Write detailed rationale for each candidate
- Include mechanism of action diagrams
- Provide recommendations for preclinical validation
- Format as professional PDF with citations

Expected Output:
- Ranked list of 5-10 repurposing candidates
- Network analysis of drug-target-disease relationships
- Safety and efficacy evidence summary
- Repurposing strategy report with next steps
```

---

## Clinical Trial Analysis

### Example 2: Competitive Landscape Analysis for New Indication

**Objective**: Analyze the clinical trial landscape for a specific indication to inform development strategy.

**Skills Used**:
- `database-lookup` - Query ClinicalTrials.gov, FDA, DrugBank, Open Targets
- `paper-lookup` - Search PubMed, OpenAlex for published results
- `polars` - Data manipulation
- `matplotlib` - Visualization
- `seaborn` - Statistical plots
- `plotly` - Interactive plots
- `market-research-reports` - Competitive intelligence
- `pdf` - Report generation

**Workflow**:

```bash
Step 1: Search ClinicalTrials.gov for all trials in indication
- Query: "[disease/indication]"
- Filter: All phases, all statuses
- Extract fields:
  * NCT ID, title, phase, status
  * Start date, completion date, enrollment
  * Intervention/drug names
  * Primary/secondary outcomes
  * Sponsor and collaborators
- Export to structured JSON/CSV

Step 2: Categorize trials by mechanism of action
- Extract drug names and intervention types
- Query DrugBank for mechanism of action
- Query Open Targets for target information
- Classify into categories:
  * Small molecules vs biologics
  * Target class (kinase inhibitor, antibody, etc.)
  * Novel vs repurposing

Step 3: Analyze trial phase progression
- Calculate success rates by phase (I -> II, II -> III)
- Identify terminated trials and reasons for termination
- Track time from phase I start to NDA submission
- Calculate median development timelines

Step 4: Search FDA database for recent approvals
- Query FDA drug approvals in the indication (last 10 years)
- Extract approval dates, indications, priority review status
- Note any accelerated approvals or breakthroughs
- Review FDA drug labels for safety information

Step 5: Extract outcome measures
- Compile all primary endpoints used
- Identify most common endpoints:
  * Survival (OS, PFS, DFS)
  * Response rates (ORR, CR, PR)
  * Biomarker endpoints
  * Patient-reported outcomes
- Note emerging or novel endpoints

Step 6: Analyze competitive dynamics
- Identify leading companies and their pipelines
- Map trials by phase for each major competitor
- Note partnership and licensing deals
- Assess crowded vs underserved patient segments

Step 7: Search PubMed for published trial results
- Query: "[NCT ID]" for each completed trial
- Extract published outcomes and conclusions
- Identify trends in efficacy and safety
- Note any unmet needs highlighted in discussions

Step 8: Analyze target validation evidence
- Query Open Targets for target-disease associations
- Extract genetic evidence scores
- Review tractability assessments
- Compare targets being pursued across trials

Step 9: Identify unmet needs and opportunities
- Analyze trial failures for common patterns
- Identify patient populations excluded from trials
- Note resistance mechanisms or limitations mentioned
- Assess gaps in current therapeutic approaches

Step 10: Perform temporal trend analysis
- Plot trial starts over time (by phase, mechanism)
- Identify increasing or decreasing interest in targets
- Correlate with publication trends and scientific advances
- Predict future trends in the space

Step 11: Create comprehensive visualizations
- Timeline of all trials (Gantt chart style)
- Phase distribution pie chart
- Mechanism of action breakdown
- Geographic distribution of trials
- Enrollment trends over time
- Success rate funnels (Phase I -> II -> III -> Approval)
- Sponsor/company market share

Step 12: Generate competitive intelligence report
- Executive summary of competitive landscape
- Total number of active programs by phase
- Key players and their development stage
- Standard of care and approved therapies
- Emerging approaches and novel targets
- Identified opportunities and white space
- Risk analysis (crowded targets, high failure rates)
- Strategic recommendations:
  * Patient population to target
  * Differentiation strategies
  * Partnership opportunities
  * Regulatory pathway considerations
- Export as professional PDF with citations and data tables

Expected Output:
- Comprehensive trial database for indication
- Success rate and timeline statistics
- Competitive landscape mapping
- Unmet need analysis
- Strategic recommendations
- Publication-ready report with visualizations
```

---

## Materials Science & Chemistry

### Example 3: High-Throughput Materials Discovery for Battery Applications

**Objective**: Discover novel solid electrolyte materials for lithium-ion batteries using computational screening.

**Skills Used**:
- `pymatgen` - Materials analysis and feature engineering
- `scikit-learn` - Machine learning
- `pymoo` - Multi-objective optimization
- `sympy` - Symbolic math
- `vaex` - Large dataset handling
- `dask` - Parallel computing
- `matplotlib` - Visualization
- `plotly` - Interactive visualization
- `scientific-writing` - Report generation
- `scientific-visualization` - Publication figures

**Workflow**:

```bash
Step 1: Generate candidate materials library
- Use Pymatgen to enumerate compositions:
  * Li-containing compounds (Li1-xM1+xX2)
  * M = transition metals (Zr, Ti, Ta, Nb)
  * X = O, S, Se
- Generate ~10,000 candidate compositions
- Apply charge neutrality constraints

Step 2: Filter by thermodynamic stability
- Query Materials Project database via Pymatgen
- Calculate formation energy from elements
- Calculate energy above convex hull (E_hull)
- Filter: E_hull < 50 meV/atom (likely stable)
- Retain ~2,000 thermodynamically plausible compounds

Step 3: Predict crystal structures
- Use Pymatgen structure predictor
- Generate most likely crystal structures for each composition
- Consider common structure types: LISICON, NASICON, garnet, perovskite
- Calculate structural descriptors

Step 4: Calculate material properties with Pymatgen
- Lattice parameters and volume
- Density
- Packing fraction
- Ionic radii and bond lengths
- Coordination environments

Step 5: Feature engineering with Pymatgen
- Calculate compositional features using Pymatgen's featurizers:
  * Elemental property statistics (electronegativity, ionic radius)
  * Valence electron concentrations
  * Stoichiometric attributes
- Calculate structural features:
  * Pore size distribution
  * Site disorder parameters
  * Partial radial distribution functions

Step 6: Build ML models for Li+ conductivity prediction
- Collect training data from literature (experimental conductivities)
- Train ensemble models with scikit-learn:
  * Random Forest
  * Gradient Boosting
  * Neural Network
- Use 5-fold cross-validation
- Predict ionic conductivity for all candidates

Step 7: Predict additional properties
- Electrochemical stability window (ML model)
- Mechanical properties (bulk modulus, shear modulus)
- Interfacial resistance (estimate from structure)
- Synthesis temperature (ML prediction from similar compounds)

Step 8: Multi-objective optimization with PyMOO
Define optimization objectives:
- Maximize: ionic conductivity (>10^-3 S/cm target)
- Maximize: electrochemical window (>4.5V target)
- Minimize: synthesis temperature (<800C preferred)
- Minimize: cost (based on elemental abundance)

Run NSGA-II to find Pareto optimal solutions
Extract top 50 candidates from Pareto front

Step 9: Analyze Pareto optimal materials
- Identify composition trends (which elements appear frequently)
- Analyze structure-property relationships
- Calculate trade-offs between objectives
- Identify "sweet spot" compositions

Step 10: Validate predictions with DFT calculations
- Select top 10 candidates for detailed study
- Set up DFT calculations using Pymatgen's interface
- Calculate:
  * Accurate formation energies
  * Li+ migration barriers (NEB calculations)
  * Electronic band gap
  * Elastic constants
- Compare DFT results with ML predictions

Step 11: Literature and patent search
- Search for prior art on top candidates
- PubMed and Google Scholar: "[composition] AND electrolyte"
- USPTO: Check for existing patents on similar compositions
- Identify any experimental reports on related materials

Step 12: Generate materials discovery report
- Summary of screening workflow and statistics
- Pareto front visualization (conductivity vs stability vs cost)
- Structure visualization of top candidates
- Property comparison table
- Composition-property trend analysis
- DFT validation results
- Predicted performance vs state-of-art materials
- Synthesis recommendations
- IP landscape summary
- Prioritized list of 5-10 materials for experimental validation
- Export as publication-ready PDF

Expected Output:
- Screened library of 10,000+ materials
- ML models for property prediction
- Pareto-optimal set of 50 candidates
- Detailed analysis of top 10 materials
- DFT validation results
- Comprehensive materials discovery report
```

---

## Experimental Physics & Data Analysis

### Example 4: Analysis of Particle Physics Detector Data

**Objective**: Analyze experimental data from particle detector to identify signal events and measure physical constants.

**Skills Used**:
- `astropy` - Units and constants
- `sympy` - Symbolic mathematics
- `statistical-analysis` - Statistical analysis
- `scikit-learn` - Classification
- `stable-baselines3` - Reinforcement learning for optimization
- `matplotlib` - Visualization
- `seaborn` - Statistical plots
- `statsmodels` - Hypothesis testing
- `dask` - Large-scale data processing
- `vaex` - Out-of-core dataframes
- `plotly` - Interactive visualization

**Workflow**:

```bash
Step 1: Load and inspect detector data
- Load ROOT files or HDF5 with raw detector signals
- Use Vaex for out-of-core processing (TBs of data)
- Inspect data structure: event IDs, timestamps, detector channels
- Extract key observables:
  * Energy deposits in calorimeters
  * Particle trajectories from tracking detectors
  * Time-of-flight measurements
  * Trigger information

Step 2: Apply detector calibration and corrections
- Load calibration constants
- Apply energy calibrations to convert ADC to physical units
- Correct for detector efficiency variations
- Apply geometric corrections (alignment)
- Use Astropy units for unit conversions (eV, GeV, MeV)
- Account for dead time and detector acceptance

Step 3: Event reconstruction
- Cluster energy deposits to form particle candidates
- Reconstruct particle trajectories (tracks)
- Match tracks to calorimeter clusters
- Calculate invariant masses for particle identification
- Compute momentum and energy for each particle
- Use Dask for parallel processing across events

Step 4: Event selection and filtering
- Define signal region based on physics hypothesis
- Apply quality cuts:
  * Track quality (chi-squared, number of hits)
  * Fiducial volume cuts
  * Timing cuts (beam window)
  * Particle identification cuts
- Estimate trigger efficiency
- Calculate event weights for corrections

Step 5: Background estimation
- Identify background sources:
  * Cosmic rays
  * Beam-related backgrounds
  * Detector noise
  * Physics backgrounds (non-signal processes)
- Simulate backgrounds using Monte Carlo (if available)
- Estimate background from data in control regions
- Use sideband subtraction method

Step 6: Signal extraction
- Fit invariant mass distributions to extract signal
- Use scipy for likelihood fitting:
  * Signal model: Gaussian or Breit-Wigner
  * Background model: polynomial or exponential
  * Combined fit with maximum likelihood
- Calculate signal significance (S/sqrt(B) or Z-score)
- Estimate systematic uncertainties

Step 7: Machine learning event classification
- Train classifier with scikit-learn to separate signal from background
- Features: kinematic variables, topology, detector response
- Models: Boosted Decision Trees (XGBoost), Neural Networks
- Cross-validate with k-fold CV
- Optimize selection criteria using ROC curves
- Calculate signal efficiency and background rejection

Step 8: Reinforcement learning for trigger optimization
- Use Stable-Baselines3 to optimize trigger thresholds
- Environment: detector simulator
- Action: adjust trigger thresholds
- Reward: maximize signal efficiency while controlling rate
- Train PPO or SAC agent
- Validate on real data

Step 9: Calculate physical observables
- Measure cross-sections:
  * sigma = N_signal / (epsilon x L x BR)
  * N_signal: number of signal events
  * epsilon: detection efficiency
  * L: integrated luminosity
  * BR: branching ratio
- Use Sympy for symbolic error propagation
- Calculate with Astropy for proper unit handling

Step 10: Statistical analysis and hypothesis testing
- Perform hypothesis tests with statsmodels:
  * Likelihood ratio test for signal vs background-only
  * Calculate p-values and significance levels
  * Set confidence limits (CLs method)
- Bayesian analysis for parameter estimation
- Calculate confidence intervals and error bands

Step 11: Systematic uncertainty evaluation
- Identify sources of systematic uncertainty:
  * Detector calibration uncertainties
  * Background estimation uncertainties
  * Theoretical uncertainties (cross-sections, PDFs)
  * Monte Carlo modeling uncertainties
- Propagate uncertainties through analysis chain
- Combine statistical and systematic uncertainties
- Present as error budget

Step 12: Create comprehensive physics report
- Event displays showing candidate signal events
- Kinematic distributions (momentum, energy, angles)
- Invariant mass plots with fitted signal
- ROC curves for ML classifiers
- Cross-section measurements with error bars
- Comparison with theoretical predictions
- Systematic uncertainty breakdown
- Statistical significance calculations
- Interpretation:
  * Consistency with Standard Model
  * Constraints on new physics parameters
  * Discovery potential or exclusion limits
- Recommendations:
  * Detector improvements
  * Additional data needed
  * Future analysis strategies
- Export publication-ready PDF formatted for physics journal

Expected Output:
- Reconstructed physics events
- Signal vs background classification
- Measured cross-sections and branching ratios
- Statistical significance of observations
- Systematic uncertainty analysis
- Comprehensive experimental physics paper
```

---

## Chemical Engineering & Process Optimization

### Example 5: Optimization of Chemical Reactor Design and Operation

**Objective**: Design and optimize a continuous chemical reactor for maximum yield and efficiency while meeting safety and economic constraints.

**Skills Used**:
- `sympy` - Symbolic equations and reaction kinetics
- `statistical-analysis` - Numerical analysis
- `pymoo` - Multi-objective optimization
- `simpy` - Process simulation
- `pymc` - Bayesian parameter estimation
- `scikit-learn` - Process modeling
- `stable-baselines3` - Real-time control optimization
- `matplotlib` - Process diagrams
- `plotly` - Interactive process visualization
- `fluidsim` - Fluid dynamics simulation
- `scientific-writing` - Engineering reports
- `pdf` - Technical documentation

**Workflow**:

```bash
Step 1: Define reaction system and kinetics
- Chemical reaction: A + B -> C + D
- Use Sympy to define symbolic rate equations:
  * Arrhenius equation: k = A x exp(-Ea/RT)
  * Rate law: r = k x [A]^alpha x [B]^beta
- Define material and energy balances symbolically
- Include equilibrium constants and thermodynamics
- Account for side reactions and byproducts

Step 2: Develop reactor model
- Select reactor type: CSTR, PFR, batch, or semi-batch
- Write conservation equations:
  * Mass balance: dC/dt = (F_in x C_in - F_out x C)/V + r
  * Energy balance: rho*Cp x dT/dt = Q - dH_rxn x r x V
  * Momentum balance (pressure drop)
- Include heat transfer correlations
- Model mixing and mass transfer limitations

Step 3: Parameter estimation with PyMC
- Load experimental data from pilot reactor
- Bayesian inference to estimate kinetic parameters:
  * Pre-exponential factor (A)
  * Activation energy (Ea)
  * Reaction orders (alpha, beta)
- Use MCMC sampling with PyMC
- Incorporate prior knowledge from literature
- Calculate posterior distributions and credible intervals
- Assess parameter uncertainty and correlation

Step 4: Model validation
- Simulate reactor with estimated parameters using scipy.integrate
- Compare predictions with experimental data
- Calculate goodness of fit (R2, RMSE)
- Perform sensitivity analysis:
  * Which parameters most affect yield?
  * Identify critical operating conditions
- Refine model if needed

Step 5: Machine learning surrogate model
- Train fast surrogate model with scikit-learn
- Generate training data from detailed model (1000+ runs)
- Features: T, P, residence time, feed composition, catalyst loading
- Target: yield, selectivity, conversion
- Models: Gaussian Process Regression, Random Forest
- Validate surrogate accuracy (R2 > 0.95)
- Use for rapid optimization

Step 6: Single-objective optimization
- Maximize yield with scipy.optimize:
  * Decision variables: T, P, feed ratio, residence time
  * Objective: maximize Y = (moles C produced) / (moles A fed)
  * Constraints:
    - Temperature: 300 K <= T <= 500 K (safety)
    - Pressure: 1 bar <= P <= 50 bar (equipment limits)
    - Residence time: 1 min <= tau <= 60 min
    - Conversion: X_A >= 90%
- Use Sequential Least Squares Programming (SLSQP)
- Identify optimal operating point

Step 7: Multi-objective optimization with PyMOO
- Competing objectives:
  1. Maximize product yield
  2. Minimize energy consumption (heating/cooling)
  3. Minimize operating cost (raw materials, utilities)
  4. Maximize reactor productivity (throughput)
- Constraints:
  - Safety: temperature and pressure limits
  - Environmental: waste production limits
  - Economic: minimum profitability
- Run NSGA-II or NSGA-III
- Generate Pareto front of optimal solutions
- Select operating point based on preferences

Step 8: Dynamic process simulation with SimPy
- Model complete plant:
  * Reactors, separators, heat exchangers
  * Pumps, compressors, valves
  * Storage tanks and buffers
- Simulate startup, steady-state, and shutdown
- Include disturbances:
  * Feed composition variations
  * Equipment failures
  * Demand fluctuations
- Evaluate dynamic stability
- Calculate time to steady state

Step 9: Control system design
- Design feedback control loops:
  * Temperature control (PID controller)
  * Pressure control
  * Flow control
  * Level control
- Tune PID parameters using Ziegler-Nichols or optimization
- Implement cascade control for improved performance
- Add feedforward control for disturbance rejection

Step 10: Reinforcement learning for advanced control
- Use Stable-Baselines3 to train RL agent:
  * Environment: reactor simulation (SimPy-based)
  * State: T, P, concentrations, flow rates
  * Actions: adjust setpoints, flow rates, heating/cooling
  * Reward: +yield -energy cost -deviation from setpoint
- Train PPO or TD3 agent
- Compare with conventional PID control
- Evaluate performance under disturbances
- Implement model-free adaptive control

Step 11: Economic analysis
- Calculate capital costs (CAPEX):
  * Reactor vessel cost (function of size, pressure rating)
  * Heat exchanger costs
  * Pumps and instrumentation
  * Installation costs
- Calculate operating costs (OPEX):
  * Raw materials (A, B, catalyst)
  * Utilities (steam, cooling water, electricity)
  * Labor and maintenance
- Revenue from product sales
- Calculate economic metrics:
  * Net present value (NPV)
  * Internal rate of return (IRR)
  * Payback period
  * Levelized cost of production

Step 12: Safety analysis
- Identify hazards:
  * Exothermic runaway reactions
  * Pressure buildup
  * Toxic or flammable materials
- Perform HAZOP-style analysis
- Calculate safe operating limits:
  * Maximum temperature of synthesis reaction (MTSR)
  * Adiabatic temperature rise
  * Relief valve sizing
- Design emergency shutdown systems
- Implement safety interlocks

Step 13: Uncertainty quantification
- Propagate parameter uncertainties from PyMC:
  * How does kinetic parameter uncertainty affect yield?
  * Monte Carlo simulation with parameter distributions
- Evaluate robustness of optimal design
- Calculate confidence intervals on economic metrics
- Identify critical uncertainties for further study

Step 14: Generate comprehensive engineering report
- Executive summary of project objectives and results
- Process flow diagram (PFD) with material and energy streams
- Reaction kinetics and model equations
- Parameter estimation results with uncertainties
- Optimization results:
  * Pareto front for multi-objective optimization
  * Recommended operating conditions
  * Trade-off analysis
- Dynamic simulation results (startup curves, response to disturbances)
- Control system design and tuning
- Economic analysis with sensitivity to key assumptions
- Safety analysis and hazard mitigation
- Scale-up considerations:
  * Pilot to commercial scale
  * Heat and mass transfer limitations
  * Equipment sizing
- Recommendations:
  * Optimal reactor design (size, type, materials of construction)
  * Operating conditions for maximum profitability
  * Control strategy
  * Further experimental studies needed
- Technical drawings and P&ID (piping and instrumentation diagram)
- Export as professional engineering report (PDF)

Expected Output:
- Validated reactor model with parameter uncertainties
- Optimal reactor design and operating conditions
- Pareto-optimal solutions for multi-objective optimization
- Dynamic process simulation results
- Advanced control strategies (RL-based)
- Economic feasibility analysis
- Safety assessment
- Comprehensive chemical engineering design report
```

---

## Scientific Illustration & Visual Communication

### Example 6: Creating Publication-Ready Scientific Figures

**Objective**: Generate and refine scientific illustrations, diagrams, and graphical abstracts for publications and presentations.

**Skills Used**:
- `generate-image` - AI image generation and editing
- `matplotlib` - Data visualization
- `plotly` - Interactive visualization
- `scientific-visualization` - Best practices
- `scientific-schematics` - Scientific diagrams
- `scientific-writing` - Figure caption creation
- `scientific-slides` - Presentation materials
- `latex-posters` - Conference posters
- `pptx-posters` - PowerPoint posters
- `pdf` - PDF report generation

**Workflow**:

```bash
Step 1: Plan visual communication strategy
- Identify key concepts that need visual representation:
  * Experimental workflow diagrams
  * Molecular structures and interactions
  * Data visualization (handled by matplotlib)
  * Conceptual illustrations for mechanisms
  * Graphical abstract for paper summary
- Determine appropriate style for target journal/audience
- Sketch rough layouts for each figure

Step 2: Generate experimental workflow diagram
- Use generate-image skill with detailed prompt:
  "Scientific illustration showing a step-by-step experimental 
  workflow for CRISPR gene editing: (1) guide RNA design at computer,
  (2) cell culture in petri dish, (3) electroporation device,
  (4) selection with antibiotics, (5) sequencing validation.
  Clean, professional style with numbered steps, white background,
  suitable for scientific publication."
- Save as workflow_diagram.png
- Review and iterate on prompt if needed

Step 3: Create molecular interaction schematic
- Generate detailed molecular visualization:
  "Scientific diagram of protein-ligand binding mechanism:
  show receptor protein (blue ribbon structure) with binding pocket,
  small molecule ligand (ball-and-stick, orange) approaching,
  key hydrogen bonds indicated with dashed lines, water molecules
  in binding site. Professional biochemistry illustration style,
  clean white background, publication quality."
- Generate multiple versions with different angles/styles
- Select best representation

Step 4: Edit existing figures for consistency
- Load existing figure that needs modification:
  python scripts/generate_image.py "Change the background to white
  and make the protein blue instead of green" --input figure1.png
- Standardize color schemes across all figures
- Edit to match journal style guidelines:
  python scripts/generate_image.py "Remove the title text and
  increase contrast for print publication" --input diagram.png

Step 5: Generate graphical abstract
- Create comprehensive visual summary:
  "Graphical abstract for cancer immunotherapy paper: left side
  shows tumor cells (irregular shapes, red) being attacked by
  T cells (round, blue). Center shows the drug molecule structure.
  Right side shows healthy tissue (green). Arrow flow from left
  to right indicating treatment progression. Modern, clean style
  with minimal text, high contrast, suitable for journal TOC."
- Ensure dimensions meet journal requirements
- Iterate to highlight key findings

Step 6: Create conceptual mechanism illustrations
- Generate mechanism diagrams:
  "Scientific illustration of enzyme catalysis mechanism:
  Show substrate entering active site (step 1), transition state
  formation with electron movement arrows (step 2), product
  release (step 3). Use standard biochemistry notation,
  curved arrows for electron movement, clear labeling."
- Generate alternative representations for supplementary materials

Step 7: Produce presentation-ready figures
- Create high-impact visuals for talks:
  "Eye-catching scientific illustration of DNA double helix
  unwinding during replication, with DNA polymerase (large
  green structure) adding nucleotides. Dynamic composition,
  vibrant but professional colors, dark background for
  presentation slides."
- Adjust style for poster vs slide format
- Create versions at different resolutions

Step 8: Generate figure panels for multi-part figures
- Create consistent series of related images:
  "Panel A: Normal cell with intact membrane (green outline)
  Panel B: Cell under oxidative stress with damaged membrane
  Panel C: Cell treated with antioxidant, membrane recovering
  Consistent style across all panels, same scale, white background,
  scientific illustration style suitable for publication."
- Ensure visual consistency across panels
- Annotate with panel labels

Step 9: Edit for accessibility
- Modify figures for colorblind accessibility:
  python scripts/generate_image.py "Change the red and green
  elements to blue and orange for colorblind accessibility,
  maintain all other aspects" --input figure_v1.png
- Add patterns or textures for additional differentiation
- Verify contrast meets accessibility standards

Step 10: Create supplementary visual materials
- Generate additional context figures:
  "Anatomical diagram showing location of pancreatic islets
  within the pancreas, cross-section view with labeled structures:
  alpha cells, beta cells, blood vessels. Medical illustration
  style, educational, suitable for supplementary materials."
- Create protocol flowcharts and decision trees
- Generate equipment setup diagrams

Step 11: Compile figure legends and captions
- Use scientific-writing skill to create descriptions:
  * Figure number and title
  * Detailed description of what is shown
  * Explanation of symbols, colors, and abbreviations
  * Scale bars and measurement units
  * Statistical information if applicable
- Format according to journal guidelines

Step 12: Assemble final publication package
- Organize all figures in publication order
- Create high-resolution exports (300+ DPI for print)
- Generate both RGB (web) and CMYK (print) versions
- Compile into PDF using pdf skill:
  * Title page with graphical abstract
  * All figures with captions
  * Supplementary figures section
- Create separate folder with individual figure files
- Document all generation prompts for reproducibility

Expected Output:
- Complete set of publication-ready scientific illustrations
- Graphical abstract for table of contents
- Mechanism diagrams and workflow figures
- Edited versions meeting journal style guidelines
- Accessibility-compliant figure versions
- Figure package with captions and metadata
- Documentation of prompts used for reproducibility
```

---

## Quantum Computing for Chemistry

### Example 7: Variational Quantum Eigensolver for Molecular Ground States

**Objective**: Use quantum computing to calculate molecular electronic structure and ground state energies for drug design applications.

**Skills Used**:
- `qiskit` - IBM quantum computing framework
- `pennylane` - Quantum machine learning
- `cirq` - Google quantum circuits
- `qutip` - Quantum dynamics simulation
- `sympy` - Symbolic Hamiltonian construction
- `matplotlib` - Energy landscape visualization
- `scientific-visualization` - Publication figures
- `scientific-writing` - Quantum chemistry reports

> **Note**: Molecular structure input (e.g., from SMILES strings) may require installing RDKit or similar cheminformatics tools separately, as RDKit is not a curated skill in this collection.

**Workflow**:

```bash
Step 1: Define molecular system
- Load molecular structure (small drug molecule)
- Extract atomic coordinates and nuclear charges
- Define basis set (STO-3G, 6-31G for small molecules)
- Calculate number of qubits needed (2 qubits per orbital)

Step 2: Construct molecular Hamiltonian
- Use Qiskit Nature to generate fermionic Hamiltonian
- Apply Jordan-Wigner transformation to qubit Hamiltonian
- Use SymPy to symbolically verify Hamiltonian terms
- Calculate number of Pauli terms

Step 3: Design variational ansatz with Qiskit
- Choose ansatz type: UCCSD, hardware-efficient, or custom
- Define circuit depth and entanglement structure
- Calculate circuit parameters (variational angles)
- Estimate circuit resources (gates, depth)

Step 4: Implement VQE algorithm
- Initialize variational parameters randomly
- Define cost function: <psi(theta)|H|psi(theta)>
- Choose classical optimizer (COBYLA, SPSA, L-BFGS-B)
- Set convergence criteria

Step 5: Run quantum simulation with PennyLane
- Configure quantum device (simulator or real hardware)
- Execute variational circuits
- Measure expectation values of Hamiltonian terms
- Update parameters iteratively

Step 6: Error mitigation
- Implement readout error mitigation
- Apply zero-noise extrapolation
- Use measurement error correction
- Estimate uncertainty in energy values

Step 7: Quantum dynamics with QuTiP
- Simulate molecular dynamics on quantum computer
- Calculate time evolution of molecular system
- Study non-adiabatic transitions
- Visualize wavefunction dynamics

Step 8: Compare with classical methods
- Run classical HF and DFT calculations for reference
- Compare VQE results with CCSD(T) (gold standard)
- Analyze quantum advantage for this system
- Quantify accuracy vs computational cost

Step 9: Scale to larger molecules
- Design circuits for larger drug candidates
- Estimate resources for pharmaceutical applications
- Identify molecules where quantum advantage is expected
- Plan for near-term quantum hardware capabilities

Step 10: Generate quantum chemistry report
- Energy convergence plots
- Circuit diagrams and ansatz visualizations
- Comparison with classical methods
- Resource estimates for target molecules
- Discussion of quantum advantage timeline
- Publication-quality figures
- Export comprehensive report

Expected Output:
- Molecular ground state energies from VQE
- Optimized variational circuits
- Comparison with classical chemistry methods
- Resource estimates for drug molecules
- Quantum chemistry analysis report
```

---

## Research Grant Writing

### Example 8: NIH R01 Grant Proposal Development

**Objective**: Develop a comprehensive research grant proposal with literature review, specific aims, and budget justification.

**Skills Used**:
- `database-lookup` - Query ClinicalTrials.gov for preliminary data context
- `paper-lookup` - Search PubMed, OpenAlex for literature and citations
- `research-grants` - Grant writing templates and guidelines
- `literature-review` - Systematic literature analysis
- `hypothesis-generation` - Scientific hypothesis development
- `scientific-writing` - Technical writing
- `scientific-critical-thinking` - Research design
- `citation-management` - Reference formatting
- `pdf` - PDF generation

**Workflow**:

```bash
Step 1: Define research question and significance
- Use hypothesis-generation skill to refine research questions
- Identify knowledge gaps in the field
- Articulate significance and innovation
- Define measurable outcomes

Step 2: Comprehensive literature review
- Search PubMed for relevant publications (last 10 years)
- Query OpenAlex for citation networks
- Identify key papers and review articles
- Use literature-review skill to synthesize findings
- Identify gaps that proposal will address

Step 3: Develop specific aims
- Aim 1: Mechanistic studies (hypothesis-driven)
- Aim 2: Translational applications
- Aim 3: Validation and clinical relevance
- Ensure aims are interdependent but not contingent
- Define success criteria for each aim

Step 4: Design research approach
- Use scientific-critical-thinking for experimental design
- Define methods for each specific aim
- Include positive and negative controls
- Plan statistical analysis approach
- Identify potential pitfalls and alternatives

Step 5: Preliminary data compilation
- Gather existing data supporting hypothesis
- Search ClinicalTrials.gov for relevant prior work
- Create figures showing preliminary results
- Quantify feasibility evidence

Step 6: Innovation and significance sections
- Articulate what is novel about approach
- Compare to existing methods/knowledge
- Explain expected impact on field
- Address NIH mission alignment

Step 7: Timeline and milestones
- Create Gantt chart for 5-year project
- Define quarterly milestones
- Identify go/no-go decision points
- Plan for personnel and resource allocation

Step 8: Budget development
- Calculate personnel costs (PI, postdocs, students)
- Equipment and supplies estimates
- Core facility usage costs
- Travel and publication costs
- Indirect cost calculation

Step 9: Rigor and reproducibility
- Address biological variables (sex, age, strain)
- Statistical power calculations
- Data management and sharing plan
- Authentication of key resources

Step 10: Format and compile
- Use research-grants templates for NIH format
- Apply citation-management for references
- Create biosketch and facilities sections
- Generate PDF with proper formatting
- Check page limits and formatting requirements

Step 11: Review and revision
- Use peer-review skill principles for self-assessment
- Check for logical flow and clarity
- Verify alignment with FOA requirements
- Ensure responsive to review criteria

Step 12: Final deliverables
- Specific Aims page (1 page)
- Research Strategy (12 pages)
- Bibliography
- Budget and justification
- Biosketches
- Letters of support
- Data management plan
- Human subjects/vertebrate animals sections (if applicable)

Expected Output:
- Complete NIH R01 grant proposal
- Literature review summary
- Budget spreadsheet with justification
- Timeline and milestone chart
- All required supplementary documents
- Properly formatted PDF ready for submission
```

---

## Summary

These examples demonstrate:

1. **Cross-domain applicability**: Skills are useful across many scientific fields
2. **Skill integration**: Complex workflows combine multiple databases, packages, and analysis methods
3. **Real-world relevance**: Examples address actual research questions and clinical needs
4. **End-to-end workflows**: From data acquisition to publication-ready reports
5. **Best practices**: QC, statistical rigor, visualization, interpretation, and documentation
