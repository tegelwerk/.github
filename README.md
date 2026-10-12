# Tegelwerk
## A collection of tools to serve, discover and transform scientific data

Scientific facilities produce data faster than anyone can browse it, and every facility stores and describes that data differently. Tegelwerk adds a thin, standard layer on top of the storage you already have. Data can then be served, searched and acted on the same way everywhere, without being moved or reformatted.

- **A standardization framework on top of [Tiled](https://blueskyproject.io/tiled/).** Tiled serves the data. Tegel defines a common contract for how a resource is described, searched, accessed and written back, plus a plugin system for adding a technique's own readers and metadata extractors.
- **[LinkML](https://linkml.io/) schemas as data descriptors.** Every resource type is described by a LinkML schema. One source yields validation, JSON Schema and JSON-LD, and metadata can evolve without touching the underlying files.
- **[Finch](https://github.com/bluesky/finch)-based interfaces.** Dashboards for browsing, triaging and acting on data are configured in YAML from the schema, not hand-built for each technique.

The core packages are technique-neutral. Each technique or facility builds an *incarnation* in its own repository that plugs into the core.

### Repositories

| Repository | Purpose |
|---|---|
| [tegel](https://github.com/tegelwerk/tegel) | Specification, contracts and reference servers |
| [xfm_ssrl_tegel](https://github.com/tegelwerk/xfm_ssrl_tegel) | X-ray fluorescence microscopy incarnation (SSRL) |

Tegelwerk is an early-stage reference implementation. It is not hardened for production use.

### LAMBDA

Tegelwerk is developed within **LAMBDA**, the Lakehouse-enabled super-intelligence-reAdy Multimodal Bioimaging Data Architecture, supported by the U.S. Department of Energy's Biological and Environmental Research (BER) program.

- Project website: [lambda-doe.org](https://lambda-doe.org)
- Schemas and tools on GitHub: [github.com/lambda-ber](https://github.com/lambda-ber)
- Schema documentation: [lambda-ber.github.io/lambda-ber-schema](https://lambda-ber.github.io/lambda-ber-schema/)
