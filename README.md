<img src="https://cloud.githubusercontent.com/assets/75655/11761766/ec67aedc-a0cf-11e5-9a9f-b069cc57f555.png" width="180" alt="ElementDiff"> [![Version](https://img.shields.io/cocoapods/v/ElementDiff.svg?style=flat)](http://cocoapods.org/pods/ElementDiff)
[![License](https://img.shields.io/cocoapods/l/ElementDiff.svg?style=flat)](http://cocoapods.org/pods/ElementDiff)
[![Platform](https://img.shields.io/cocoapods/p/ElementDiff.svg?style=flat)](http://cocoapods.org/pods/ElementDiff)

<hr>

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

 - **0.3.0** - 2016-09-03 - Remove `reloadRowsAtIndexPaths`
 - 0.2.1 - 2016-03-04 - Make ElementDiff struct fields vars
 - **0.2.0** - 2015-12-22 - Allow for using custom identifier
 - **0.1.0** - 2015-12-12 - Initial public release
 - 0.0.0 - 2015-07-29 - Initial private version for project at [Q42](http://q42.com)

## License & Credits

ElementDiff is written by [Tom Lokhorst](https://twitter.com/tomlokhorst) of [Q42](https://q42.com) and available under the [MIT license](https://github.com/Q42/ElementDiff/blob/master/LICENSE), so fee free to use it in commercial and non-commercial projects.
