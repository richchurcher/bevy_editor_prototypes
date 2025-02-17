# Roadmap

Making an editor is a huge project! How do we even know where to begin?

Like usual, we're starting by building something small. While we won't be adopting any of the existing prototypes directly to avoid drowning in a new sprawling code-base, please look to them aggressively for inspiration on both features and implementations.

The stages contained below are a flexible, coarse resolution roadmap to give newcomers and onlookers a sense of the overall plan and progress.
If you'd like to add items to this roadmap, open a PR and ping `@alice-i-cecile` as needed for dispute resolution.
Try to keep each stage small, simple, and easily accomplished.
We can easily add more stages, but trying to jump ahead to a complex feature risks killing all momentum.
For actionable, well-scoped items, please open issues instead.

As you complete tasks, check them off here!
The tasks don't need to be done *well* to be considered completed here: the Bevy community is very good at cleaning up loose strings as we work.

Feel free to tackle any listed item in any order: foundations and primitives can often be built out well before the features that need them are in place.
This list is not "all of the features that the editor will have": other stages will follow as these features are added.
It's best not to plan too far in advance!

## Stage 0: Hello Project

- [x] make a repo
- [x] add a README
- [x] add a CONTRIBUTING.md
- [x] add a basic Bevy project
- [x] define the broad plan for what we're doing
- [x] define basic constraints for how we're building the editor
- [x] define a shared vision for what the editor is (and is not)

## Stage 1: Standalone Scene Editor

- [ ] undo-redo abstraction
- [ ] can load scenes from disk using a native file picking widget
- [ ] can display scenes in a viewer
  - [ ] 2D
  - [ ] 3D
- [ ] simple camera controller
  - [ ] 2D
  - [ ] 3D
- [ ] gizmos can be toggled
  - [ ] UI outlines
  - [ ] lights
  - [ ] AABBs
- [ ] the list of entities and their components is shown in the inspector
  - [ ] supports hierarchy via a folding tree view
- [ ] existing component values can be modified using a graphical interface
- [ ] resources can be inspected, showing their values and allowing modification
- [ ] loaded assets can be inspected, providing basic information about them
- [ ] scenes can be saved back to disk

## Stage 2: Editor-Game Interaction

- [ ] provide the editor with access to the game's code, allowing it to correctly initialize objects
  - [ ] game-specific rendering techniques display correctly in the editor's scene editing
- [ ] users can press a button in the editor, launching the game from the very beginning
- [ ] users can press a button in the editor, and their game will run, loading the currently active scene
- [ ] asset hotreloading, allowing changes in the asset file to be reflected in the editor and game views
- [ ] components that reference assets can be changed to load a new asset via a file dialog
- [ ] components can be added and removed, including components specific to the user's game
- [ ] entities can be spawned and despawned via a GUI
- [ ] entity hierarchies can be spawned and despawned via a GUI
  - [ ] manually
  - [ ] by composing scene files
- [ ] distinct editor and game views that can be run simultaneously
- [ ] live edit resource and component data in the editor view while the game is running

## Stage 3: UI/UX Foundations

- [ ] tooltips
- [ ] hotkeys
- [ ] primitive widgets
  - [ ] text entry
  - [ ] numeric entry
  - [ ] radio buttons
  - [ ] dropdown
  - [ ] checkboxes
  - [ ] slider
  - [ ] color selector
  - [ ] image preview
  - [ ] file path entry
  - [ ] progress bar
  - [ ] audio playback widget
- [ ] editor UI foundations
  - [ ] resizable panes
  - [ ] scrollable tool detail panels
  - [ ] toolbar
  - [ ] Blender-style workspaces
  - [ ] context menus
  - [ ] command palette
- [ ] dedicated hotkeys and controls for the most common operations:
  - [ ] manipulating camera
  - [ ] modifying transforms
  - [ ] toggling visibility
  - [ ] adding and removing entities
  - [ ] saving the project
  - [ ] opening the command palette

## Stage 4: Fundamental Features

- [ ] preferences
  - [ ] hotkey rebinding
  - [ ] camera controls
  - [ ] preferred language
- [ ] scene object picking: click on objects in the scene to select them in the inspector
- [ ] entities can be looked up by name in the inspector
- [ ] system stepping support
- [ ] create new Bevy project
  - [ ] blank
  - [ ] from template
- [ ] localization framework (first-party: English-only)

## Uncategorized work

There's a great deal of further feature work that needs to be done beyond the current milestones.
They haven't been forgotten, and are listed in no particular order here:

- [ ] editor extensions, for adding custom functionality
- [ ] a central hub for hosting (and selling?) editor extensions and assets
- [ ] performance overlays of all kinds
- [ ] system graph visualizer
- [ ] investigate a separate process model using Bevy Remote Protocol
- [ ] investigate code hot reloading and dynamic linking
- [ ] animation graph editor
- [ ] particle effects editor
- [ ] tilemap support
- [ ] edit the abstract syntax tree (AST) of the Bevy Scene Notation (.bsn) format
- [ ] in-game dev console
- [ ] MaterialX custom material creator

While there are also important engine features that will unblock or improve various parts of the editor (relations! BSN!),
this should not be tracked here: the emphasis is on user-facing goals, not any particular path.
