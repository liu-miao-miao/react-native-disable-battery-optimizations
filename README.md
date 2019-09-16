# react-native-disable-battery-optimizations

## Getting started
## 安装

`$ npm install https://github.com/liu-miao-miao/react-native-disable-battery-optimizations.git`

### Mostly automatic installation
### 自动link

`$ react-native link react-native-disable-battery-optimizations`

### Manual installation
### 手动link

#### Android

1. Open up `android/app/src/main/java/[...]/MainActivity.java`
  - Add `import com.reactlibrary.RNDisableBatteryOptimizationsPackage;` to the imports at the top of the file
  - Add `new RNDisableBatteryOptimizationsPackage()` to the list returned by the `getPackages()` method
2. Append the following lines to `android/settings.gradle`:
  	```
  	include ':react-native-disable-battery-optimizations'
  	project(':react-native-disable-battery-optimizations').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-disable-battery-optimizations/android')
  	```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
  	```
      compile project(':react-native-disable-battery-optimizations')
  	```
4. add the following line to `AndroidManifest.xml`:
	```
	<uses-permission android:name="android.permission.REQUEST_IGNORE_BATTERY_OPTIMIZATIONS"/>
	```

## Usage
```javascript
import RNDisableBatteryOptimizations from 'react-native-disable-battery-optimizations';

RNDisableBatteryOptimizations.isBatteryOptimizationEnabled().then((isEnabled)=>{
	if(isEnabled){
		RNDisableBatteryOptimizations.openBatteryModal();
	}
});

RNDisableBatteryOptimizations;
```
  
