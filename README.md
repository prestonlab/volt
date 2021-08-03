# Volt
[Short description] Volt is a virtual world paradigm built in Unity to help test spatial perception and navigation ability in human participants.

**Table of Contents**
- [Volt](#volt)
  - [Getting Started - Prebuilt](#getting-started---prebuilt)
    - [Prerequisites](#prerequisites)
    - [Building](#building)
      - [Setting up the Header](#setting-up-the-header)
      - [Practice Study Phase](#practice-study-phase)
      - [Practice Study Phase](#practice-study-phase-1)
  - [Getting Started - Custom Build](#getting-started---custom-build)
  - [Volt Overview](#volt-overview)
  - [Configuration File Overview](#configuration-file-overview)
  - [Built With](#built-with)
  - [Versions](#versions)
  - [Authors](#authors)
  - [License](#license)
  - [Acknowledgments](#acknowledgments)

## Getting Started - Prebuilt

These instructions will give you a copy of the project up and running on
your local machine using the most up-to-date version of Volt running on a pre-compiled Unity build. If you are interested in making changes to the project before running it, please refer to the [Getting Started - Custom Build](#getting-started---custom-build) instructions below.

### Prerequisites

Requirements for the software and other tools to build:
- [MatLab](https://www.mathworks.com/products/matlab.html) - Version?
- [Unity 3D v5.0.0f4](https://unity3d.com/get-unity/download/archive) - This can be downloaded using the archive. If you have multiple versions of unity installed on your machine, we recommend that you install [Unity Hub](https://unity3d.com/get-unity/download) as well to manage the versions you use. **Note**: If you are using Mac OS Catalina or later (>10.15.x), you should install this version of Unity with the "Unity Editor" not the "Unity Installer" due to the differences in how storage is managed in newer versions of Mac OS.

### Building

First off, clone this repository to your local machine and open `MatLab` to create the header for your experiment. 

#### Setting up the Header
In `MatLab`, make sure to change to the directory of where you cloned this repo. For example, 

```
cd ~/Experiments/volt
```

Next, create the subject header with this command: 

```
volt_header
```

You will be prompted to enter in the `Subject #`, `Subject Initials`, and `Subject Gender`. 

Once entered, you will have built your subject header. 

#### Practice Study Phase

When you are ready to run the experiment, begin by creating the configuration file. In `MatLab`, type:

```
volt_config(header, 2)
```

Here, `header` is referencing the header you created in the previous step, and `2` is the type of trial. In this case - a test trial.

Once that's done running, run the following command to launch the Unity build: 

```
. volt.bash
```

Press "Play!" and the free roam will run. After completion, hit `Enter` in the terminal.

#### Practice Study Phase

Once the practice study phase is over, you can begin the practice test phase with similar commands. 

In `MatLab`, type: 

```
volt_config(header, 3)
```

Next, run the experiment as before: 

```
. volt.bash
```

After completion, hit `Enter` in the terminal. 


## Getting Started - Custom Build

These instructions will give you a copy of the project up and running on
your local machine and allow you to make any modifications to the codebase that you like. If you are only interested in running the
experiment with the most recent build, please refer to the `Getting Started - Prebuilt` instructions above.


## Volt Overview

The original version of volt was built with Unity 

## Configuration File Overview

## Built With

  - [Unity 3D](https://unity.com/) - Used to run the game the participant plays.
  - [MatLab](https://www.mathworks.com/products/matlab.html) - Used to generate headers and for analysis.

## Versions

There are currently two versions of Volt available for use. The first is located on the master branch and is the original version used for participant testing. This is where the main build and additional scripts are located. The second version is on a branch called `simple-movement` and it contains an updated version of the movement ability, giving participants smoother movement controls making it easier to navigate through the environment.

## Authors

  - **Katherine R. Sherrill<sup>1,4</sup>** - *Role* - [GitHub](https://github.com/orgs/prestonlab/people/ksherrill)
  - **Robert J. Molitor<sup>1</sup>** - *Role* - [CV](https://minio.la.utexas.edu/colaweb-prod/person_files/0/6323/robert_molitor_curriculum_vitae.pdf)
  - **Ata B. Karagoz<sup>1</sup>** - *Role* - [GitHub](https://github.com/orgs/prestonlab/people/atakaragoz)
  - **Manasa Atyam<sup>1</sup>** - *Role* - [GitHub](https://github.com/orgs/prestonlab/people/manasa-atyam)
  - **Michael L. Mack<sup>3</sup>** - *Role* - [Mack Lab](http://macklab.utoronto.ca/)
  - **Alison R. Preston<sup>1,2,4</sup>** - *Role* - [Preston Lab](https://clm.utexas.edu/preston/)

1. Center for Learning and Memory, University of Texas at Austin, Austin, TX 78712, USA
2. Department of Psychology, University of Texas at Austin, Austin, TX 78712, USA
3. Department of Psychology, University of Toronto, Toronto, ON M5G 1E6, Canada
4. Department of Neuroscience, University of Texas at Austin, Austin, TX 78712, USA

## License

License details.

## Acknowledgments

  - Acknowledgement 1
  - Acknowledgement 2
  - Acknowledgement 3
