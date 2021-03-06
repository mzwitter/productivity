<html>
<head>
	<style type="text/css">
	body {background-color: #fff1e0;}
	h1 {font-family: financierdisplayweb; text-align: center; font-size: 250%;}
	h2 {font-family: financierdisplayweb; font-size: 225%; background-color: #F6E6D7}
	h3 {font-family: financierdisplayweb; text-align: center; font-size: 150%;}
  h4 {font-family: financierdisplayweb; color: #751D2D; text-align: left; font-size: 100%; background-color: #F6E6D7}
	p {font-family: financierdisplayweb; color: #3C2D18; font-size: 130%}
  p.source {font-family: financierdisplayweb; text-align: right; font-style: italic; font-size: 80%}
  p.sub {{font-family: financierdisplayweb; color: #7F7164; font-size: 130%}}
  p.pic {{font-family: financierdisplayweb; color: #7F7164; font-size: 80%}}
  a:link, a:visited {color: #1C513F; font-family: financierdisplayweb; font-size: 100%; text-decoration: none;}
  a:hover {text-decoration: underline;}
  a:active {display: inline-block;}
  div.up {background-color: #F6E6D7}
	.content {max-width: 960px; margin: auto;}
	</style>
	<script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
    <script type="text/javascript">
      google.charts.load('current', {
        'packages':['corechart'],
        'mapsApiKey': 'AIzaSyD-9tSrke72PouQMnMX-a7eZSW0jkFMBWY'
      });
      google.charts.setOnLoadCallback(drawRegionsMap1);
      google.charts.setOnLoadCallback(drawDiffusionChart);
      google.charts.setOnLoadCallback(drawWagesChart);
      google.charts.setOnLoadCallback(drawSectorChart);
      google.charts.setOnLoadCallback(drawForebearanceChart);
      google.charts.setOnLoadCallback(drawInvestmentChart);
      google.charts.setOnLoadCallback(drawInvestment2Chart);


      function drawRegionsMap1() {
        var data = google.visualization.arrayToDataTable([
          ['Country', 'Productivity'],
          ['Belgium', 102.4],
          ['Bulgaria', 116.9],
          ['CZ', 108.7],
          ['Denmark', 105.6],
          ['Germany', 106.4],
          ['Estonia', 108.3],
          ['Ireland', 142.8],
          ['Greece', 93.6],
          ['Spain', 106.4],
          ['France', 105.1],
          ['Croatia', 114.9],
          ['Italy', 100.8],
          ['Cyprus', 105.3],
          ['Latvia', 117.6],
          ['Lithuania', 112.8],
          ['Luxembourg', 101.9],
          ['Hungary', 101.7],
          ['Malta', 111.4],
          ['Netherlands', 103.8],
          ['Austria', 104.8],
          ['Poland', 114.1],
          ['Portugal', 103.2],
          ['Romania', 135.1],
          ['Slovenia', 106.3],
          ['Slovakia', 113.4],
          ['Finland', 102.9],
          ['Sweden', 106.1],
          ['GB', 101.4],
          ['Norway', 103.1],
          ['Switzerland', 101.4]
        ]);

        var options = {
          region: '150', // Europe
          colorAxis: {colors: ['#FF0000', '#FFD300', '#E5FF00', '#00FF00']},
          backgroundColor: '#81d4fa',
          datalessRegionColor: 'grey',
          defaultColor: '#f5f5f5',
        };

        var chart = new google.visualization.GeoChart(document.getElementById('regions1_div'));

        chart.draw(data, options);
      }

      function drawDiffusionChart() {
        var data = google.visualization.arrayToDataTable([
          ['Year', 'Frontier companies', 'Total', 'Non-frontier companies'],
          ['2002', 173, 43, 35],
          ['2003', 160, 42, 35],
          ['2004', 180, 46, 39],
          ['2005', 198, 47, 39],
          ['2006', 219, 48, 39],
          ['2007', 248, 54, 44],
          ['2008', 308, 56, 43],
          ['2009', 278, 51, 39],
          ['2010', 262, 49, 38],
          ['2011', 264, 51, 39],
          ['2012', 280, 52, 39],
          ['2013', 317, 55, 42],
          ['2014', 346, 58, 43]
        ]);

        var options = {
          title: 'Labour productivity among frontier and non-frontier companies',
          width: 900,
          height: 500,
          backgroundColor: '#fff1e0',
          vAxis: {
            title: 'GVA per person, £ thousands'
          },
          hAxis: {
            format: '####'
          }
        };

        var chart = new google.visualization.LineChart(document.getElementById('Diffusion_chart'));

        chart.draw(data, options);
      }

      function drawWagesChart() {
        var data = google.visualization.arrayToDataTable([
          ['Country','Labour cost 2016 (2012=100)','Labour productivity 2016 (2012=100)','Region','size'],
          ['Austria', 111.1, 102.6118612, 'Western Europe', 1],
          ['Belgium', 103.2, 103.1324218, 'Western Europe', 1],
          ['Bulgaria', 132.3, 109.2825616, 'Eastern Europe', 1],
          ['Croatia', 110, 108.2331136, 'Eastern Europe', 1],
          ['Cyprus', 94.9, 103.5409806, 'Mediterranean', 1],
          ['Czech Republic', 113.5, 106.36353, 'Eastern Europe', 1],
          ['Denmark', 107.9, 103.2358673, 'Western Europe', 1],
          ['Estonia', 128.5, 105.2724184, 'Eastern Europe', 1],
          ['EU (28 countries)', 107.6, 103.5444393, 'Europe', 1],
          ['Euro area (19 countries)', 106.2, 103.5454553, 'Europe', 1],
          ['Finland', 105.4, 102.817224, 'Western Europe', 1],
          ['France', 104.4, 103.956556, 'Western Europe', 1],
          ['Germany', 110.7, 103.6477742, 'Western Europe', 1],
          ['Greece', 87.5, 98.67749227, 'Mediterranean', 1],
          ['Hungary', 118.4, 100.3762554, 'Eastern Europe', 1],
          ['Ireland', 104.8, 129.9777884, 'Western Europe', 1],
          ['Italy', 102.5, 100.6952697, 'Mediterranean', 1],
          ['Latvia', 131.8, 109.2860167, 'Eastern Europe', 1],
          ['Lithuania', 132.5, 103.180078, 'Eastern Europe', 1],
          ['Luxembourg', 109.8, 104.5356616, 'Western Europe', 1],
          ['Malta', 113, 108.6567024, 'Mediterranean', 1],
          ['Netherlands', 103.9, 103.3350409, 'Western Europe', 1],
          ['Norway', 111.2, 103.1333486, 'Western Europe', 1],
          ['Poland', 117.3, 107.0777656, 'Eastern Europe', 1],
          ['Portugal', 101.6, 100.790646, 'Mediterranean', 1],
          ['Romania', 133.4, 120.2599296, 'Eastern Europe', 1],
          ['Slovakia', 117.9, 109.5146809, 'Eastern Europe', 1],
          ['Slovenia', 107.8, 103.511257, 'Eastern Europe', 1],
          ['Spain', 101, 102.7236829, 'Mediterranean', 1],
          ['Sweden', 112.4, 105.595548, 'Western Europe', 1],
          ['United Kingdom', 109.6, 101.9018708, 'Western Europe', 1]
        ]);

        var options = {
          title: 'Wage and productivity growth 2012-2016',
          width: 900,
          height: 600,
          backgroundColor: '#fff1e0',
          bubble: {textStyle: {color: 'none'}},
          vAxis: {
            title: 'Labour productivity 2016 (2012=100)',
            baseline: 100
          },
          hAxis: {
            title: 'Labour cost 2016 (2012=100)',
            baseline: 100,
            viewWindowMode: 'explicit',
            viewWindow: {
              max: 140
            },
          },
          sizeAxis: {
            minvalue: 0,
            maxValue: 5,
            maxsize: 5,
          },
        };

        var chart = new google.visualization.BubbleChart(document.getElementById('Wages_chart'));

        chart.draw(data, options);
      }
      
      function drawSectorChart() {
        var data = google.visualization.arrayToDataTable([
          ['SECTOR', 'AGRICULTURE FORESTRY AND FISHING', 'MINING AND QUARRYING', 'MANUFACTURING', 'UTILITIES', 'CONSTRUCTION', 'DISTRIBUTION TRANSPORT ACCOMODATION FOOD', 'INFORMATION AND COMMUNICATION', 'FINANCIAL AND REAL ESTATE', 'PROFFESSIONAL AND ADMINISTRATIVE', 'PUBLIC SECTOR EDUCATION HEALTH', 'ARTS AND OTHER', 'TOTAL', {role: 'annotation'} ],
          ['1998-2006', 0.104695417, -0.012407422, 0.528353506, 0.042829324, 0.046434907, 0.558293124, 0.153899655, 0.141212838, 0.300711606, 0.081321892, 0.035694998, 1.97754116, ''],
          ['2007-2009', -0.058320901, -0.014780015, 0.047462012, -0.055749665, -0.264265618, -0.27645177, 0.078669493, 0.061936131, 0.031284972, -0.180826156, -0.068697195, -0.698699718, ''],
          ['2010-2017', 0.00557266, -0.010929293, 0.141712792, -0.019711665, 0.189477387, 0.335474223, 0.067750401, -0.083495001, 0.291613741, 0.036848531, -0.036916025, 0.910267391, '']
        ]);

        var options = {
          width: 960,
          height: 700,
          backgroundColor: '#fff1e0',
          isStacked: true,
          seriesType: 'bars',
          series: {
            11: {type: 'line'}},
          vAxis: {
            ticks: [-1, 0, 1, 2],
            title: "Contribution to productivity growth [% pt]"
          }
        };

        var chart = new google.visualization.ComboChart(document.getElementById('Sectors_chart'));

        chart.draw(data, options);
      }
      function drawForebearanceChart() {
        var data = google.visualization.arrayToDataTable([
          ["Percent of banks' exposure to each industry reciaving forebearance", "change in productivity growth between 1998-2007 and 2008-2017", {role: 'annotation'}],
          [12, -3.079967502, "Manufacturing"],
          [27, 0.596050452, "construction"],
          [3, -0.848017396, "wholesale and retail"],
          [6, -3.413625471, "transport"],
          [28, -2.516326889, "accomodation and food"],
          [7, -3.209308023, "information and communication"],
          [6, -2.530720862, "professional and scientific"],
          [14, -0.755801337, "administration"]
        ]);

        var options = {
          title: "Loose monetary policy and productivity",
          width: 900,
          height: 700,
          backgroundColor: '#fff1e0',
          vAxis: {
            title: 'Change in average productivity growth between 1998-2007 and 2008-2017 [% pt]',
          },
          hAxis: {
            title: "Percent of banks' exposure to each industry recieving forebearance",
          },
          legend: {
            position: 'none'
          },
          colorAxis: {
            legend: {
              position: 'none'
            }
          }
        };

        var chart = new google.visualization.ScatterChart(document.getElementById('Forebearance_chart'));

        chart.draw(data, options);
      }
       function drawInvestment2Chart() {
        var data = google.visualization.arrayToDataTable([
          ["year", "1980s", "1990s", "2000s"],
          [0, 100, 100, 100],
          [1, 95.250708, 97.789339, 94.851123],
          [2, 86.93382099, 91.6005627, 81.79617676],
          [3, 92.15982156, 92.42417726, 85.49857191],
          [4, 96.81012414, 93.86533544, 87.35041797],
          [5, 105.6143979, 99.86938281, 89.16175991],
          [6, 110.0176523, 104.6029968, 92.20734196],
          [7, 112.4322317, 109.485486, 98.74405044],
          [8, 123.0888015, 107.7343292, 101.4834217],
          [9, 141.3613587, 114.8000906, 103.2947638]
        ]);

        var options = {
          title: 'Investment after crisis',
          width: 900,
          height: 500,
          backgroundColor: '#fff1e0',
          vAxis: {
            title: 'Gross fixed capital formation [pre-crisis peak=100]'
          },
          hAxis: {
            title: 'Xears since beginning of recession',
            format: '####'
          }
        };

        var chart = new google.visualization.LineChart(document.getElementById('Investment2_chart'));

        chart.draw(data, options);
      }
       function drawInvestmentChart() {
        var data = google.visualization.arrayToDataTable([
          ["Asset class", "2000-2007", "2009-2016"],
          ["Total assets", 2.490124, 1.202725],
          ["Dwellings", 2.363561232, 1.236853797],
          ["Transport", 3.13587867, 14.63587265],
          ["ICT", 11.29064036, 1.552536887],
          ["Other machinery", 0.874558284, -0.249601331],
          ["Cultivated assets", 8.744772627, -2.915711215],
          ["Software", 3.599134434, 0.71943757],
          ["R&D", 3.021932595, 0.455029942],
          ["buildings and transfer costs", 1.891965403, 0.727830979]
        ]);

        var options = {
          title: "Investment",
          width: 900,
          height: 700,
          backgroundColor: '#fff1e0',
          vAxis: {
            title: 'Gross fixed capital formation',
          },
          hAxis: {
            title: "Asset classes",
          },
          colorAxis: {
            legend: {
              position: 'in'
            }
          }
        };

        var chart = new google.visualization.ColumnChart(document.getElementById('Investment_chart'));

        chart.draw(data, options);
      }
    </script>
</head>
<body>
<div class="content">
<h1>FINANCIAL TIMES</h1>
<div class="up">
  <h4>UK Labour productivity</h4>
  <h2>Productivity puzzle in 6 charts</h2>
<p class="sub">Productivity growth in industrialized economies has slowed since the financial crisis.</p>
<p style="text-align: center"><img src="productivity.jpg" alt="Productivity growth in industrialized economies has slowed since the financial crisis" align="middle" width="650"></p>
<p class="pic">Productivity growth is key to long-term sustainable economic and welfare growth.</p>
</div>
<hr>
<p>Productivity growth in industrialized economies has slowed since the financial crisis. Labour productivity, which measures the amount of output produced by a unit of labour, is tightly connected to long-term, sustainable welfare growth. </p>
<p>In the UK average productivity growth has halved since the crisis. Most other industrialized countries have experienced slowing growth as well, although some more so than others. The map shows labour productivity gains in Europe between 2010 and 2016.</p>
<div id="regions1_div" style="border: 1px solid #ccc"></div>
<p class="source">Source: EuroStat</p>
<p>Economists have put forward many explanations for the fall in productivity growth. Here we explore some of them. 
<br>
<h3 id="Innovation">Slowing innovation</h3>
<p>Some argue innovation has stopped. Or more accurately, that contemporary innovations, such as a smartphone app do not bring productivity improvements on the scale that electricity or indoor plumbing had 100 years ago.</p>
<p>It is a contentious theory and <a href="https://ftalphaville.ft.com/2017/12/08/2196617/can-we-avoid-another-financial-crisis/">some economists</a> see it as an attempt by the profession to absolve itself of responsibility and lay the blame for economic under-performance at the feet of engineers. It is also hard to reconcile with all the talk about robots and artificial intelligence taking over blue-collar jobs.</p> 
<p>The chart below also does not support such a conclusion. It shows labour productivity growth among companies on the productivity frontier (5 percent of most productive companies in each sector) and companies that lag behind.</p>
<div id="Diffusion_chart" style="border: 1px transparent #ccc"></div>
<p class="source">Source: <a href="https://www.bankofengland.co.uk/-/media/boe/files/speech/2017/productivity-puzzles.pdf?la=en&hash=708C7CFD5E8417000655BA4AA0E0E873D98A18DE">BoE</a></p>
<p>It is clear from the chart that productivity growth among the best is doing just fine, but the rest struggle to keep pace.</p>
<p>Another <a href="https://www.ineteconomics.org/perspectives/blog/which-productivity-puzzle">theory</a> suggests we might be in the first stages of a cycle of what economists call technology diffusion. The argument rests on the historical experience that each innovation needs a few decades to reach its productive potential. After it is picked up by the most innovative companies, infrastructure - be it electricity grid 100 years ago or broadband internet today - needs to be built. Only then can the majority of companies begin experimenting with the new technology and finding its new productive uses. In short, the theory states we might be on the verge of an ICT-based productivity boom.</p>
<br>
<h3 id="wagestagnation">Wage stagnation</h3>
<p>Growing cost of labour provides an incentive for companies to invest in labour-saving machinery and therefore raise productivity. Some argue that wage stagnation is to blame for lack of productivity growth. The chart below plots European countries based on their wage and productivity growth between 2012 and 2016.</p>
<div id="Wages_chart" style="border: 1px transparent #ccc"></div>
<p class="source">Source: EuroStat, own calculations</p>
<p>Correlation between wages and productivity has long been acknowledged. But there is less agreement among economists as to the direction of this relationship. While some say wages should follow productivity, others argue a proactive wage policy is needed to force companies into productivity enhancement, particularly by raising the minimum wage, which is most widespread in the least productive industries.</p>
<br>
<h3 id="sectors">Productivity growth among sectors</h3>
<p>It is important to note, that different sectors exhibit different productivity trends. The chart shows sector contributions to total productivity growth.</p> 
<p>Finance and real estate, for example, shifted from a positive contribution before the crisis, to a negative today. Manufacturing contributed more than half a percentage point on average in the decade prior to the crisis, but now its contribution is less than a third of that. Significant slowdown in productivity growth can also be observed in the ICT, as well as distribution, transport, food and accomodation sectors.</p>
<p>On the other hand productivity of professional services, which include such activities as legal, managerial, engineering, advertising and similar services, continues to grow with the same pace after the crisis. Construction sector even managed to significantly expand its contribution to overall productivity growth.</p>
<div id="Sectors_chart" style="border: 1px transparent #ccc"></div>
<p class="source">Source: ONS, own calculations</p>
<p></p>
<br>
<h3 id="monetary">Accommodative monetary policy</h3>
<p>Some, including <a href="https://www.oecd.org/eco/The-Walking-Dead-Zombie-Firms-and-Productivity-Performance-in-OECD-Countries.pdf">OECD</a>, argue that central banks' post-crisis monetary policy, including low interest rates and quantitative easing, stifled productivity growth. Loose monetary policy enables unproductive <i>"zombie companies"</i> to stay in the business and limits competitive pressures on companies to invest and innovate.</p>
<p>The following chart plots sectors of UK economy by prevalence of loan forebearance against percentage point fall in average labour productivity since the crisis. There is no clear correlation between sector dependence on forebearance and productivity slowdown.</p>
<div id="Forebearance_chart" style="border: 1px transparent #ccc"></div>
<p class="source">Source: <a href="https://www.bankofengland.co.uk/-/media/boe/files/quarterly-bulletin/2013/sme-forbearance-and-its-implications-for-monetary-and-financial-stability.pdf?la=en&hash=AD7C84B9463B0C6D507139A56F62BFF7EAD22256">BoE</a>, ONS, own calculations</p>
<p>The BoE concludes, that while there is some evidence to support the negative effects of accomodative monetary policy, it is <a href="https://www.bankofengland.co.uk/-/media/boe/files/quarterly-bulletin/2013/sme-forbearance-and-its-implications-for-monetary-and-financial-stability.pdf?la=en&hash=AD7C84B9463B0C6D507139A56F62BFF7EAD22256"><i>"far from conclusive"</i></a> and <a href="https://www.bankofengland.co.uk/-/media/boe/files/speech/2017/productivity-puzzles.pdf?la=en&hash=708C7CFD5E8417000655BA4AA0E0E873D98A18DE"><i>"the net effect on productivity is an empirical question"</i></a>. It is important to note however, that while BoE policy might have adversly affected productivity, it also helped to sustain employment.</p>
<br>
<h3 id="investment">Insufficient investment</h3>
<p>For productivity to grow companies need to invest in more and better buildings, machinery, software or other labour-saving improvements.</p>
<p>This does not seem to be happening. The chart shows gross fixed capital formation by business sector in first 9 years after the pre-crisis peak for the 1980s, 1990s and 2000s recessions.</p>
<div id="Investment2_chart" style="border: 1px transparent #ccc"></div>
<p class="source">Source: OECD, own calculations</p>
<p>In 2016 UK business sector investments were only 3 percent higher than prior to the crisis. In other words, there has not been a post recession investment boom, as can be seen after previous recessions. As to why that is </p>
<br>  

</div>
</body>
</html>
