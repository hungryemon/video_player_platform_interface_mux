# video_player_platform_interface_mux

A common platform interface for the [`video_player_mux`][1] plugin.

This interface allows platform-specific implementations of the `video_player_mux`
plugin, as well as the plugin itself, to ensure they are supporting the
same interface.

# Usage

To implement a new platform-specific implementation of `video_player_mux`, extend
[`VideoPlayerPlatform`][2] with an implementation that performs the
platform-specific behavior, and when you register your plugin, set the default
`VideoPlayerPlatform` by calling
`VideoPlayerPlatform.instance = MyPlatformVideoPlayer()`.

# Note on breaking changes

Strongly prefer non-breaking changes (such as adding a method to the interface)
over breaking changes for this package.

See https://flutter.dev/go/platform-interface-breaking-changes for a discussion
on why a less-clean interface is preferable to a breaking change.

[1]: https://github.com/hungryemon/video_player_mux
[2]: lib/video_player_platform_interface_mux.dart
