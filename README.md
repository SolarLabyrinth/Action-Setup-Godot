# Action: Setup Godot

A GitHub Action to install Godot 4 on a GitHub Actions runner.

> Note: Only supported on Ubuntu runners with Godot 4+.

## Usage

This action will download export templates and provide access to the godot binary on your runner's path. You can then reference that binary in other workflow steps.

```yml
- name: Setup Godot
  uses: solarlabyrinth/action-setup-godot@v2
  with:
    version: 4.4.1-stable

- name: Build Game
  run: |
    mkdir -p ./build
    godot --headless --export-debug "Windows" ./build/game.exe
```

### Variables

```yml
- name: Setup Godot
  uses: solarlabyrinth/action-setup-godot@v2
  with:
    version: 4.4.1-stable
    # Optional. Defaults to false
    csharp: false
    # Optional. Defaults to "godot"
    name: godot
```

### Supported Versions

This action is tested by exporting a small Godot project to the following target platforms.

| Version      | Windows | Linux | Mac | Windows - C# | Linux - C# | Mac - C# |
| ------------ | ------- | ----- | --- | ------------ | ---------- | -------- |
| 4.5-beta1    | ✅      | ✅    | ✅  | ✅           | ✅         | ✅       |
| 4.4.1-stable | ✅      | ✅    | ✅  | ✅           | ✅         | ✅       |
| 4.3-stable   | ✅      | ✅    | ✅  | ✅           | ✅         | ✅       |
| 4.2.2-stable | ✅      | ✅    | ✅  | ✅           | ✅         | ✅       |
| 4.1.4-stable | ✅      | ✅    | ✅  | ✅           | ✅         | ✅       |
| 4.0.4-stable | ✅      | ✅    | ✅  | ✅           | ✅         | ✅       |
