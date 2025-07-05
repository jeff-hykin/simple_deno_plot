```js
import { plotlyPlotHtml } from "https://esm.sh/gh/jeff-hykin/simple_deno_plot/main.js"

Deno.writeTextFileSync('plot1.html', 
    // same args as plotly.js examples, just builds it for you with proper escaping and offline support
    plotlyPlotHtml([{
        x: ['January', 'February', 'March', 'April', 'May'],
        y: [10, 15, 13, 17, 21],
        type: 'scatter',
        mode: 'lines+markers',
        name: 'Sales',
        line: { color: 'blue' }
    }],{
        title: 'Monthly Sales Trend',
        xaxis: { title: 'Month' },
        yaxis: { title: 'Sales ($k)' }
    })
)
```