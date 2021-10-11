# Volt
[Short description] Volt is a virtual world paradigm built in Unity to help test spatial perception and navigation ability in human participants.

**Table of Contents**

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

These instructions will give you a copy of the project up and running on your local machine using the most up-to-date version of Volt running on a pre-compiled Unity build. If you are interested in making changes to the project before running it, please refer to the [Getting Started - Custom Build](#getting-started---custom-build) instructions below.

### Prerequisites

Requirements for the software and other tools to build:
- [MatLab v2018a](https://www.mathworks.com/products/matlab.html) - Version?
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

The original version of volt was built with Unity 5.0.0f4...

## Configuration File Overview
The configuration file is automatically produced by the header script and is read by the Unity build to inform the order of trial presentation along with other important characteristics. You can find a review of each line and its purpose below, but the repository also contains a `general.txt` which offers a similar explanation. 

>Note: Lines CANNOT have extra whitespace before or after them, so don't put any spaces after a line!

**config.txt**
| Line | Example Value | Type | Description 
|---|---|---|---|
| 1  | -1  | int  | Run number  |
| 2  | Johnny Appleseed  | string  | Subject's name  |
| 3  | 10.0  | float  | Collision sphere's radius (meters). If running free roam, set to 0 for no collisions. During task, set to 8.  |
| 4  | 10.0  | float  | Player's movement speed (meters per second)  |
| 5  | 0  | int  | Sets the phase to Learning if it is 0, if its one its Free Roam, otherwise it becomes Testing phase  | 
| 6  | 20.0  |  float | Phase's time limit (seconds)  |
| 7  |   |   | Parsed by 4s. pos 1-4 snow; 5-8 desert; 9-12 arena; 13-16 forest; 17-20 castle; 21-24 factory; 25-28 volano. First four and final 8 are static and 5-20 are randomized across participants.  |
| 8  |   |   |   |
| 9  |   |   |   |
| 10  |   |   |   |
| 11  |   |   |   |
| 12  |   |   |   |


```
participant number - int
participant initials - string
10.0 - Radius of Collision Sphere - float
10.0 - Speed in (vm/s) - float
0 - Mode - set to learning if 0, 1-free roam, 2 - testing - int
60.0 - phase time limit - float
1.0 - time initial image is shown - float (if free roam, set to 0)
1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28
4 0 0 0 2 3 4 5 6 0 - order of env that participant moves through
1 1 2 3 0 0 0 0 0 0 - spawn locations (cardinal locations)
1 2 1 3 0 0 0 0 0 0 - Object spawns (corners) (if free roam, use 0 to show no object)
```

Free roam always occurred within the practice environment (env 6) but others can be used. Free roam also used 1000s for time instead of 60. In lines 9-11 for free roam, there have to be a minimum 2 columns. 

### Environment Numbers: 
```
0 - Snow
1 - Desert
2 - Arena
3 - Meadow
4 - Castle
5 - Factory
6 - Volcano
```

## Built With

  - [Unity 3D](https://unity.com/) - Used to run the game the participant plays.
  - [MatLab](https://www.mathworks.com/products/matlab.html) - Used to generate headers and for analysis.

## Versions

There are currently two versions of Volt available for use. The first is located on the master branch and is the original version used for participant testing. This is where the main build and additional scripts are located. The second version is on a branch called `simple-movement` and it contains an updated version of the movement ability, giving participants smoother movement controls making it easier to navigate through the environment.

<!-- ## Related Projects
Volt contains the boilerplate code used in a number of experiments and this repository acts as the main codebase for altering and contributing to Unity code. This section provides a short overview of the other related repositories, should you be interested in checking them out. 

  - **Glutton** - [GitHub]() - This experiment test generalization ability in human participants. 
  - **Voltage** - [GitHub]() -->

## Authors
Roles and affiliations of authors at the time of data collection.
  - **Katherine R. Sherrill<sup>1,4</sup>** - *Post Doctoral Research Fellow* - [GitHub](https://github.com/orgs/prestonlab/people/ksherrill)
  - **Robert J. Molitor<sup>1</sup>** - *PhD Candidate* - [CV](https://minio.la.utexas.edu/colaweb-prod/person_files/0/6323/robert_molitor_curriculum_vitae.pdf)
  - **Ata B. Karagoz<sup>1</sup>** - *Undergraduate Research Assistant* - [GitHub](https://github.com/orgs/prestonlab/people/atakaragoz)
  - **Manasa Atyam<sup>1</sup>** - *Undergraduate Research Assistant* - [GitHub](https://github.com/orgs/prestonlab/people/manasa-atyam)
  - **Michael L. Mack<sup>3</sup>** - *Post Doctoral Research Fellow* - [Mack Lab](http://macklab.utoronto.ca/)
  - **Alison R. Preston<sup>1,2,4</sup>** - *Principle Investigator* - [Preston Lab](https://clm.utexas.edu/preston/)

1. Center for Learning and Memory, University of Texas at Austin, Austin, TX 78712, USA
2. Department of Psychology, University of Texas at Austin, Austin, TX 78712, USA
3. Department of Psychology, University of Toronto, Toronto, ON M5G 1E6, Canada
4. Department of Neuroscience, University of Texas at Austin, Austin, TX 78712, USA

## License

License details.

## Acknowledgments

This research was supported by the National Institute of Mental Health (R01 MH100121-01 to A.R.P.) and the National Institute of Neurological Disorders and Stroke (National Research Service Award F32 NS098808 to K.R.S.) of the National Institutes of Health. Thanks to Neal Morton, Hannah Roome, Athula Pudhiyidath, Christine Coughlin, and Nicole Varga for valuable discussions.
