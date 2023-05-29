## Getting started

Add package to `pubspec.yaml`

```yaml
analog_clock:
  git:
    url: https://github.com/nurhamidqq/flutter_analog_clock.git
    ref: master
```

## How to use

Create controller for control the value of the clock

```dart
AnalogClockController analogClockController = AnalogClockController();
```

You can provide default value inside the controller

```dart
AnalogClockController analogClockController = AnalogClockController(
  value: DateTime.now(),
  periodType: PeriodType.am,
  onPeriodTypeChange: (date, period) {
    //TODO : Do Something
  },
);
```

you can set period change listener after initialize it

```dart
analogClockController.setOnPeriodTypeChangeListener((date, period) {
      //TODO : Do Something
});
```

Minimal usage

```dart
AnalogClockPicker(
  controller: analogClockController,
  size: MediaQuery.of(context).size.width * 0.74,
  secondHandleColor: Colors.red,
  minutesHandleColor: Colors.black,
  hourHandleColor: Colors.black,
  clockBackground: Image.asset(
    AssetImages.clockBackground,
  ),
  onClockChange: (date){
    //TODO : Do Something
  },
)
```
