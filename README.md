# DSA3101 Manpower Optimisation for MFLG

👋 Hello! This is the deployment repo for our group's application stack. The frontend and backend repos are added as submodules to this repository, tagged to a commit hash that is stable and working.

For more detailed information on the [frontend](https://github.com/kevin-pek/dsa3101-frontend/) and [backend](https://github.com/shecheeyee/dsa3101-manpower-optimization-ci-backend/) repos please click the links here! To learn more about how to use our frontend application do check out our [user guide](https://docs.google.com/document/d/1UIK-Pzp5kED8erwhT2WhK-t0zv-lOWuc3SqK3n4nTaQ/edit?usp=sharing) as well!

Check out our [wiki](https://github.com/kevin-pek/dsa3101-deployment/wiki) for more information about our project!

Confused? Need help running this app? Check out our [help](https://github.com/kevin-pek/dsa3101-deployment/wiki/Help) page for a list of common issues and FAQs!

## Prerequisites

The entire application stack runs on docker, so please make sure you have [Docker](https://docs.docker.com/engine/install/) installed.

## Getting Started

To get started clone this repository, navigate to into the directory and run the following commands:

```sh
git submodule init    # registers the frontend and backend repos as submodules
git submodule update  # pulls the submodule repos
docker compose up -d  # run the entire stack (MySQL, Flask API, React App) in detached mode
```
NOTE: When you first run the app, the dashboard will not display any demand forecast. To view the demand forecast, make sure to input the actual customer count, click "Submit", and wait for the demand forecasting chart to be updated!

Once all containers are running the frontend app should now be accessible on port 3000. See `docker-compose.yml` for the port mappings for each service. Alternatively, you can also clone the frontend and backend repos separately and run them manually. See their respective repos for more information.

To login to the app, use the credentials `manager` and `pword123`.

Should you wish to make any changes in the frontend/backend repositories, you can edit them within the `frontend` and `backend` directories and push/pull any changes while inside the respective directories.
