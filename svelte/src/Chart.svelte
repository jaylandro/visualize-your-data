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
    "caption": "Top 10 Countries by Happy Life Years",
    "yaxisname": "Years",
    "aligncaptionwithcanvas": "0",
    "plottooltext": "<b>$dataValue</b> years of happines",
    "theme": "fusion"
  },
  "data": [
    {
      "label": "Switzerland",
      "value": 59.3,
      "Footprint": 5.8
    },
    {
      "label": "Iceland",
      "value": 58,
      "Footprint": 6.4
    },
    {
      "label": "Sweden",
      "value": 57.4,
      "Footprint": 7.3
    },
    {
      "label": "Norway",
      "value": 57.1,
      "Footprint": 5
    },
    {
      "label": "Netherlands",
      "value": 57,
      "Footprint": 5.3
    },
    {
      "label": "Finland",
      "value": 54.6,
      "Footprint": 5.9
    },
    {
      "label": "Denmark",
      "value": 54.4,
      "Footprint": 5.5
    },
    {
      "label": "Austria",
      "value": 54.4,
      "Footprint": 6.1
    },
    {
      "label": "Canada",
      "value": 53.9,
      "Footprint": 8.2
    },
    {
      "label": "Australia",
      "value": 53.1,
      "Footprint": 9.3
    }
  ]
};

const chartConfigs = {
   type: 'bar2d',
   width: 600,
   height: 600,
   order: 'desc',
   dataFormat: 'json',
   dataSource
};

</script>

<SvelteFC {...chartConfigs} />