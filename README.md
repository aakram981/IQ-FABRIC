# Microsoft Fabric IQ: Ontology on a Hospital Lakehouse

A hands-on project that turns raw Lakehouse tables into a business **ontology** in Microsoft Fabric IQ.

![IQ - Fabric - Analogy](images/iq-fabric-analogy.png)

## Concept: the factory analogy

| Layer | Analogy | In this project |
|---|---|---|
| Lakehouse | Factory floor with raw materials | Tables loaded into `Lakjouse_IQ` |
| Ontology | Map of how everything relates | Entity types + relationships in `Ontology_1` |
| Analogy | Explaining the unfamiliar with the familiar | Making the model easy to share with business users and AI agents |

## Architecture

```
Lakehouse (Lakjouse_IQ)  ->  Ontology (Ontology_1)  ->  Agents / analytics
   dbo tables                 entities + relationships
```

## Step 1: Data in the Lakehouse

The source data lives in the `dbo` schema of the Lakehouse:

- `hospitals`
- `departments`
- `rooms`
- `patients`
- `vitalsignequipment`

![Lakehouse tables](images/lakehouse-tables.png)

## Step 2: Ontology in Fabric IQ

Entity types defined in `Ontology_1`:

- Hospital
- Department
- Room
- Patient
- VitalSignEquipment

The graph shows 5 entities and 4 relationships:
`VitalSignEquipment -> Patient -> Room -> Department`.

![Ontology graph](images/ontology-graph.png)

## Key learnings

- Start from clean Lakehouse tables: the ontology is only as good as its source data.
- Define entities first, then relationships.
- Think in business concepts ("a patient is in a room"), not in joins.
- A well-defined model lets an AI agent reason over the data instead of guessing.

## Tools

Microsoft Fabric, Fabric IQ (Ontology), Lakehouse, SQL analytics endpoint

## Author

Akram Brahem - Data Analyst (PL-300)

#MicrosoftFabric #FabricIQ #Ontology #Lakehouse
