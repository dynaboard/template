# Get Started
Dynaboard allows you to export a project state and use that as a starting point for future projects. These starting points can be used when creating a new project by importing the file or by pasting in the GitHub repository URL.

## dynaboard.yml
This is the configuration file which Dynaboard reads to learn about your template. It must be located at the root of the repository, and has a few required fields:
 - `type`
   - Only currently supported type is `project`
 - `filename`
   - The path from the root of the repository to your template yml file
 - `name`
   - The display name of the template, and default name for new projects using this template

Additionally, you may supply a freetext `description` key. This is currently unused, but may be shown as extra information on the create project screen in the future.


## Your Template
The actual exported value of your template. This can exist anywhere in the repository, so long as the filename in your `dynaboard.yml` file points to it. Currently, we support YAML format (with both `.yml` and `.yaml` file extensions) and JSON format (with `.json` file extension). The contents of this file are typically created via the `Export project` menu item in the Dynaboard app, and contain a map of nodes used by the application, along with a `runtimeVersion` string which represents an internal Dynaboard compatability version and should not be modified.

In order to ensure continued compatability between your template and the evergreen Dynaboard app, it is suggested that edits be made by creating a template project, editing in Dynaboard and re-exporting.