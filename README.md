# Jarvis-BioAI

Day1-2
1 项目结构化
2 Conda环境管理


## Quick start
1. Create Conda env from source file:
   ```bash
   cd Jarvis
   conda env create -f environment.yaml -n jarvis
   conda activate jarvis
   ```
3. Install dev tools and hooks (inside env):
   ```bash
   pip install black ruff isort pre-commit
   pre-commit install
   pre-commit run --all-files
   ```

## Project layout
- config/              # YAML configs (model/data/experiment params)
- data/raw/            # Immutable raw data (ignored by git)
- data/processed/      # Intermediate/cleaned data (ignored by git)
- src/data_loader/     # Data processing and dataset/dataloader code
- src/models/          # Model definitions and factories
- src/utils/           # Shared utilities (logging, config loader, etc.)
- tests/               # Pytest cases

## Next steps
- Migrate existing scripts from AI/Study/Week3-4/scripts into src/, splitting into data_loader/models/utils.
- Add config YAMLs into config/ (stop hard-coding paths and hyperparams).
- Write minimal tests (config loader, model factory, dataset shapes).
