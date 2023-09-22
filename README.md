<!--
This README describes the package. If you publish this package to pub.dev,
this README's contents appear on the landing page for your package.

For information about how to write a good package README, see the guide for
[writing package pages](https://dart.dev/guides/libraries/writing-package-pages).

For general information about developing packages, see the Dart guide for
[creating packages](https://dart.dev/guides/libraries/create-library-packages)
and the Flutter guide for
[developing packages and plugins](https://flutter.dev/developing-packages).
-->

# horizontal_list_view

Flutter horizontal list view with fixed crossAxisCount.

## Installing

Add to pubspec.yaml file

```sh
dependencies:
  horizontal_list_view: ^1.0.0
```

import

```sh
import 'package:horizontal_list_view/horizontal_list_view.dart';
```

## Usage

TODO: Include short and useful examples for package users. Add longer examples
to `/example` folder.

### Code example

```dart
import 'package:horizontal_list_view/horizontal_list_view.dart';

HorizontalListView(
    crossAxisCount: 3, // Number of items displayed per row.
    crossAxisSpacing: 16, // Spacing between items in the same row.
    controller: HorizontalListViewController(), // Optional scroll controller.
    itemCount: 10, // Total number of items in the list.
    itemBuilder: (BuildContext context, int index) {
        // Create and return the widgets for each item.
        return AspectRatio(
            aspectRatio: 16 / 9,
            child: Container(
                color: Colors.red,
                child: Center(
                    child: Text('item: $index'),
                ),
            ),
        );
    },
)