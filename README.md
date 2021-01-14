# cpufetch

Simplistic yet fancy CPU architecture fetching tool
![cpu1](pictures/i9.png)

### Platforms
cpufetch currently supports x86_64 CPUs (both Intel and AMD) and ARM.

| Platform  | x86_64                    | ARM                | Notes             |
|:---------:|:------------------------:|:-------------------:|:-----------------:|
| Linux     | :heavy_check_mark:        | :heavy_check_mark: | Prefered platform. <br> Experimental ARM support |
| Windows   | :heavy_check_mark:        | :x:                | Some information may be missing. <br> Colors will be used if supported |
| Android   | :heavy_exclamation_mark:  | :heavy_check_mark: | Experimental ARM support |
| macOS     | :heavy_check_mark:        | :x:                | Some information may be missing |

| Emoji                   | Meaning       |
|:-----------------------:|:-------------:|
|:heavy_check_mark:       | Supported     |
|:x:                      | Not supported |
|:heavy_exclamation_mark: | Not tested    |


### Usage and installation
#### Linux
There is a cpufetch package available in Arch Linux ([cpufetch-git](https://aur.archlinux.org/packages/cpufetch-git)).

If you are in another distro, you can build `cpufetch` from source (see below)

#### Windows
In the [releases](https://github.com/Dr-Noob/cpufetch/releases) section you will find some cpufetch executables compiled for Windows. Just download and run it from Windows CMD.

#### Building from source
Just clone the repo and use `make` to compile it

```
git clone https://github.com/Dr-Noob/cpufetch
cd cpufetch
make
./cpufetch
```

The Makefile is designed to work on both Linux and Windows.

### Examples
Here are more examples of how `cpufetch` looks on different CPUs.

##### x86_64 CPUs

![cpu2](pictures/epyc.png)

![cpu3](pictures/cascade_lake.png)

##### ARM CPUs

![cpu4](pictures/exynos.png)

![cpu5](pictures/snapdragon.png)

### Colors and style
By default, `cpufetch` will print the CPU art with the system colorscheme. However, you can always set a custom color scheme, either
specifying Intel or AMD, or specifying the colors in RGB format:

```
./cpufetch --color intel (default color for Intel)
./cpufetch --color amd (default color for AND)
./cpufetch --color 239,90,45:210,200,200:100,200,45:0,200,200 (example)
```

In the case of setting the colors using RGB, 4 colors must be given in with the format: ``[R,G,B:R,G,B:R,G,B:R,G,B]``. These colors correspond to CPU art color (2 colors) and for the text colors (following 2). Thus, you can customize all the colors.

### Implementation

See [cpufetch programming documentation](https://github.com/Dr-Noob/cpufetch/blob/master/doc/README.md).

### Bugs or improvements
There are many open issues in github (see [issues](https://github.com/Dr-Noob/cpufetch/issues)). Feel free to open a new one report an issue or propose any improvement in `cpufetch`

### Testing
I would like to thank [Gonzalocl](https://github.com/Gonzalocl) and [OdnetninI](https://github.com/OdnetninI) for their help, running `cpufetch` in many different CPUs they have access to, which makes it easier to debug and check the correctness of `cpufetch`.
