# Structured Reasoning Frameworks for LLM-Based Venture Capital Evaluation

**Supporting Materials and Data Repository**

This repository contains the complete dataset, evaluation resources, and results for the research paper:

**Structured Reasoning Frameworks for LLM-Based Venture Capital Evaluation: Integrating Systems Engineering and Business Analysis**

Dan Velarde, Stephen Gillespie  
United States Military Academy, West Point, New York, USA

## Abstract

Venture capital decision-making for early-stage startups involves high uncertainty and relies heavily on qualitative reasoning from pitch decks. This study investigates whether large language models (LLMs) equipped with structured knowledge frameworks can improve predictive accuracy in startup evaluation. We designed four evaluation personas using Gemini 2.5 Pro Preview: a baseline model, a venture capital-informed model, a systems engineering-guided model using established standards from IEEE, INCOSE, NASA, and MITRE, and a combined model integrating both frameworks. Testing on 14 historical pitch decks from companies including LinkedIn, Theranos, and WeWork, the combined persona achieved 85.7% accuracy in predicting startup outcomes, outperforming specialized and baseline configurations. The systems engineering rubric provided quantitative risk assessment while the venture capital knowledge stack enhanced market opportunity identification. Results demonstrate that LLMs can function as structured reasoning engines when constrained by domain-specific frameworks, offering transparent and auditable decision support for high-uncertainty investment environments.

## Research Overview

### Key Findings
- Combined Framework Accuracy: 85.7% prediction accuracy
- Systems Engineering Framework: 64.3% accuracy (conservative, technically rigorous)
- Venture Capital Framework: 64.3% accuracy (market-focused, optimistic bias)
- Baseline Model: 78.6% accuracy

### Methodology
Four evaluation personas were tested:
1. Basic Persona - Control model with no domain knowledge
2. Venture Capital Persona - Informed by VC literature and industry best practices
3. Systems Engineering Persona - Guided by IEEE, INCOSE, NASA, and MITRE standards
4. Combined Persona - Integrated both frameworks for balanced technical and market evaluation

All evaluations used Gemini 2.5 Pro Preview with identical configurations for comparability.

## Repository Contents

### Pitch Deck Dataset

**sucessful_company_pitch_decks/** - 7 successful startup pitch decks
- bufferstartuppitchdeck-190612112003.pdf (Buffer)
- coinbasestartuppitchdeck-190612112004.pdf (Coinbase)
- intercomstartuppitchdeck-190612112012.pdf (Intercom)
- linkedinstartuppitchdeck-190612112013.pdf (LinkedIn)
- matchboxtinderstartuppitchdeck-190612140347.pdf (Tinder)
- monzostartuppitchdeck-190615080041.pdf (Monzo)
- weworkstartuppitchdeck-190612112018.pdf (WeWork)

**failed_company_pitch_decks/** - 7 failed startup pitch decks
- blissstartuppitchdeck-190617123851.pdf
- cardlifestartuppitchdeck-190617123853.pdf
- castlestartuppitchdeck-190612112003.pdf
- flowtabstartuppitchdeck-190612112012.pdf
- limetreestartuppitchdeck-190617123853.pdf
- sec.gov_Archives_edgar_data_1720990_000121390020017291_ea124083ex99-3_spartanenergy.htm.pdf (Spartan Energy)
- theranosstartuppitchdeck-190615080040.pdf (Theranos)

Dataset Characteristics:
- 14 total pitch decks (7 successful, 7 failed)
- All sourced from SlideShare.net
- OCR-processed and manually cleaned for analysis
- Historical outcomes verified through public records

### Knowledge Stacks

**VC_Stack/** - Venture Capital Knowledge Stack

40+ industry documents and academic papers including:
- Due diligence questionnaires and frameworks
- Investment decision-making methodologies
- Valuation techniques and startup lifecycle models
- Case studies and historical market analysis
- Fund structuring and LP/GP relationship guides

Key Sources:
- ILPA Private Equity Principles
- PitchBook-NVCA Venture Monitor Q2 2024
- Academic papers on VC investment patterns
- Industry reports on startup failure patterns
- Deep tech investment frameworks

**SE Resources/** - Systems Engineering Knowledge Stack

Authoritative standards from major SE organizations:
- IEEE Standard 15288-2:2014 - Technical Reviews and Audits on Defense Programs
- INCOSE Systems Engineering Handbook (4th Edition, 2015)
- NASA Systems Engineering Handbook
- MITRE Systems Engineering Guide

**SE Rubric.pdf** - Systems Engineering Evaluation Rubric

Comprehensive 5-category, 20-subcriteria rubric:
- Cost Risk (4 subcriteria × 25 points)
- Schedule Risk (4 subcriteria × 25 points)
- Technical Risk (4 subcriteria × 25 points)
- Programmatic Risk (4 subcriteria × 25 points)
- System Ilities (4 subcriteria × 25 points)
- Total Possible: 100 points per category
- Project Risk Score: Average across all categories

### Results and Analysis

**LLM Data.xlsx** - Complete evaluation dataset
- All 56 persona evaluations (4 personas × 14 decks)
- Decision classifications (Yes/Leaning Yes/Leaning No/No)
- Confidence scores (0-100)
- Reasoning summaries
- Accuracy calculations

**Figures/** - Publication-quality visualizations
- Methodology figure.png - Research workflow diagram
- basic_confusion_matrix.png
- vc_confusion_matrix.png
- se_confusion_matrix.png
- combined_confusion_matrix.png
- confusion_matrices_2x2.png - Comparative view
- decision_distribution_basic_vc_se_combined.png

## Key Research Contributions

1. Novel Integration of SE and VC Frameworks - First study to systematically combine systems engineering standards (IEEE, INCOSE, NASA, MITRE) with venture capital evaluation criteria for LLM-based startup assessment.

2. Unstructured Data Analysis - Unlike prior work using structured datasets, this study evaluates LLMs on authentic pitch decks containing only the information available to real investors.

3. Structured Reasoning Framework - Demonstrates that LLMs can function as structured reasoning engines (not just pattern matchers) when constrained by domain-specific rubrics, enabling transparent decision rationales, auditable evaluation processes, and confidence-calibrated predictions.

4. Error Pattern Analysis - Identified three primary failure modes: Technical Conservatism (SE frameworks reject ventures lacking architectural documentation), Narrative Bias (VC frameworks over-weight founder storytelling), and Information Asymmetry (Conflicting signals lead to misclassification).

## Experimental Configuration

LLM Environment:
- Model: Gemini 2.5 Pro Preview
- Platform: MSTY.ai (local desktop deployment)
- Hardware: NVIDIA RTX 5080, Intel Core i9
- Max Output Tokens: 16,000
- Context Length: 30 messages
- Embedding Model: BERT-based retriever

Evaluation Protocol:
- Single-pass evaluation per deck (mimics real VC review)
- Identical model parameters across all personas
- No external connectivity required (local knowledge base retrieval)

## Reproducibility

All materials required to reproduce the study are included:
1. Original pitch decks (PDF format)
2. Complete knowledge stacks (VC_Stack/ and SE Resources/)
3. Systems Engineering rubric (SE Rubric.pdf)
4. Full evaluation results (LLM Data.xlsx)
5. Analysis figures and visualizations (Figures/)

Note: The specific Gemini 2.5 Pro Preview version used may not be publicly accessible. For replication, use the latest available Gemini Pro model or equivalent (e.g., GPT-4, Claude Opus).

## Usage Instructions

For Researchers:
1. Review the SE rubric to understand evaluation criteria
2. Examine sample pitch decks and their classifications
3. Analyze evaluation results in LLM Data.xlsx
4. Explore error patterns and confidence calibration
5. Adapt frameworks for your own evaluation contexts

For Practitioners:
1. Use the VC and SE knowledge stacks as due diligence checklists
2. Apply the SE rubric to assess technical risk in early-stage ventures
3. Reference the Combined framework approach for balanced evaluation
4. Calibrate confidence thresholds (≥85% shows 91.7% accuracy)

## Limitations

As discussed in the paper:
- Information Leakage: LLM training may include knowledge of high-profile companies
- Sample Size: 14 pitch decks (small for statistical generalization)
- Binary Classification: Success/failure oversimplifies complex outcomes
- Hindsight Bias: Historical evaluation introduces retrospective knowledge
- Single-Pass Evaluation: No ensemble aggregation or repeated trials
- No Human Benchmark: Expert investor performance not measured

## Future Research Directions

- Expand dataset to 100+ pitch decks
- Implement ensemble evaluation with repeated trials
- Benchmark against expert venture capitalists
- Test alternative LLM architectures (GPT-4, Claude Opus, Llama)
- Develop adaptive rubric weighting via reinforcement learning
- Incorporate multimodal analysis (slide layouts, images, charts)
- Conduct ablation studies on knowledge stack components
- Explore cross-domain applications (grants, R&D proposals, acquisitions)

## Citation

If you use this dataset, methodology, or findings in your research, please cite:

Velarde, D., & Gillespie, S. (2025). Structured Reasoning Frameworks for LLM-Based Venture Capital Evaluation: Integrating Systems Engineering and Business Analysis. United States Military Academy, West Point, NY.

## Authors

Dan Velarde  
United States Military Academy  
West Point, New York, USA  
Email: dan.velarde@westpoint.edu

Stephen Gillespie  
United States Military Academy  
West Point, New York, USA  
Email: stephen.gillespie@westpoint.edu

## Acknowledgments

The authors acknowledge the use of:
- Claude Sonnet 4.5 (Anthropic, 2025) for data analysis, section development, and manuscript preparation
- ChatGPT (OpenAI, 2025) for figure generation and visualization support
- Gemini 2.5 Pro Preview (Google, 2024) as the evaluation model for all persona configurations

## License

This research is released for academic and educational use. For commercial applications or derivative works, please contact the authors.

## Keywords

Large language models, venture capital, systems engineering, artificial intelligence, decision support systems, startup evaluation, structured reasoning, pitch deck analysis, risk assessment, LLM evaluation frameworks

---

Repository Status: Complete dataset and materials for published research  
Last Updated: November 2025
