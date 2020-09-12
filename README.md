# Npm Publisher Support [![Github license](https://img.shields.io/github/license/codewriter-packages/NpmPublisherSupport.svg)](#)

A tool for managing [Unity](https://unity.com/) projects with multiple [UnityPackageManager](https://docs.unity3d.com/Packages/com.unity.package-manager-ui@1.8/manual/index.html) packages.
<br/>

[![Npm Publisher Support Preview](https://user-images.githubusercontent.com/26966368/73605698-a1d7ef80-45b2-11ea-8721-9dcd54b1346a.png)](#)

## About

Splitting up large codebases into separate independently versioned packages
is extremely useful for code sharing. However, making changes across many
repositories is messy and difficult to track, and testing across repositories
gets complicated really fast.

**NPM Publisher Suport is a tool that optimizes the workflow around managing multi-package
repositories.**

### Features

* Publish packages to any npm registry (like [NpmJS](https://www.npmjs.com/) or you own) directly from the Unity
* Fast switch between npm registries
* Track available updates for package dependencies:
  * From Unity built-in registry 
  * From [Scoped Package Registries](https://docs.unity3d.com/Manual/upm-scoped.html)
  * From Local project (it’s convenient if several packages are located in one project)
* Increment packages version from Unity
  * Patch Dependent option allow to automatically patch dependant packages version (If there are several packages in the project that depend on the current one)
* [Samples~](https://forum.unity.com/threads/samples-in-packages-manual-setup.623080/) and Documentation~ folders support:
  * Automatically copy contents of `Samples` folder to `Samples~` (same for `Documentation`) before package publishing
* _Publish modified packages_ command compares local package versions with specified remote registry that allow publish packages much faster

### What does a NPM Publisher Support repo look like?

There's actually very little to it. You have a file structure that looks like this:

```
Assets/
  Package-A/
    Sources/
      package.json
  Package-B/
    Sources/
      Runtime/
      Editor/
      Samples/
      Documentation/
      package.json
      README.md
      LICENSE.md
```

## Getting started
#### Step 1. Select registry
[![](https://user-images.githubusercontent.com/26966368/73605869-e5cbf400-45b4-11ea-9a1e-027bc592db83.png)](#)
#### Step 2. Login
[![](https://user-images.githubusercontent.com/26966368/73605873-fa0ff100-45b4-11ea-99e4-1f20508798e1.png)](#)
#### Step 3. Publish
Click `Publish` button.

### Install
Library distributed as git package ([How to install package from git URL](https://docs.unity3d.com/Manual/upm-ui-giturl.html))
<br>Git URL: `https://github.com/codewriter-packages/NpmPublisherSupport.git`