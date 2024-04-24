Welcome to the GitHub Pages branch for My Helm Charts repository! This repository hosts Helm charts that you can use to deploy applications and services on Kubernetes clusters.

## Usage

To use these Helm charts, you'll need Helm installed on your local machine and access to a Kubernetes cluster. Follow these steps to get started:

1. **Add the Helm Repository**: Add the repository to Helm:

    ```bash
    helm repo add arslan https://arslankhanali.github.io/helm-charts/
    ```

2. **Search for Available Charts**: List the available charts:

    ```bash
    helm search repo arslan
    ```

3. **Install a Chart**: Install a chart on your Kubernetes cluster:

    ```bash
    helm install my-release-name arslan/chart-name
    ```

4. **Customize Chart Values**: You can customize chart values by creating a `values.yaml` file and passing it to the `helm install` command with the `-f` flag.

For more information on Helm and how to use it, refer to the [Helm documentation](https://helm.sh/docs/).

## [Available Charts](https://github.com/arslankhanali/helm-charts/tree/main/charts)

- [operators](https://github.com/arslankhanali/helm-charts/tree/main/charts/operators): Install operators on Red Hat OpenShift
- [workbench](https://github.com/arslankhanali/helm-charts/tree/main/charts/workbench): Create a workbench in Red Hat OpenShift AI
- [rbac](https://github.com/arslankhanali/helm-charts/tree/main/charts/rbac): Create a role and rb
- [s2i](https://github.com/arslankhanali/helm-charts/tree/main/charts/s2i): Deploy a pod from a source

## Contributing

If you'd like to contribute to this repository by adding new charts, fixing bugs, or improving documentation, please fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
