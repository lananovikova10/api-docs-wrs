[//]: # (title: Syntetic SDK example)

## listProductsReleases

List all available IntelliJ-based IDE releases with their updates. The result list is used for testing the plugin with Plugin Verifier using the runPluginVerifier task.

<table>
            <tr>
            <td>Parameter</td>
            <td>Description</td>
            <td>Default value</td>
            </tr>
            <tr>
                <td>
                    <p><code>updatesFile</code> </p>
                    <p><format color="Crimson">required</format></p>
                </td>
                <td>
                    <p><format color="Gray">
                        List&lt;String&gt;</format></p>
                    <p>Path to the products releases update file.</p>
                </td>
                <td>Gradle cache</td>
            </tr>
        <tr>
            <td><code>types</code>
            </td>
            <td>
            <p><format color="Gray">
                        String</format> </p>
                <p>List of types of IDEs that will be listed in results.</p>
            </td>
            <td>
                <p>intellij.type</p>
            </td>
        </tr>
 <tr>
            <td><code>sinceVersion</code>
            </td>
            <td>
            <p><format color="Gray">
                        String</format> </p>
                <p>Lower boundary of the listed results in product marketing version format, e.g., 2020.2.1. It takes precedence over listProductsReleases.sinceBuild property.</p>
            </td>
            <td>
                <p>intellij.version</p>
            </td>
        </tr>
    </table>
