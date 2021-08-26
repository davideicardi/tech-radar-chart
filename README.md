# blips-chart

Tech Radar Chart using D3.js

![screenshot](https://raw.github.com/davideicardi/blips-chart/master/docs/blips-chart.png)

## Usage

```html
<svg id="radar"></svg>

<script type="module">
    import { create_chart } from 'https://cdn.jsdelivr.net/npm/blips-chart@1.4.0/dist/blips-chart.js';
    const quadrants = [
        { name: "DATA", text_color: "#ddd" },
        { name: "PLATFORMS", text_color: "#ddd" },
        { name: "PATTERNS", text_color: "#ddd" },
        { name: "LANGUAGES", text_color: "#ddd" },
    ];
    const rings = [
        { name: "ADOPT", color: "#f75258", text_color: "#f75258" },
        { name: "TRIAL", color: "#54f6d1", text_color: "#54f6d1" },
        { name: "ASSESS", color: "#5371f7", text_color: "#5371f7" },
        { name: "HOLD", color: "#6f58c4", text_color: "#6f58c4" }
    ];
    const blips = [
        {
            name: "azuredevops",
            title: "Azure DevOps",
            quadrant: "PLATFORMS",
            ring: "HOLD",
            moved: 0
        },
        {
            name: "dotnetcore",
            title: ".NET Core",
            quadrant: "LANGUAGES",
            ring: "ADOPT",
            moved: 0,
            url: "https://dotnet.microsoft.com/"
        },
        {
            name: "eventsourcing",
            title: "EventSourcing",
            quadrant: "PATTERNS",
            ring: "TRIAL",
            moved: -1
        },
        {
            name: "cqrs",
            title: "CQRS",
            quadrant: "PATTERNS",
            ring: "ADOPT",
            moved: 0
        },
        {
            name: "kafka",
            title: "Kafka",
            quadrant: "DATA",
            ring: "TRIAL",
            moved: 1,
            url: "https://kafka.apache.org/"
        },
        {
            name: "strapi",
            title: "Strapi",
            quadrant: "DATA",
            ring: "ASSESS",
            moved: -1
        },
        {
            name: "deno",
            title: "Deno",
            quadrant: "LANGUAGES",
            ring: "ASSESS",
            moved: 0
        },
        {
            name: "docker",
            title: "Docker",
            quadrant: "PLATFORMS",
            ring: "ADOPT",
            moved: 0
        },
    ];

    create_chart({
        svg_id: "radar",
        colors: {
            background: "#1d1d1d",
            grid: "#ddd"
        },
        quadrants: quadrants,
        rings: rings,
        entries: blips,
    });
</script>
```

See [this](https://jsfiddle.net/603ejspt/) jsfiddle or `examples` folder for more details.