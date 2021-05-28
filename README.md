# Keptn Selfmon with Monaco

This repository holds monitoring as code (monaco) files for monitoring Keptn with Dynatrace, based on https://github.com/bacherfl/keptn-dt-monitoring .

## Instructions

1. Download and Install Monaco from https://github.com/dynatrace-oss/dynatrace-monitoring-as-code
2. Create a file called `environments.yaml` and add the following information:
    ```yaml
    environment1:
      - name: "Your Environment Name"
      - env-url: "URL To Your Dynatrace Environment"
      - env-token-name: "Dynatrace API Token (requires API v1 read/write configuration)"
    ```
3. Execute monaco as follows to verify that everything is valid:
    ```console
    monaco --environments environments.yaml --project keptn-selfmon --dry-run
    ```
4. Run it using monaco
    ```console
    export DT_API_TOKEN=<insert-dt-api-token>
    monaco --environments environments.yaml --project keptn-selfmon --dry-run
    ```

