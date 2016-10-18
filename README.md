# Sc.Dev.Perf

This repository provides configuration tweaks that when applied to a [Sitecore](https://sitecore.net/) development environment should improve website performance and resource utilization.

## Sitecore Web.config Include Files 

This repository provides a set of [Sitecore Configuration](https://community.sitecore.net/technical_blogs/b/sitecorejohn_blog/posts/all-about-web-config-include-files-with-the-sitecore-asp-net-cms) include files that tailor a website to remove unwanted features in development environments.

The developer performance settings include files can be found in the `Website/App_Config/Include/ZZZ-Developer-Environment-Settings` folder.

### Naming Convention Explained

The approach taken in this repository is to disable individual features via distinct configuration include files.

Each configuration include file follow the naming convention of:

```
    Disable.Feature.<FeatureName>.config
```

If you wish to prevent a feature from being disabled in your development environment simply remove the related configuration file. 

## Disabling Release Features

The various custom Sitecore configuration include files provided in this repository disable a variety of Sitecore release features that are often not required in a development environment.

Each performance optimization is detailed below.

### Disable MVC View Pre-Compilation

Removes the [Sitecore.Pipelines.Initialize.PrecompileSpeakViews](https://doc.sitecore.net/speak/development/improving_performance_by_disabling_precompilation_of_mvc_views) processors.

*Configuration File:* [Disable.Feature.PrecompileSpeakViews.config](Website/App_Config/Include/ZZZ-Developer-Environment-Settings/Disable.Feature.PrecompileSpeakViews.config)