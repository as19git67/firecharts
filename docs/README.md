# firecharts 

A collection of TrueNAS SCALE enhanced Helm charts for services for the voluntary fire brigade
(Germany, Bavaria).

## TrueNAS SCALE Chart Structure

A TrueNAS SCALE chart also has three additional files an `app-readme.md` file that provides a high level overview display in the TrueNAS SCALE UI and a `questions.yaml` file defining questions to prompt the user with and an `item.yaml` file outlining item specific details.

There are 2 directories `charts` and `test`, each representing a train. Chart releases created from catalog items in a specific train cannot be moved to another train. Currently only the `charts` train can be used inside the UI.

```shell
charts/ix-chart/<chart version>/
  app-readme.md            # TrueNAS SCALE Specific: Readme file for display in TrueNAS SCALE UI
  charts/                  # Directory containing dependency charts
  Chart.yaml               # Required Helm chart information file
  questions.yaml           # TrueNAS SCALE Specific: File containing questions for TrueNAS SCALE UI
  README.md                # Optional: Helm Readme file (will be rendered in TrueNAS SCALE UI as well)
  templates/               # A directory of templates that, when combined with values.yml will generate K8s YAML
  values.yaml              # The default configuration values for this chart
```

