# ElementDiff

[![Version](https://img.shields.io/cocoapods/v/ElementDiff.svg?style=flat)](http://cocoapods.org/pods/ElementDiff)
[![License](https://img.shields.io/cocoapods/l/ElementDiff.svg?style=flat)](http://cocoapods.org/pods/ElementDiff)
[![Platform](https://img.shields.io/cocoapods/p/ElementDiff.svg?style=flat)](http://cocoapods.org/pods/ElementDiff)

Compute differences between two sequences of elements.

These can be passed to `updateSection` extensions to animate transitions.

## Example

```swift
// Update self.items array of view models
let previous: [ViewModel] = self.items
self.items = model.currentViewModels()
let diff = previous.diff(self.items)

// Animate changes to view models array
self.tableView.beginUpdates()
self.tableView.updateSection(0, diff: diff)
self.tableView.endUpdates()
```

## Installation

ElementDiff is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "ElementDiff"
```

Releases
--------

 - **0.1.0** - 2015-12-12 - Initial public release
 - 0.0.0 - 2015-07-29 - Initial private version for project at [Q42](http://q42.com)

## License & Credits

ElementDiff is written by [Tom Lokhorst](https://twitter.com/tomlokhorst) of [Q42](https://q42.com) and available under the [MIT license](https://github.com/Q42/ElementDiff/blob/master/LICENSE), so fee free to use it in commercial and non-commercial projects.