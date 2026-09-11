# ShellCore

This repository contains a collection of sample Bash scripts for learning and practicing shell scripting.

## Prerequisites

- **Operating System:** Linux, macOS, or Windows (with WSL or Git Bash)
- **Bash:** Version 3.0 or higher recommended
- **Git:** For cloning the repository

## How to Run Scripts

1. **Make the script executable:**
```bash
chmod +x src/scripts/sample-script.sh
```

2. **Execute the script:**
```bash
./src/scripts/sample-script.sh
```

Alternatively, you can run:
```bash
bash src/scripts/sample-script.sh
```

## Run pre-commit
The pre-commit framework is a powerful, language-agnostic tool for managing Git hooks. Create a .pre-commit-config.yaml file in the root of your repository. Run the below commnad from the git repo root to set up the git hook scripts into your git hooks. It will be installed at .git/hooks/pre-commit

```bash
pre-commit install
pre-commit install --config <file> # If config file has non-standard name
pre-commit validate-config # Validate .pre-commit-config.yaml files
```

now pre-commit will run automatically on git commit. Usually, it runs only for the changed files. Its good to run the hooks against all the files when adding new hooks. To manually run all pre-commit hooks on a repo, use below -

```bash
# to run hooks on all files
pre-commit run --all-files

# to run hooks on all files using a non-standard naming config file
pre-commit run --all-files --config .pre-commit-config-old.yaml

# to run individual hook
pre-commit run <hook_id>
```

Once you have pre-commit installed, adding pre-commit plugins to your project is done with the .pre-commit-config.yaml configuration file. You can generate a very basic configuration using `pre-commit sample-config`. Every time you clone a project using pre-commit running pre-commit install should always be the first thing you do.

## Contributing

Contributions are welcome! Please open issues or submit pull requests for improvements or new scripts.

## License

This project is licensed under the [MIT License](LICENSE).
