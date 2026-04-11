# cuda-pipeline

Data pipeline — ETL stages, map/filter/reduce transforms, stream processing (Rust)

Part of the Cocapn workflow layer — task orchestration and pipeline execution.

## What It Does

### Key Types

- `DataItem` — core data structure
- `MapStage<F: Fn(DataItem) -> DataItem>` — core data structure
- `FilterStage<F: Fn(&DataItem) -> bool>` — core data structure
- `FlatMapStage<F: Fn(DataItem) -> Vec<DataItem>>` — core data structure
- `PipelineStats` — core data structure
- `Pipeline` — core data structure

## Quick Start

```bash
# Clone
git clone https://github.com/Lucineer/cuda-pipeline.git
cd cuda-pipeline

# Build
cargo build

# Run tests
cargo test
```

## Usage

```rust
use cuda_pipeline::*;

// See src/lib.rs for full API
// 9 unit tests included
```

### Available Implementations

- `DataItem` — see source for methods
- `PipelineStats` — see source for methods
- `Pipeline` — see source for methods

## Testing

```bash
cargo test
```

9 unit tests covering core functionality.

## Architecture

This crate is part of the **Cocapn Fleet** — a git-native multi-agent ecosystem.

- **Category**: workflow
- **Language**: Rust
- **Dependencies**: See `Cargo.toml`
- **Status**: Active development

## Related Crates

- [cuda-workflow](https://github.com/Lucineer/cuda-workflow)
- [cuda-orchestrator](https://github.com/Lucineer/cuda-orchestrator)
- [cuda-scheduler](https://github.com/Lucineer/cuda-scheduler)
- [cuda-taskq](https://github.com/Lucineer/cuda-taskq)

## Fleet Position

```
Casey (Captain)
├── JetsonClaw1 (Lucineer realm — hardware, low-level systems, fleet infrastructure)
├── Oracle1 (SuperInstance — lighthouse, architecture, consensus)
└── Babel (SuperInstance — multilingual scout)
```

## Contributing

This is a fleet vessel component. Fork it, improve it, push a bottle to `message-in-a-bottle/for-jetsonclaw1/`.

## License

MIT

---

*Built by JetsonClaw1 — part of the Cocapn fleet*
*See [cocapn-fleet-readme](https://github.com/Lucineer/cocapn-fleet-readme) for the full fleet roadmap*
