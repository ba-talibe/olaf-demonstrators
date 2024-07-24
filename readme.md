# olaf-demonstators


# Installation

```bash
git clone https://github.com/wikit-ai/olaf-llm-eswc2024
cd olaf-llm-eswc2024
python3 -m venv ./venv
source venv/bin/activate
pip install -r requirements.txt
```path/to/your/local/obo/robot/cli/tool/folder/robot.jar
```

# Data

The text used to learn the ontology is created based on default documentation for the manufacture of metal plates. 


# Notebooks
In this folowing notebooks concepts, relations, metarelation components 
are assessed on the basis of a hand-created ground truth (GC10-DET_doc_annotated).
- concept_extraction_evaluation.ipynb 
- relation_extraction_evaluation.ipynb 
- metarelation_extraction_evaluation.ipynb 
- axiom_extraction_evaluation.ipynb 

# Results

Built ontology are stored in `results` in turtle format.
