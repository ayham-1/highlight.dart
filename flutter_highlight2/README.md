# flutter_highlight2

![example_screenshot](https://raw.githubusercontent.com/ayham-1/highlight.dart/master/flutter_highlight2/screenshot.png)

This is not necessarily the output of the below example, but has been acheived
with the basis of that example.

Fork of flutter_higlight adding line numberings.

## Usage

```dart
import 'package:flutter/material.dart';
import 'package:flutter_highlight/flutter_highlight.dart';
import 'package:flutter_highlight/themes/github.dart';

class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    var code = '''main() {
  print("Hello, World!");
}
''';

    return HighlightView(
      // The original code to be highlighted
      code,

      // Specify language
      // It is recommended to give it a value for performance
      language: 'dart',

      // Specify highlight theme
      // All available themes are listed in `themes` folder
      theme: githubTheme,

      // Specify padding
      padding: EdgeInsets.all(12),

      // Specify text style
      textStyle: TextStyle(
        fontFamily: 'My awesome monospace font',
        fontSize: 16,
      ),
	  
	  // Enable Line numbers
	  lineNumbers: true,
	  
	  // Line numbers container border
	  lineNumbersBorder: Border.all(color: Colors.grey, width: 0),
	  
	  // Line numbers container radius
	  lineNumbersRadius: const BorderRadius.only(
      bottomLeft: Radius.circular(15), topLeft: Radius.circular(15)),
    );
  }
}
```

## References

- [All available languages](https://github.com/pd4d10/highlight/tree/master/highlight/lib/languages)
- [All available themes](https://github.com/pd4d10/highlight/blob/master/flutter_highlight/lib/themes)

## License

MIT
