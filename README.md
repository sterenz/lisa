# LISA Ontology

**LISA Ontology** (Linked Interpretative Semantic Annotations) is a custom, streamlined ontology designed to model annotation versioning and iconographical recognitions within the Mirador annotation tool. Building upon the **Multi-Level Annotation Ontology (MLAO)** framework, LISA integrates elements from the **ICON Ontology** to enhance the semantic representation and management of annotations.

## Key Features

- **Foundation on MLAO:** Extends the Multi-Level Annotation Ontology to support hierarchical and multi-tiered annotations, facilitating complex annotation structures.
- **Integration with ICON:** Utilizes ICON for modeling iconographical recognitions, enriching the semantic depth and interpretative capabilities of annotations.
- **Annotation Versioning:** Provides a structured approach to version control, managing transitions between different annotation states such as Draft, Published, and Deprecated.
- **Provenance Support:** Incorporates provenance properties to trace the origin, attribution, and modifications of annotations, ensuring transparency and accountability.

## Purpose

The LISA Ontology serves as a foundational component for projects requiring robust and semantically rich annotation management. By combining the hierarchical strengths of MLAO with the recognition capabilities of ICON, LISA facilitates more structured, interoperable, and meaningful annotation workflows within digital humanities and related fields.


```ttl
# Example Instances

## Instance: Draft Stage
lisa:Draft a lisa:PublishingStage ;
    rdfs:label "Draft Stage" ;
    rdfs:comment "Initial stage where annotations are being created and not yet published." ;
    prov:wasAttributedTo [
        a foaf:Person ;
        foaf:name "J. Doe"
    ] ;
    prov:generatedAtTime "2025-01-23T10:00:00Z"^^xsd:dateTime .

## Instance: Published Stage
lisa:Published a lisa:PublishingStage ;
    rdfs:label "Published Stage" ;
    rdfs:comment "Stage where annotations are published and publicly accessible." ;
    prov:wasAttributedTo [
        a foaf:Person ;
        foaf:name "J. Doe"
    ] ;
    prov:generatedAtTime "2025-02-01T12:00:00Z"^^xsd:dateTime .

## Instance: Deprecated Stage
lisa:Deprecated a lisa:PublishingStage ;
    rdfs:label "Deprecated Stage" ;
    rdfs:comment "Stage indicating that annotations are deprecated and no longer valid." ;
    prov:wasAttributedTo [
        a foaf:Person ;
        foaf:name "J. Doe"
    ] ;
    prov:generatedAtTime "2025-03-15T09:30:00Z"^^xsd:dateTime .
```
