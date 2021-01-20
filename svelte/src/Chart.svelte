<script>
import FusionCharts from 'fusioncharts';
import Charts from 'fusioncharts/fusioncharts.charts';
import FusionTheme from 'fusioncharts/themes/fusioncharts.theme.fusion';
import SvelteFC, { fcRoot } from 'svelte-fusioncharts';
import { onMount } from "svelte";

// Always set FusionCharts as the first parameter
fcRoot(FusionCharts, Charts, FusionTheme);

const dataSource = {
  "chart": {
    "caption": "Lead sources by industry",
    "yaxisname": "Number of Leads",
    "aligncaptionwithcanvas": "0",
    "plottooltext": "<b>$dataValue</b> leads received",
    "theme": "fusion"
  },
  "data": [
    {
      "label": "Travel & Leisure",
      "value": "41"
    },
    {
      "label": "Advertising/Marketing/PR",
      "value": "39"
    },
    {
      "label": "Other",
      "value": "38"
    },
    {
      "label": "Real Estate",
      "value": "32"
    },
  ]
};

const chartConfigs = {
   type: 'bar2d',
   width: 600,
   height: 400,
   dataFormat: 'json',
   dataSource
};

// dataFormat: 'jsonurl',
// dataSource: 'https://static.fusioncharts.com/sample/oilReserves.json'
</script>

<SvelteFC {...chartConfigs} />