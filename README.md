# The-Goodness-Project (GNS)
![](https://i.paste.pics/014eecc6d1ee9dce3fba36f376a9c7a8.png)

The Goodness Project - a cryptocurrency project with the goal of raising funds in charity funds around the world.

[Our Website](https://goodnesscoin.xyz/)

[Bitcointalk ANN](https://bitcointalk.org/index.php?topic=5155791.0)

Libraries needed : boost >=1.58

If you want to compile the latest stable release, currently in production, clone the master branch :

```html
git clone https://github.com/GoodnessCoin/The-Goodness-Project.git
```
**Compile on Linux:** 

Update core submodule :

```html
$ cd The-Goodness-Project
$ git submodule update --init
$ git submodule foreach git pull origin master
```

Build :

```html
$ git clone -b master https://github.com/GoodnessCoin/The-Goodness-Project.git
$ cd The-Goodness-Project
$ mkdir build
$ cd build
$ cmake -D STATIC=ON -D CMAKE_BUILD_TYPE=RELEASE ..
$ PORTABLE=1 make
```
**Compile on Windows:**

```html
$ git clone -b master https://github.com/GoodnessCoin/The-Goodness-Project.git
$ cd The-Goodness-Project
$ mkdir build
$ cd build
$ cmake -DCMAKE_BUILD_TYPE=Release -DBOOST_ROOT=C:/local/boost_1_68_0 -G "Visual Studio 15 2017 Win64" ..
$ MSBuild goodness.sln /p:Configuration=Release /p:PlatformToolset=v141 /m
