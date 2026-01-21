# Pellin Web Tool - Sequencing Data Analysis Platform

A web-based prototype for RNA-seq data analysis, designed for the Pellin Lab. This tool provides an intuitive interface for uploading paired-end FASTQ files, configuring differential gene expression (DEG) analysis parameters, and visualizing sequencing quality metrics.

## Overview

The Pellin Web Tool is a mockup demonstration of a sequencing data analysis platform that streamlines the workflow from raw FASTQ file upload through quality control visualization. This prototype showcases the intended user experience for researchers working with RNA-seq data.

## Features

### 1. File Upload Interface ([docs/index.html](docs/index.html))
- **Paired-End Read Upload**: Support for both R1 and R2 FASTQ files
- **Drag-and-Drop Functionality**: Intuitive file selection via click or drag-and-drop
- **Supported Formats**: `.fastq`, `.fq`, `.fastq.gz`, `.fq.gz`
- **File Validation**: Real-time feedback on uploaded files

### 2. DEG Analysis Configuration
The tool provides comprehensive options for differential gene expression analysis:

#### Alignment Settings
- **Alignment Algorithms**: STAR (recommended), HISAT2, TopHat2
- **Reference Genomes**: 
  - Human: GRCh38/hg38, GRCh37/hg19
  - Mouse: mm10, mm39
  - Custom reference support
- **Parameters**:
  - Multi-mapping reads option
  - Strand-specific alignment

#### Expression Level Analysis
- **Quantification Methods**: featureCounts, HTSeq, Salmon, Kallisto
- **Normalization Methods**: TPM, FPKM, RPKM, DESeq2
- **Configurable Expression Threshold**: Minimum expression value filter

#### Gene Annotation & Naming
- **Gene ID Types**: Ensembl, Entrez, Gene Symbol, RefSeq
- **Annotation Databases**: Ensembl, GENCODE, RefSeq, UCSC
- **Additional Annotations**:
  - Gene descriptions
  - Gene biotype
  - Chromosome location

### 3. Results Visualization ([docs/results.html](docs/results.html))
Interactive results page featuring:

#### Summary Cards
- Total reads processed
- Average quality score (Phred scale)
- GC content percentage
- Sequence length

#### Quality Visualizations
- **Quality Score Distribution**: Per-base quality scores for R1 and R2 reads
- **Base Composition**: Pie chart showing A, T, G, C percentages
- **Read Length Distribution**: Histogram of read lengths across the dataset

### 4. Script Editor ([docs/scripts.html](docs/scripts.html))
An integrated code editor for customizing analysis visualizations:
- **Monaco-style Code Editor**: Dark theme with syntax highlighting
- **Editable Visualization Scripts**:
  - Quality score distribution chart
  - Base composition chart
  - Read length distribution histogram
- **Live Edit Capability**: Modify JavaScript rendering code
- **Reset Functionality**: Restore default scripts

## Project Structure

```
pellinwebtool-mockup1/
├── README.md
└── docs/
    ├── index.html      # Main upload and configuration page
    ├── results.html    # Analysis results and visualizations
    └── scripts.html    # Script editor for customization
```

## User Workflow

1. **Upload Files**: Navigate to the main page and upload paired R1 and R2 FASTQ files
2. **Configure Analysis**: Switch to the "DEG Analysis Options" tab to customize analysis parameters
3. **Run Analysis**: Click "Analyze Sequences" to initiate processing
4. **View Results**: Automatically navigate to the results page to explore quality metrics and visualizations
5. **Customize (Optional)**: Use the script editor to modify visualization code

## Technical Implementation

### Frontend Technologies
- **HTML5/CSS3**: Modern, responsive design with gradient styling
- **JavaScript**: Interactive file handling, form validation, and data visualization
- **Canvas API**: Custom chart rendering for quality metrics
- **LocalStorage**: Client-side data persistence between pages

### Design Features
- **Gradient Color Scheme**: Blue gradient theme (from #1e3a8a to #60a5fa)
- **Responsive Layout**: Adapts to different screen sizes
- **Smooth Animations**: Fade-in effects and hover transitions
- **Drag-and-Drop**: Native file upload with visual feedback

## Requirements

- Modern web browser with JavaScript enabled
- Canvas API support for visualizations
- LocalStorage support for data persistence

## Development Status

**Current Version**: Prototype/Mockup v1.0

This is a demonstration prototype showcasing the intended user interface and workflow. The analysis functionality uses simulated data and does not perform actual bioinformatics processing.

## Future Development

Planned enhancements for production version:
- Backend integration for actual sequence analysis
- Real bioinformatics pipeline integration (STAR, featureCounts, etc.)
- User authentication and session management
- Results export functionality (CSV, PDF reports)
- Batch file processing
- Advanced filtering and comparison tools

## Usage

To view the prototype:

1. Click [`the link`](https://swamyshogan.github.io/pellinwebtool-mockup1/)
2. Upload sample FASTQ files (or use any files for demo purposes)
3. Configure analysis options as desired
4. Click "Analyze Sequences" to proceed to results
5. Explore the visualizations and script editor

## Contact

Developed for the Pellin Lab

---

**Note**: This is a mockup/prototype for demonstration purposes. All analysis results shown are simulated and do not represent actual sequencing data analysis.
