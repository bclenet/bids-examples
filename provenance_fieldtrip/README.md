# Provenance of MEG analysis with Fieldtrip and reproducescript

This example aims at showing provenance metadata for a MEG analysis performed with [`Fieldtrip`](https://www.fieldtriptoolbox.org/) and [`reproducescript`](https://github.com/matsvanes/reproducescript). Provenance metadata was created manually ; it acts as a guideline for further machine-generated provenance by `Fieldtrip` with `reproducescript`. 

## Original dataset

This example is based on Fieltrip's tutorial [Using reproducescript for a group analysis](https://www.fieldtriptoolbox.org/example/other/reproducescript_group/). Datasets, code and workflow originate from this tutorial.

The tutorial itself is based on the manuscript [Reducing the efforts to create reproducible analysis code with FieldTrip](http://dx.doi.org/10.21105/joss.05566).

## Directory tree

The directory tree is as follows.

> [!NOTE]
> Note that the `docs/` directory contains explanatory data (see [Provenance as RDF graphs](#provenance-as-rdf-graphs)) that is not required to encode provenance.

```
.
├── dataset_description.json
├── docs
│   ├── prov-group.jsonld
│   ├── prov-group.png
│   ├── prov-overview.jsonld
│   ├── prov-overview.png
│   ├── prov-scripts.jsonld
│   ├── prov-scripts.png
│   ├── prov-subject01.jsonld
│   └── prov-subject01.png
├── prov
│   ├── provenance.tsv
│   ├── prov-group_act.json
│   ├── prov-group_io.json
│   ├── prov-group_soft.json
│   ├── prov-overview_act.json
│   ├── prov-overview_io.json
│   ├── prov-overview_soft.json
│   ├── prov-scripts_act.json
│   ├── prov-scripts_io.json
│   ├── prov-scripts_soft.json
│   ├── prov-subject01_act.json
│   ├── prov-subject01_io.json
│   └── prov-subject01_soft.json
└── README.md
```

## Provenance as RDF graphs

Provenance metadata can be aggregated as JSON-LD RDF graphs, which are available in [`docs/`](docs/) alongside with rendered versions of the graphs in PNG.

## Several levels of granularity

Provenance in this dataset comes at several levels of granularity. Indeed, the same workflow is described from broad (dataset level, one command) to detailed (file level, each function of the script is an activity) content. Find more information in the [`prov/provenance.tsv`](prov/provenance.tsv) file that provides correspondance between the `prov-<label>` entities and their meaning.

Hereafter are the rendered version of these descriptions from the broadest to the more detailed.

### `prov-overview`	: Provenance overview at dataset level of subject+group analyses with reproducescript

![Rendered version of the RDF graph for entity prov-overview](docs/prov-overview.png)

### `prov-scripts` : Provenance scripts overview at dataset level of subject+group analyses with reproducescript

![Rendered version of the RDF graph for entity prov-scripts](docs/prov-scripts.png)

### `prov-subject01` and `prov-group` : Provenance of single-subject analysis for Subject01 (resp. group analysis) with reproducescript

Subject01 analysis:
![Rendered version of the RDF graph for entity prov-subject01](docs/prov-subject01.png)

Group analysis:
![Rendered version of the RDF graph for entity prov-group](docs/prov-group.png)
