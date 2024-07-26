# defect_onto_ground_truth.ttl 
This is a ground-truth ontology built manualy.

# defect_onto_kr_ttl_graph.ttl 
We used same axiomation functions as olaf-llm-eswc2024.
The hierarchisation is not satisfactory.

- kr_concepts_to_owl_classes
- kr_relations_to_owl_obj_props
- kr_metarelations_to_owl
- kr_relations_to_anonymous_some_parent
- concept_lrs_to_owl_individuals

# defect_onto_kr_ttl_graph_cheat.ttl
In this pipeline we add our five unmissable super classes that might not appear in the corpus for a better axiomatisation.
Thanks to that, we made a better hierarchisation of classes.

- kr_concepts_to_owl_classes,
- kr_relations_to_owl_obj_props,
- kr_metarelations_to_owl,
- kr_relations_to_anonymous_some_parent,
- concept_lrs_to_owl_individuals

# defect_onto_kr_ttl_graph_cheat_v2.ttl
This pipeline is a improved version of the previous one. We have refined the metarelation extraction by adding context to the LLM prompt. But according to the `defect_onto_ground_truth.ttl`, we missed Domain and range definition for each relation.

- kr_concepts_to_owl_classes,
- kr_relations_to_owl_obj_props,
- kr_metarelations_to_owl,
- kr_relations_to_anonymous_some_parent,
- concept_lrs_to_owl_individuals

# defect_onto_kr_ttl_graph_cheat_equi.ttl
In this pipeline, we specified domain and range for each relation, and equivalence between relations during axiomatisation.
But The relation equivalence associated with a no generalised domain and range specification suggest that all subclasses of a class are not distinct. Which not compatible with our ground truth.

- kr_relations_to_owl_obj_props
- kr_metarelations_to_owl
- kr_relations_to_domain_range_obj_props
- kr_relations_to_anonymous_some_equivalent
- concept_lrs_to_owl_individuals

# defect_onto_kr_ttl_graph_equi_dis.ttl
This pipeline is a improved version of the previous one. In contrast, we maked all classes distinct during axiomatisation.
This approach raise inconsistency ontology error during reasoning.Because the equivalence between relation and the classes distinction created conflicts.

- kr_relations_to_owl_obj_props
- kr_metarelations_to_owl
- kr_relations_to_domain_range_obj_props
- kr_relations_to_anonymous_some_equivalent
- all_classes_distinct

# final_defect_onto_kr_ttl_graph.ttl
This is the optimal version we choose.During axiomatisation, we only made all subclasses distinct without making equivalence between relations to avoid inconsistency ontology.We removed domains and ranges specification because it can be done correctly and automatically.

- kr_concepts_to_owl_classes
- kr_relations_to_owl_obj_props
- kr_metarelations_to_owl
- kr_relations_to_anonymous_some_parent
- concept_lrs_to_owl_individuals
- all_sub_classes_distinct