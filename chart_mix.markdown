---
layout: page
title: Chart_mix.js
permalink: /chartmix/
---

<script src="//cdnjs.cloudflare.com/ajax/libs/moment.js/2.29.1/moment.min.js"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/Chart.js/2.9.4/Chart.min.js"></script>

<canvas id="canvas" width="400" height="400"></canvas>
<script>
window.onload = function () {
        var ctx       = document.getElementById("canvas").getContext("2d");
        window.myLine = new Chart(ctx, config);
    };
var timeFormat = 'DD/MM/YYYY';

    var config = {
        type:    'line',
        data:    {
            datasets: [
                {
                    label: "US Dates",
                    data: [{
                        x: "04/01/2014", y: 175
                    }, {
                        x: "10/01/2014", y: 175
                    }, {
                        x: "04/01/2015", y: 178
                    }, {
                        x: "10/01/2015", y: 178
                    }],
                    fill: false,
                    borderColor: 'red'
                },
                {
                    label: "UK Dates",
                    data:  [{
                        x: "01/04/2014", y: 175
                    }, {
                        x: "01/10/2014", y: 175
                    }, {
                        x: "01/04/2015", y: 178
                    }, {
                        x: "01/10/2015", y: 178
                    }],
                    fill:  false,
                    borderColor: 'blue'
                }
            ]
        },
        options: {
            responsive: true,
            title:      {
                display: true,
                text:    "Chart.js Time Scale"
            },
            scales:     {
                xAxes: [{
                    type:       "time",
                    time:       {
                        format: timeFormat,
                        tooltipFormat: 'll'
                    },
                    scaleLabel: {
                        display:     true,
                        labelString: 'Date'
                    }
                }],
                yAxes: [{
                    scaleLabel: {
                        display:     true,
                        labelString: 'value'
                    }
                }]
            }
        }
    };
</script>