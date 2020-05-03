# Registry for Julia Vlasov packages

## Add Registry

To activate the registry, do
```
using Pkg
pkg"registry add https://github.com/juliavlasov/Registry"
```
This only needs to be done once per Julia installation.

## Register a Package

Install [LocalRegistry](https://github.com/GunnarFarneback/LocalRegistry.jl)

```
using LocalRegistry
register(package, "JuliaVlasov")
```

To register the new `package` in the registry `JuliaVlasov` you must be a member of the Julia Vlasov organization. 
The version number and other information is obtained from the package's
`Project.toml`. The `package` is specify by name as  a string.

Notes:
* You need to have a clean working copy of your registry.
* The changes are committed to the registry but **you need to push them
  yourself**.
* The package must be stored as a git working copy, e.g. having been
  cloned with `Pkg.develop`.
* The package must be available in the current `Pkg` environment.
* The package must have a `Project.toml` file.
* There is no checking that the dependencies are available in any
  registry.

## Register a New Version of a Package

```
using LocalRegistry
register(package)
```
