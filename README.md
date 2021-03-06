# LiveData-CombineTuple-KT

LiveData-CombineTuple-KT contains helper functions for LiveData, to combine their latest emissions into typed tuples.

Under the hood, it uses Tuples-KT to help provide combiners from 2 to 16 arity.

``` kotlin
combineTuple(liveData1, liveData2, liveData3)
    .observe(lifecycleOwner) { (t1, t2, t3) ->
        // do something with combined livedata values
    }
```

## Using LiveData-CombineTuple-KT

In order to use LiveData-CombineTuple-KT, you need to add `jitpack` to your project root `build.gradle.kts`
(or `build.gradle`):

``` kotlin
// build.gradle.kts
allprojects {
    repositories {
        // ...
        maven { setUrl("https://jitpack.io") }
    }
    // ...
}
```

or

``` groovy
// build.gradle
allprojects {
    repositories {
        // ...
        maven { url "https://jitpack.io" }
    }
    // ...
}
```

and then, add the dependency to your module's `build.gradle.kts` (or `build.gradle`):

``` kotlin
// build.gradle.kts
implementation("com.github.Zhuinden:livedata-combinetuple-kt:1.0.0")
```

or

``` groovy
// build.gradle
implementation 'com.github.Zhuinden:livedata-combinetuple-kt:1.0.0'
```

## License

    Copyright 2020 Gabor Varadi

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
