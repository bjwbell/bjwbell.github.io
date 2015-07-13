---
layout: post
title:  "End of Moore's Law"
---


Is Moore's Law Over?

Moore's Law has never been a physical law. It's observation due at least partly to economics.

Problems with Moore's Law appeared a few years ago with Nvidia's 40nm to 28nm transition. Nvidia put out a presentation,
http://www.extremetech.com/computing/123529-nvidia-deeply-unhappy-with-tsmc-claims-22nm-essentially-worthless,
outlining the issues they had with their foundry, TSMC. 
Particularly the cost per transistor did not decrease with the 40nm to 28nm transistion. This was partly because 28nm uses [double patterning](https://en.wikipedia.org/wiki/Multiple_patterning) lithography.
Double patterning is needed because extreme ultraviolet (EUV) lithography has faced setbacks & delays.

This was the first time that shrinking the process node yielded no economic benefit.
The implications are obvious. There is less economic incentive for developing new process nodes.



Intel's recent annoucement of a ~1 year delay to their 10nm architecture, Cannonlake, indicates that Moore's Law is at least severely strained.

Last year Intel's 14nm architecture, Broadwell, was also delayed by 6 months.

- 65nm (Core), 3/2006
- 45nm (Penryn), 11/2007 
- 32nm (Westmere), 1/2010
- 22nm (Ivybridge), 4/2012
- 14nm (Broadwell), 10/2014
- 10nm (Cannonlake), ?



<div id="container" style="width: 600px; height: 400px; margin: 0 auto"></div>
<script type="text/javascript">
$(function () {
$('#container').highcharts({
            chart: {
                type: 'spline'
            },
            title: {
                text: 'Process Nodes',
                x: -20 //center
            },
            subtitle: {
                text: 'Source: Wikipedia',
                x: -20
                },

        xAxis: {
            type: 'datetime',
            dateTimeLabelFormats: { // don't display the dummy year
                month: '%e. %b aaa',
                year: '%b %y'
            },
            title: {
                text: 'Date'
            }
        },
            yAxis: {
                title: {
                    text: 'log(nm)'
                    },
                    min: 0,
                    type: 'linear'
                    },
                    
            tooltip: {
                valueSuffix: ' (log nm)'
            },
        plotOptions: {
            spline: {
                marker: {
                    enabled: true
                }
            }
        },        series: [{
            name: "Intel",
            // Define the data points. All series have a dummy year
            // of 1970/71 in order to be compared on the same x axis. Note
            // that in JavaScript, months start at 0 for January, 1 for February etc.
            data: [
                [Date.UTC(2006, 3, 1), 4.17],
                [Date.UTC(2007, 11, 1), 3.80],
                [Date.UTC(2010, 01, 1), 3.46],
                [Date.UTC(2012, 04, 1), 3.09],
                [Date.UTC(2014, 10, 1), 2.64],
                [Date.UTC(2017, 10, 1), 2.30],
            ]
        }]
        });
    });

</script>


