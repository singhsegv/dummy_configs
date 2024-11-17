# AeroDaaS

## Updated configs after the meeting on 17th November 2024
- `primitives` directory contains the exhaustive set of sample primitives. Each file is named after the primitive category, i.e., Navigation, Sensing, etc.
- `17_nov` directory contains new app configs based on the latest discussions.

## To-be brainstormed
- `DNN callbacks` concept
    - Do we give `DNN callbacks` kinda concept in the basic navigation primitives?
    - Or do we keep these separate and provide a way to compose applications?
    - Or set some functions to be called
- Still dicey if primitives are blocking or non-blocking
    - Async or sync
    - This will change the code generation for a lot of other primitives
    - Primitives like `return_to_base` with conditions can be kind of intent registrations based on conditions to be polled constantly
    - If we go with sync style ordered list of tasks, analytics activation and deactivation can make our lives easy

## About
Every directory is an application idea and each of them contains:
1. `daas_layer_1.yaml`: For apps to be submitted to our platform. This is the user facing config.
2. `daas_layer_2.yaml`: This is the system facing config created for the layer 1 file.
3. `non_daas_layer_1.yaml`: For apps that user wants to run locally on his/her drone. This is the user facing config.
4. `non_daas_layer_2.yaml`: This is the system facing config created for the layer 1 file.

## Note
Start looking at this repo from the `vip_navigation` example since that has the most documented YAML files for now.