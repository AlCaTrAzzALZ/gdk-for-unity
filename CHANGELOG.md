# Changelog

## Unreleased

### Added

- Added support for the Steam authentication flow.

## `0.1.2` - 2018-11-01

### Added

- Added the ability to acknowledge `AuthorityLossImminent` messages.
- Added an `Open Inspector` button to the `SpatialOS` menu in the Unity Editor.
- Added support for local mobile development.
- Added a changelog.
- Added field level dirty markers in components. This allows for partial automatic component updates to be sent.
- Added full support for `EntityQuery` world commands.
    - Added `Improbable.Gdk.Core.EntityQuerySnapshot` to hold the result of a single entity from a snapshot query.
    - Added `Improbable.Gdk.Core.ISpatialComponentSnapshot` to differentiate between a snapshot of component state and component data.

### Changed

- Changed the allocation type used internally for Unity ECS chunk iteration from `Temp` to `TempJob`
- Running a build in the Editor no longer automatically selects all scenes in the Unity build configuration
- `Improbable.Gdk.Core.Snapshot.AddEntity` now returns the `EntityId` assigned in the snapshot.
- Changed the `WorkerConnector` to be more generic and have an explicit `StandaloneWorkerConnector` for any workers running on OSX/Linux/Windows.
- Updated the default Unity version to `2018.2.14f1`.

### Fixed

- Fixed a bug where deserialising multiple events in a single component update only returned N copies of the last event received, where N is the number of events in the update.
- Fixed a broken link to the setup guide in an error message.

## `0.1.1` - 2018-10-19

### Added

- Better error messages when missing build support for a target platform.
- Better error messages for common problems when downloading the Worker SDK.

### Changed

- Position updates are now sent after all other updates.
- Simplified the heartbeating system in the `PlayerLifecycle` feature module.
- Updated the `README` and "Get Started" guide.

### Fixed

- The `GameLogic` worker is run in headless mode.
- The `Clean All Workers` menu item now works.

## `0.1.0` - 2018-10-10

The initial alpha release of the SpatialOS GDK for Unity.
