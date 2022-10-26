# Đây là dự án demo việc sử dụng module quy hoạch (aar)

## How to build

### Tải aar

 - Tải các files aar (4 files) vào folder: app/libs/aar/

### build.gradle (Project level)

 - Cần khai báo biến ext { ktx = '1.0.2', ... },  build.gradle(module level) sẽ dùng các biến này

### build.gradle (Module level)

 - Thêm các dependencies cần thiết của module quy hoạch (com.google.gms, io.realm, multidex, ...)
 - Thêm các *.aar (implementation files('libs\\...aar'))

### Resources:
 
 - Bạn nên copy đầy đủ resources: icons, ... vào projects của bạn
 - Bạn có thể tùy chỉnh app chính bằng cách thay file bằng file resources riêng với cùng tên
 - **TODO**: trong các version aar sau, có thể public các resource ra, và project  chính không cần phải thêm các resource này vào thư mục res, nhưng hiện tại bạn cần phải thêm bằng tay.

### File settings.gradle

 - Khi build dự án chính có thể bị lỗi, cần khai báo các repositories maven, jitpack, ...

### References:
 
 - https://developer.android.com/studio/projects/android-library

## How to use

 - Từ bất kỳ đâu trong ứng dụng của bạn đều gọi được SplashActivity

```kotlin
    val intent = Intent(this, com.geotechvn.dakland.ui.splash.SplashActivity::class.java)
    startActivity(intent)
```
