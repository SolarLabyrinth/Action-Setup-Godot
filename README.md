# Setup Godot Action

A GitHub Action to install Godot on a GitHub Actions a runner.

## Usage

This action will download export templates and provide access to the godot binary on your runner's path. You can then reference that binary in other workflow steps.

```yml
- name: Setup Godot
  uses: SolarLabyrinth/Action-Setup-Godot@v1
  with:
    version: 4.4-stable

- name: Build Game
  run: |
    mkdir -p ./build
    godot --headless --export-debug "Linux" ./build/game.exe
```
