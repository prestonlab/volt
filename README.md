# Volt
[Short description] Volt is a virtual world paradigm built in Unity to help test spatial perception and navigation ability in human participants.

## Getting Started - Prebuilt

These instructions will give you a copy of the project up and running on
your local machine using the most up-to-date version of Volt running on a pre-compiled Unity build. If you are interested in making changes to the project before
running it, please refer to the `Getting Started - Custom Build` instructions below.

### Prerequisites

Requirements for the software and other tools to build:
- [MatLab](https://www.mathworks.com/products/matlab.html)

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

## Built With

  - [Tech 1]() - Used
    for the Code of Conduct

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code
of conduct, and the process for submitting pull requests to us.

## Versioning

We use [Semantic Versioning](http://semver.org/) for versioning.

## Authors

  - **Author 1** - *Provided README Template* -
    [Link](https://github.com/)

See also the list of
[contributors](https://github.com/)
who participated in this project.

## License

License details

## Acknowledgments

  - Acknowledgement 1
