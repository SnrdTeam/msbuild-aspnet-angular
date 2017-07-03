# msbuild-aspnet-angular

MSBuild targets for building ASP.NET Core project with Angular frontend. The targets uses [Angular CLI tool](https://github.com/angular/angular-cli).

## Features

  * Automatic building Frontend with ASP .NET Core Backend
  * Restoring Frontend's NPM dependencies is needed
  * Incremental build of Angular's Frontend
  * Visual Studio Integration
  * Debugging TypeScript in Visual Studio

## Requirements

  * Microsoft Visual Studio 2017 or later
  * MSBuild 15 or later
  * NuGet 3.5 or later
  * NPM 3.x
  * Angular CLI 1.1 or later

## Warnings

The usual folder `wwwroot` is not available for using during development anymore. The folder is used by Visual Studio to run project in debug mode, so Angular sources are compiled into this folder, while redundant files are deleted.

## Usage

See [Usage documentation](docs/Usage.MD).