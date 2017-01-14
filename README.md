libsaltpack-jni
===============
A Java Native Interface wrapper for [libsaltpack](https://github.com/Gherynos/libsaltpack).

Dependencies
------------

* [libsaltpack](https://github.com/Gherynos/libsaltpack)
* [libsodium](https://download.libsodium.org/doc/) >= 1.0.3
* [msgpack](https://github.com/msgpack/msgpack-c) >= 2.0.0
* [GMP](https://gmplib.org/) >= 6.0.0 (or [MPIR](http://mpir.org/) >= 2.6.0 on Windows)

Building
--------

Here's how to build the JAR package and the dynamic library on Linux or OSX:

```bash
mvn compile
cd target
cmake ../
make
cd ..
mvn package
```

### Android

Here's how to build libsaltpack-jni and all its dependencies for Android using Docker:

```bash
docker run -v `pwd`:/opt/libsaltpack-jni -t ubuntu:16.04 /bin/bash /opt/libsaltpack-jni/android/compile.sh
```

This will produce the `libsaltpack-jni-libs.jar` file under the `android` directory; add that file together with the JAR created by the previous step to the Android Studio project.

Documentation
-------------

The Javadoc can be found here: [https://gherynos.github.io/libsaltpack-jni](https://gherynos.github.io/libsaltpack-jni).

Copyright and license
---------------------

Copyright 2016-2017 Luca Zanconato (<luca.zanconato@nharyes.net>)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this work except in compliance with the License.
You may obtain a copy of the License in the LICENSE file, or at:

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.