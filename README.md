# Barbarian Upload GitHub Action

Uploads conan package to [Barbarian](https://barbarian.bfgroup.xyz).

The recipe has to be present in the file system before using this action, for example by using github action [`actions/checkout`](https://github.com/actions/checkout).

This action will create a `barbarian` branch on the repo, and commit information on the recipe revision on this branch. More information can be found in [barbarian documentation](https://barbarian.bfgroup.xyz/create.html) 

**Works on**: Linux

## Inputs

### `recipe_path`

The path to the recipe to upload. It should contain the conanfile

### `package_name`

The name of the package to upload

### `package_version`

The version of the package to upload

## Outputs

No outputs

## Example usage

~~~~
      - uses: ericLemanissier/barbarian-upload@main
        with:
          recipe_path: recipes/qt/6.x.x
          package_name: qt
          package_version: 6.2.1

~~~~
