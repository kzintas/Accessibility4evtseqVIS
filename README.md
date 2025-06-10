# Accessibility for Process Visualizations: A VQA Evaluation Dataset

This repository contains a comprehensive Visual Question Answering (VQA) dataset for evaluating the accessibility and interpretability of process visualizations across different visualization techniques and information density levels.

## Overview

The dataset includes questions and answers for three different node-link visualization techniques across two real-world datasets.

## Dataset Structure

### Visualization Techniques
1. **CoreFlow** - Tree-based visualization for event sequences
2. **SentenTree** - Graph-based hierarchical visualization
3. **Sequence Synopsis** - Timeline-based synopsis visualization

### Datasets
1. **Emergency Dataset** - Medical emergency patient flow data
2. **UMD vs UNC Basketball** - Sports event sequence data

### Information Levels
- **5, 10, 15, 20, 25, 30** - Different levels of detail/aggregation in the visualizations

## Directory Structure

```
├── images/                           # Visualization images
│   ├── CoreFlow/
│   │   ├── emergency_dataset/        # Emergency patient flow visualizations
│   │   └── umdvsunc_D2O_basketball/  # Basketball game visualizations
│   ├── SentenTree/
│   │   ├── emergency_dataset/
│   │   └── umdvsunc_D2O_basketball/
│   └── Sequence Synopsis/
│       ├── emergency_dataset/
│       └── umdvsunc_D2O_basketball/
└── VQA/
    └── VQA Event Sequence - Sheet3_new_file_path.csv  # Main dataset
```

## VQA Dataset

The main dataset (`VQA Event Sequence - Sheet3_new_file_path.csv`) contains:

### Columns:
- **Dataset**: The source dataset (emergency, UMDvsUNC)
- **Visualization**: The visualization technique used (coreflow, sententree, seq_synopsis)
- **Granularity**: Level of detail (5-30)
- **Image**: Path to the corresponding visualization image
- **Question Number**: Sequential question identifier
- **Question**: The visual question asked
- **Final Task**: The cognitive task category
- **Option 1-4**: Multiple choice answers
- **Correct Answer**: The correct option
- **Comment**: Additional notes or calculations

### Task Categories:
1. **Accurately Read Edge Weights** - Reading specific numerical values from the visualization
2. **Summing Weights** - Calculating totals across multiple paths or elements
3. **Detect Antecedent Sequealea** - Identifying sequential relationships and transitions
4. **Detect if Edge is Present** - Determining the existence of connections or relationships

## Research Applications

This dataset can be used for:

- **Accessibility Research**: Evaluating how well different visualizations can be interpreted through questions
- **Visualization Effectiveness**: Comparing the interpretability of different event sequence visualization techniques
- **VQA Model Training**: Training and evaluating visual question answering models on specialized visualization content
- **Cognitive Load Analysis**: Understanding the difficulty of different types of visual reasoning tasks

## Example Questions

### Emergency Dataset Examples:
- "How many patients died after arriving at Emergency?"
- "How many total patients were discharged alive?"
- "How many patients went to the ICU after Emergency?"

### Basketball Dataset Examples:
- "How many rebounds were made by UMD Offense?"
- "How many times did UMD Offense transition from UNC Offense?"
- "How many shots were made directly after a Rebound?"

## Usage

The dataset is structured for easy integration with VQA frameworks and can be used to:

1. **Load visualization images** from the `images/` directory
2. **Parse questions and answers** from the CSV file
3. **Evaluate model performance** across different visualization types and granularities
4. **Analyze task difficulty** by cognitive task category

## Data Statistics

- **Total Questions**: ~144 questions across all visualizations
- **Visualization Types**: 3 different techniques
- **Datasets**: 2 real-world scenarios
- **Granularity Levels**: 6 different detail levels
- **Task Types**: 4 cognitive task categories

## Citation

If you use this dataset in your research, please cite:

```bibtex
@dataset{accessibility_evtseq_vqa,
  title={Evaluating VLMs as Accessibility Bridges for Process Visualizations},
  author={[Kazi Tasnim Zinat, Saad Mohammad Abrar, Sharmila Duppala, Saimadhav Naga Sakhamuri, Zhicheng Liu]},
  year={2025},
  institution={University of Maryland, College Park},
}
```

## License

This dataset is provided under MIT License. Please refer to the original data sources for usage restrictions.

## Contact

For questions about this dataset, please contact kzintas@umd.edu.
