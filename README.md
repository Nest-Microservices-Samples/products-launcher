

## Dev

1. Clone the repository
2. Create an.env based at .env.template
3. Running command `docker compose up build`


### Steps to create Git Submodules


1. Create a new repository on GitHub
2. Clone the repository on the local machine.
3. Add the submodule, where `repository_url` is the url of the repository and `directory_name` is the name of the folder where you want the submodule to be saved (it must not exist in the project)

```
git submodule add <repository_url> <directory_name>

```
4. Add the changes to the repository (git add, git commit, git push).
Ex:

```
git add .
git commit -m “Add submodule”
git push

```
5. Initialize and update Sub-modules, when someone clones the repository for the first time, you should run the following command to initialize and update the sub-modules

```
git submodule update --init --recursive

```
6. To update the sub-module references

```
git submodule update --remote

```

## Important

If working in the repository that has the sub-modules, **first update and push** the sub-module and **then** the main repository.

If you do it the other way around, you will lose references to the sub-modules in the main repository and you will have to resolve conflicts.