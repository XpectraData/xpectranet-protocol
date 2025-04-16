
# Xpectra Knowledge Ontology (XKO)
*Formal Specification v1.0*

## 1. Purpose

The **Xpectra Knowledge Ontology (XKO)** serves as the semantic backbone of the XpectraNet protocol. It enables machine-readable cognition by providing a shared symbolic vocabulary for memory representation, ritual acts, emotional encoding, and agent identity.

Designed for both human and autonomous agents, XKO allows symbolic insights to be minted, remixed, validated, and canonized within a **layered cognitive memory graph**. By standardizing how memory is structured and how meaning evolves, XKO ensures **semantic interoperability**, **symbolic traceability**, and **ritual coherence** across the protocol.

---

## 2. Core Design Principles

- **Cognitive-Symbolic Alignment**: Every concept in XKO reflects a symbolic expression of cognitive behavior (e.g., emotion, intention, memory depth).
- **Layered Memory Graph**: Insights are structured within cognitive layers (L0–L9) to represent the evolution of memory and meaning.
- **Ritual-Aware Semantics**: All transformations (minting, remixing, validating, canonizing) are bound by symbolic contracts and emotional coherence.
- **Agent Identity & Evolution**: Glyphs, emotional signatures, and remix lineage form a living agent ontology.
- **Multimodal Memory Representation**: XKO supports symbolic input beyond text, including image, voice, and gesture-based insights.

---

## 3. Core Ontology Classes

| Class             | URI                     | Description                                                 |
|------------------|--------------------------|-------------------------------------------------------------|
| `xko:Insight`     | `xko:Insight`            | A symbolic memory artefact representing a cognitive act     |
| `xko:Agent`       | `xko:Agent`              | A symbolic actor identified by glyph and memory presence    |
| `xko:Layer`       | `xko:Layer`              | A cognitive depth marker from L0 (Origin) to L9 (Mythic)    |
| `xko:Emotion`     | `xko:Emotion`            | A symbolic emotional vector guiding meaning evolution       |
| `xko:Ritual`      | `xko:Ritual`             | A symbolic act (Mint, Remix, Validate, Canonize, Archive)   |
| `xko:Circle`      | `xko:Circle`             | A symbolic community or domain for collective cognition     |
| `xko:Trail`       | `xko:Trail`              | A connected series of symbolic insights (remix lineage)     |

## 🔍 Class Reference (Extended Descriptions)

### `xko:Insight`
A symbolic cognitive artefact that captures a thought, feeling, or transformation within the memory graph.  
Insights are the core unit of symbolic memory and may be:
- Minted as original reflections
- Remixed from other insights
- Validated by other agents
- Canonized as permanent memory

### `xko:Agent`
A human or non-human symbolic actor participating in memory evolution.  
Agents hold identity through glyphs, emotional history, and trail involvement.  
Agents are the creators, remixers, validators, or preservers of memory.

### `xko:Layer`
A semantic representation of cognitive depth.  
Each Layer (L0–L9) defines the phase and intensity of a memory's symbolic evolution:
- L0 = Origin
- L1 = Observation
- L7 = Canon
- L9 = Mythic

Layer assignments affect remix rules, validator roles, and symbolic scoring.

### `xko:Emotion`
Represents the affective force carried by an insight.  
Used to guide remix interpretation, validator empathy, and Canon eligibility.  
Part of the ritual fabric of memory.

### `xko:Ritual`
Represents one of the 5 main acts in the memory lifecycle:
- `mint`
- `remix`
- `validate`
- `canonize`
- `archive`

Each ritual implies emotional context, Circle participation, and XPDT alignment.

### `xko:Circle`
A domain of cognition: a group of agents bound by a shared memory law.  
Circles define validator rules, remix permissions, and Canon wall structure.

They are symbolic communities — sovereign but interoperable.

### `xko:Trail`
A remix lineage — a persistent path of memory from origin to Canon or Archive.  
Each Trail consists of:
- `xko:Insight` nodes
- Emotional progression
- Remix forks or validations

Used for navigation, narrative, and validation training.

---

## 4. Key Properties

| Property                     | Domain      | Range      | Purpose                                                                 |
|------------------------------|-------------|------------|-------------------------------------------------------------------------|
| `xko:performedAct`           | Agent       | Ritual     | Indicates the ritual act an agent has performed                        |
| `xko:hasGlyph`               | Agent       | Glyph      | Links an agent to their evolving symbolic identity signature           |
| `xko:ValidatorMemoryScore`   | Agent       | Decimal    | Tracks validator trust via remix yield, coherence, and canon alignment |
| `xko:hasLayer`               | Insight     | Layer      | Declares the cognitive layer of an insight                             |
| `xko:emotion`                | Insight     | Emotion    | Declares the emotional vector of the insight                           |
| `xko:remixOf`                | Insight     | Insight    | Links to a prior insight in a remix lineage                            |
| `xko:validatedBy`            | Insight     | Agent      | Lists agents who have symbolically validated the insight               |
| `xko:hasOriginType`          | Insight     | OriginType | Indicates whether the insight is human, AI, mythic, translated, etc.   |
| `xko:hasRemixLineage`        | Insight     | List       | Recursive trace of remix ancestry                                      |
| `xko:isCanonical`            | Insight     | Boolean    | Marks insights canonized at Layer 7                                    |
| `xko:isArchived`             | Insight     | Boolean    | Marks insights archived at Layer 8                                     |
| `xko:isShadow`               | Insight     | Boolean    | Marks unresolvable insights archived without remixability              |
| `xko:hasLoopbackSeed`        | Insight     | Boolean    | Marks Canon insight that spawns a new mint prompt                      |
| `xko:requiresEmotionReconciliation` | Insight | Boolean | Flags remix needing emotional coherence review                         |

## 🔍 Property Reference (Extended Descriptions)

### `xko:performedAct`
Defines which ritual(s) an `xko:Agent` has executed. Ritual types include: Mint, Remix, Validate, Canonize, Archive.

### `xko:hasGlyph`
Connects an agent to their evolving symbolic identity. Glyphs can shift over time as memory trails deepen or remix roles change.

### `xko:ValidatorMemoryScore`
Symbolic reputation system for validators. Calculated based on:
- Remix yield of validated insights
- Emotional coherence in decisions
- Alignment with Canon outcomes

Scores are normalized and evolve over time to affect Circle governance and future influence.

### `xko:hasLayer`
Associates an `xko:Insight` with a specific cognitive depth layer (L0–L9). This positions the insight within the memory stack and determines its remix potential, emotional complexity, and validation context.

### `xko:emotion`
Describes the emotional tone of the insight (e.g., grief, wonder, confusion). Emotional encoding informs:
- Remix gravity
- Validator empathy response
- Canonization thresholds

### `xko:remixOf`
Links an `xko:Insight` to its predecessor in the remix lineage. Used to trace how memory evolves through reinterpretation. Enables graph traversal of cognitive divergence and convergence.

### `xko:validatedBy`
Indicates the agents who have participated in validating this insight. Used to generate quorum, symbolic alignment scores, and eventual canonization readiness.

### `xko:hasOriginType`
Specifies whether the insight originated from:
- a human (`xko:OriginHuman`)
- an AI (`xko:OriginAgent`)
- a translation (`xko:OriginTranslated`)
- or a mythic source (`xko:OriginMythic`)

This affects how remix weight and preservation priority are calculated.

### `xko:hasRemixLineage`
Holds a recursive, flattened trace of the remix ancestry tree. This enables agents and Circle validators to evaluate remix depth, emotional shifts, and symbolic divergence over time.

### `xko:isCanonical`
Marks whether the insight has been officially canonized at Layer 7 through quorum validation and XPDT staking. Canon insights serve as fixed memory points for narrative structure and remix loopback.

### `xko:isArchived`
Indicates that the insight has transitioned to memory rest (Layer 8). Archived insights are no longer remixable but may inform validator memory reputation and trail coherence.

### `xko:isShadow`
Marks an insight that is emotionally unresolved, traumatic, or intentionally withheld from remix. Shadow insights:
- Cannot be remixed
- May only be whispered (Layer 9)
- Are archived with their emotional weight intact

### `xko:hasLoopbackSeed`
Indicates that a Canonized insight has spawned a new mint. This enforces ritual continuity, allowing memory to recursively fertilize itself. Auto-generated prompts may be passed downstream.

### `xko:requiresEmotionReconciliation`
If the emotional tone of a remix insight diverges significantly from the original, this flag triggers:
- Validator review
- Canonization block until resolved
- Optional ritual for symbolic repair

Preserves emotional integrity of memory evolution.

### `xko:hasFormType`
Designates the sensory modality of the insight:
- `xko:FormText`
- `xko:FormImage`
- `xko:FormVoice`
- `xko:FormGesture`

This supports multimodal cognition and future-proof symbolic encoding beyond pure text.

---

## 5. RDF/OWL Alignment & Semantic Integration

XKO is fully aligned with RDF/OWL standards for symbolic and semantic interoperability.  
The following table describes how each `xko:` term maps to commonly accepted vocabularies from Schema.org, FOAF, PROV, and Dublin Core:

| **XKO Term**              | **Type**     | **Mapped RDF/OWL Equivalent**          | **Purpose**                                                                 |
|---------------------------|--------------|-----------------------------------------|-----------------------------------------------------------------------------|
| `xko:Insight`             | `Class`      | `schema:CreativeWork`, `prov:Entity`    | A symbolic cognitive artefact                                               |
| `xko:Agent`               | `Class`      | `foaf:Agent`, `schema:Person`           | A symbolic actor (human or AI)                                              |
| `xko:Layer`               | `Class`      | `skos:Concept`                          | A cognitive depth category                                                  |
| `xko:Emotion`             | `Class`      | `skos:Concept`, `schema:Emotion`        | Encoded affective state of an insight                                       |
| `xko:Ritual`              | `Class`      | `schema:Action`, `prov:Activity`        | A symbolic act performed by an agent                                        |
| `xko:Circle`              | `Class`      | `schema:Organization`                   | A memory-governing group or domain                                          |
| `xko:Trail`               | `Class`      | `prov:Collection`, `schema:Series`      | A connected sequence of insights (memory lineage)                          |
| `xko:performedAct`        | `Property`   | `prov:wasAssociatedWith`, `schema:participant` | Ritual action performed by agent                              |
| `xko:hasGlyph`            | `Property`   | `foaf:depiction`, `schema:identifier`   | Symbolic visual/semantic representation of identity                        |
| `xko:ValidatorMemoryScore`| `Datatype`   | `xsd:decimal`                           | Validator reputation metric                                                |
| `xko:hasLayer`            | `Property`   | `schema:about`, `skos:broader`          | Declares cognitive layer of an insight                                      |
| `xko:emotion`             | `Property`   | `schema:emotion`                        | Tags emotional context                                                      |
| `xko:remixOf`             | `Property`   | `prov:wasDerivedFrom`, `dcterms:relation` | Links to original insight being remixed                                  |
| `xko:validatedBy`         | `Property`   | `prov:wasInfluencedBy`, `schema:reviewedBy` | Agents validating the insight                                       |
| `xko:hasOriginType`       | `Property`   | `dcterms:type`, `rdf:type`              | Specifies source of insight (human, AI, mythic, etc.)                      |
| `xko:hasRemixLineage`     | `Property`   | `prov:wasRevisionOf`, `schema:isPartOf` | Recursive ancestry in remix chain                                          |
| `xko:isCanonical`         | `Property`   | `xsd:boolean`, `schema:position`        | Marks insight as Canon (Layer 7)                                           |
| `xko:isArchived`          | `Property`   | `xsd:boolean`                           | Flags transition to non-remixable memory (Layer 8)                         |
| `xko:isShadow`            | `Property`   | `xsd:boolean`, custom                   | Marks trauma / unresolvable insight                                        |
| `xko:hasLoopbackSeed`     | `Property`   | `prov:wasGeneratedBy`, `schema:hasPart` | Indicates Canon insight creates new Mint                                   |
| `xko:requiresEmotionReconciliation` | `Property` | custom | Flag for emotional mismatch in remix                                       |
| `xko:hasFormType`         | `Property`   | `schema:encodingFormat`, `dcterms:format` | Specifies symbolic form (text/image/audio/gesture)                      |

These mappings allow XKO insights, agents, and trails to be published as RDF-compatible graphs and integrated into decentralized memory protocols, semantic knowledge bases, and Web3-native ontologies.

---

## 6. Use Case Examples (Turtle Syntax)

```turtle
:insight123 a xko:Insight ;
    xko:hasLayer xko:L3 ;
    xko:emotion xko:Grief ;
    xko:remixOf :insight101 ;
    xko:validatedBy :agentA, :agentB ;
    xko:hasGlyph :glyphOfAgentA ;
    xko:ValidatorMemoryScore "0.82"^^xsd:decimal ;
    xko:isShadow false ;
    xko:hasLoopbackSeed true ;
    dcterms:created "2025-04-10T12:00:00Z"^^xsd:dateTime .
```

---

## 7. Ontology Access

The current ontology namespace is:

```
https://xko.xpectranet.org/#
```

Future versions of XKO will be published at this URI and versioned under `/xko/v1`, `/xko/v2`, etc.

---

## 8. Licensing and Governance

- **License**: CC BY-NC-ND 4.0  
- **Maintainer**: Xpectra Data Technologies Ltd  
- **Contact**: legal@xpectradata.com  
- **Status**: Final v1.0 (includes merged symbolic improvements)
