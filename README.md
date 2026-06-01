
## 👤 Identitas
### Nama       : Aneka Lisda 
### NIM        : 25141013P
### Kelas      : SI2KR
### Mata Kuliah: Pemrograman Berbasis Objek  
---
```dart
import 'dart:math';

class Circle {
  final double radius;

  // Main Constructor
  Circle(this.radius);

  // Redirecting dari diameter
  Circle.fromDiameter(double diameter)
      : this(diameter / 2);

  // Redirecting dari keliling
  Circle.fromCircumference(double circumference)
      : this(circumference / (2 * pi));

  // Redirecting dari luas
  Circle.fromArea(double area)
      : this(sqrt(area / pi));

  double get diameter => radius * 2;
  double get circumference => 2 * pi * radius;
  double get area => pi * radius * radius;

  @override
  String toString() {
    return '''
Radius        : ${radius.toStringAsFixed(2)}
Diameter      : ${diameter.toStringAsFixed(2)}
Keliling      : ${circumference.toStringAsFixed(2)}
Luas          : ${area.toStringAsFixed(2)}
''';
  }
}

void main() {
  // Main constructor
  var c1 = Circle(7);

  // Redirecting dari diameter
  var c2 = Circle.fromDiameter(14);

  // Redirecting dari keliling
  var c3 = Circle.fromCircumference(44);

  // Redirecting dari luas
  var c4 = Circle.fromArea(154);

  print('=== Circle 1 ===');
  print(c1);

  print('=== Circle 2 ===');
  print(c2);

  print('=== Circle 3 ===');
  print(c3);

  print('=== Circle 4 ===');
  print(c4);
}
```
[Klik di sini untuk menjalankan kode DartPad](https://dartpad.dev/77ac8a58c23da7d985d1a0fdf54cb0f9)
---

