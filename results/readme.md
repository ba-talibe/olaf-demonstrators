# defect_onto_kr_ttl_graph.ttl 
We used same axiomation functions as olaf-llm-eswc2024
    - kr_concepts_to_owl_classes
    - kr_relations_to_owl_obj_props
    - kr_metarelations_to_owl
    - kr_relations_to_anonymous_some_parent
    - concept_lrs_to_owl_individuals

# defect_onto_kr_ttl_graph_cheat.ttl
In this pipeline we add our five unmissable super classes that might not appear in the corpus for a better axiomatisation.

- kr_concepts_to_owl_classes,
- kr_relations_to_owl_obj_props,
- kr_metarelations_to_owl,
- kr_relations_to_anonymous_some_parent,
- concept_lrs_to_owl_individuals

# defect_onto_kr_ttl_graph_cheat_v2.ttl
This pipeline is a improved version of the previous one. We have refined the metarelation extraction by adding context to the llm prompt.

- kr_concepts_to_owl_classes,
- kr_relations_to_owl_obj_props,
- kr_metarelations_to_owl,
- kr_relations_to_anonymous_some_parent,
- concept_lrs_to_owl_individuals

# defect_onto_kr_ttl_graph_cheat_equi.ttl
In this pipeline, we added domain and range to classes during axiomatisation.

- kr_relations_to_owl_obj_props
- kr_metarelations_to_owl
- kr_relations_to_domain_range_obj_props
- kr_relations_to_anonymous_some_equivalent
- concept_lrs_to_owl_individuals

# defect_onto_graph_distinct_classes.ttl
This pipeline is a improved version of the previous one. In contrast, we maked all classes distinct during axiomatisation.

- kr_relations_to_owl_obj_props
- kr_metarelations_to_owl
- kr_relations_to_domain_range_obj_props
- kr_relations_to_anonymous_some_equivalent
- all_classes_distinct

