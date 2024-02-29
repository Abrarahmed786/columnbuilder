```markdown
# ColumnBuilder

This is a Flutter widget named `ColumnBuilder` that allows you to dynamically build a column of widgets based on the provided parameters.

## How to Use

### 1. Import the File

Import the `ColumnBuilder` file into your Flutter project.

```dart
import 'package:flutter/material.dart';
```

### 2. Implement ColumnBuilder Widget

Use the `ColumnBuilder` widget in your Flutter application by providing the required parameters.

```dart
ColumnBuilder(
  itemBuilder: (BuildContext context, int index) {
    // Build your widget here based on the index
    // Example: return Text('Item $index');
  },
  itemCount: itemCount,
  reverse: false, // Set to true if you want to reverse the order
  mainAxisAlignment: MainAxisAlignment.start, // Customize main axis alignment
  mainAxisSize: MainAxisSize.max, // Customize main axis size
  crossAxisAlignment: CrossAxisAlignment.start, // Customize cross axis alignment
  textDirection: null, // Set the text direction if needed
  verticalDirection: VerticalDirection.down, // Customize vertical direction
)
```

### Parameters

- **itemBuilder**: A function that returns the widget for each item in the column.
- **itemCount**: The total number of items in the column.
- **reverse**: (Optional) Whether to reverse the order of items in the column.
- **mainAxisAlignment**: (Optional) Aligns the children along the main axis.
- **mainAxisSize**: (Optional) Determines how much space the column should occupy along the main axis.
- **crossAxisAlignment**: (Optional) Aligns the children along the cross axis.
- **textDirection**: (Optional) The direction to resolve text and children order.
- **verticalDirection**: (Optional) Determines the order to lay children out vertically.

### Example

```dart
import 'package:flutter/material.dart';

class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: ColumnBuilder(
        itemBuilder: (BuildContext context, int index) {
          return ListTile(
            title: Text('Item $index'),
          );
        },
        itemCount: 10,
        reverse: false,
        mainAxisAlignment: MainAxisAlignment.center,
        mainAxisSize: MainAxisSize.max,
        crossAxisAlignment: CrossAxisAlignment.center,
        verticalDirection: VerticalDirection.down,
      ),
    );
  }
}
```

This will create a column with 10 list tiles with titles "Item 0", "Item 1", ..., "Item 9". Adjust the parameters according to your requirements.

Feel free to customize the parameters and the itemBuilder function according to your application's needs.
```