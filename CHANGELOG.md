## 0.4.0 Think Locally (July 12, 2016)
### Added
- Local class names can be specified via the `local-class` attribute (#31)
- PostCSS options such as custom syntax are passed through via `postcssOptions` config (#34)
- The default extension for modules can be specified via `extension` config (#34)

### Fixed
- An `intermediateOutputPath` may be specified in order to have ember-css-modules emit to a location other than `<app-name>.css`, leaving other files in the styles tree untouched for further processing (#28). See the README for further details on how this in combination with the changes in #34 allow for working alongside other CSS preprocessors.

## 0.3.3 If At First (July 6, 2016) 
### Fixed
- `_super` is now properly called in the addon `init()` to avoid a deprecation notice

## 0.3.2 Hidden Gems (May 1, 2016)
### Fixed
- Hidden files (e.g. `.DS_Store`) no longer break the build process (#21)

### Changed
- Final linking of `@value`s now occurs _before_ other PostCSS plugins execute (#23)

## 0.3.1 Contain Your Excitement (April 14, 2016)
### Fixed
- Classes named `container` can be used once again (#15)

## 0.3.0 Location, Location, Location (Mar 31, 2016)
### Changed
- Modules are now more intelligently ordered in the final output by default, according to composition and value dependencies. See the README for further details.

### Added
- Ability to override scoped name generation (#3)
- Greater (explicit) control over module ordering in final output (#7)

### Fixed
- Handle component lookup changes in Ember 2.5+ without crashing
- Pass through non-CSS files in the styles tree (#13)
- Don't rely on custom registry options set up in an initializer (#14)
