# Dagger2.0
Dagger2.0配置  

``` 
  在 project/build.gradle 文件中加入apt插件依赖, 如:

      dependencies {
          classpath 'com.android.tools.build:gradle:2.2.3'
          classpath 'com.neenbedankt.gradle.plugins:android-apt:1.8'

          // NOTE: Do not place your application dependencies here; they belong
          // in the individual module build.gradle files
      }
  然后在`project/app/build.gradle 应用apt插件, 如:

  apply plugin: 'com.android.application'
  apply plugin: 'com.neenbedankt.android-apt'

  最后加上dagger2库依赖 :

  dependencies {
      compile fileTree(dir: 'libs', include: ['*.jar'])

      apt "com.google.dagger:dagger-compiler:2.2"
      compile "com.google.dagger:dagger:2.2"
  }  
  
```
