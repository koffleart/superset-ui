## @superset-ui/plugin-chart-plotly-pie

[![Version](https://img.shields.io/npm/v/@superset-ui/plugin-chart-plotly-pie.svg?style=flat-square)](https://www.npmjs.com/package/@superset-ui/plugin-chart-plotly-pie)

This plugin provides Plotly Pie for Superset.

### Usage

Configure `key`, which can be any `string`, and register the plugin. This `key` will be used to
lookup this chart throughout the app.

```js
import PlotlyPieChartPlugin from '@superset-ui/plugin-chart-plotly-pie';

new PlotlyPieChartPlugin().configure({ key: 'plotly-pie' }).register();
```

Then use it via `SuperChart`. See
[storybook](https://apache-superset.github.io/superset-ui/?selectedKind=plugin-chart-plotly-pie) for
more details.

```js
<SuperChart
  chartType="plotly-pie"
  width={600}
  height={600}
  formData={...}
  queriesData={[{
    data: {...},
  }]}
/>
```

### File structure generated

```
├── package.json
├── README.md
├── tsconfig.json
├── src
│   ├── PlotlyPie.tsx
│   ├── images
│   │   └── thumbnail.png
│   ├── index.ts
│   ├── plugin
│   │   ├── buildQuery.ts
│   │   ├── controlPanel.ts
│   │   ├── index.ts
│   │   └── transformProps.ts
│   └── types.ts
├── test
│   └── index.test.ts
└── types
    └── external.d.ts
```
