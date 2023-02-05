# tailwind-styles-android

Recently started to learn about Tailwind and web development.
I found the design patters to be awesome and wanted to bring the basics to Android.

It includes this categories from Tailwind, check out the links of their docs for more details.
 - [colors](https://tailwindcss.com/docs/customizing-colors#default-color-palette)
 - [spacing](https://tailwindcss.com/docs/customizing-spacing#default-spacing-scale)
 - [font size](https://tailwindcss.com/docs/font-size)
 - [border radius](https://tailwindcss.com/docs/border-radius)
 - [borders width](https://tailwindcss.com/docs/border-width)

You can find a list of the added resources here:
 - [colors.xml](https://github.com/puntogris/tailwind-styles-android/blob/main/tailwind-styles-android/src/main/res/values/colors.xml)
 - [dimens.xml](https://github.com/puntogris/tailwind-styles-android/blob/main/tailwind-styles-android/src/main/res/values/dimens.xml)

And use them as any other resource in your app.

Example:
```xml
<com.google.android.material.button.MaterialButton
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_margin="@dimen/spacing_1"
    android:backgroundTint="@color/slate_600"
    android:padding="@dimen/spacing_4"
    android:text="Tailwind is awesome!"
    android:textColor="@color/amber_50"
    app:cornerRadius="@dimen/rounded_md"
    app:strokeColor="@color/slate_700"
    app:strokeWidth="@dimen/border_2" />
```

### Installation
In your root build.gradle add the JitPack repo
```gradle
allprojects {
    repositories {
        maven { url 'https://jitpack.io' }
    }
}
```

In your app build.gradle add the dependency
```gradle
dependencies {
    implementation 'com.github.puntogris:tailwind-styles-android:1.0'
}
```