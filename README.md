# Sirius Diagnostics EPICS Screens

Sirius EPICS IOC Screens for Diagnostics

## Description

This repository acts like a reference point for all
diagnostics screens used for Sirius.

## Usage

```bash
./get-opis.sh -f [yes|no] -p [all|general|merge|top|<project_name>]
```

where the options are:

```bash
 -f          Get full git repository [yes|no]
 -p          Project name to update OPIs ["all", "general", "top", "merge"`
                    or specify a specific project name]
```

## Tip

It's possible to open CSS with the Main OPI being opened via the command-line with

```bash
<CSS executable> -data <path_to_workspace> -share_link <path_to_shared_directory>=/<directory_in_workspace> --launcher.openFile "/<directory_in_workspace>/<OPI>.opi"
```

Example:

```bash
./cs-studio/css -data /home/lerwys/workspace-share -share_link /home/lerwys/Repos/sirius-diagnostics-screens/build/op/opi=/displays --launcher.openFile "/displays/sirius_main_all.opi"
```

Example Sirius:

```bash
s-studio -consoleLog -pluginCustomization /home/opis/sirius-diagnostics-screens/cfg/combined_settings.ini -workspace_prompt /home/css-workspaces/diagnostics-work -share_link /home/opis/sirius-diagnostics-screens=/displays -workbench_xmi /home/opis/sirius-diagnostics-screens/cfg/diagnostics_workbench.xmi --launcher.appendVmargs -Dorg.eclipse.swt.internal.gtk.cairoGraphics=false -Dorg.eclipse.swt.internal.gtk.useCairo=false -Dorg.eclipse.swt.browser.DefaultType=mozilla --launcher.openFile "/displays/sirius_main_all.opi" &
```
