# Explanatory data visualization using Svelte JS

We are utilizing [↗ Svelte-Fusioncharts ↗](https://github.com/fusioncharts/svelte-fusioncharts) to build our Explanatory Data Visualization today.

To get started, take a look at `App.svelte`, especially the imports:

```js
import FusionCharts from "fusioncharts";
import Charts from "fusioncharts/fusioncharts.charts";
import FusionTheme from "fusioncharts/themes/fusioncharts.theme.fusion";
import SvelteFC, { fcRoot } from "svelte-fusioncharts";

fcRoot(FusionCharts, Charts, FusionTheme);
```

And the configuration:

```js
chartConfig = {
  type: "pie2d",
  width: "100%",
  height: "750",
  renderAt: "chart-container",
  dataSource,
};
```

[↗ More documentation on Svelte Fusion API and configuration options ↗](https://www.fusioncharts.com/dev/getting-started/sveltejs/your-first-chart-using-sveltejs)
