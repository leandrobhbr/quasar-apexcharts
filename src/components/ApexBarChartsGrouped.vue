<template>
  <card-base>
    <apexchart type="bar" height="230" :options="chartOptions" :series="series"></apexchart>
  </card-base>
</template>

<script>
import CardBase from 'components/CardBase'
export default {
  name: 'ApexBarChartsGrouped',
  components: {
    CardBase
  },
  data () {
    return {
      series: [{
        data: [44, 55, 41],
        name: 'Green'
      }, {
        data: [53, 32, 33],
        name: 'Yellow'
      }, {
        data: [60, 15, 25],
        name: 'RED'
      }],
      chartOptions: {
        colors: ['#00e396', '#feb019', '#ff4560'],
        title: {
          text: 'Bar Charts Grouped',
          align: 'left',
          style: {
            color: '#FFF'
          }
        },
        legend: {
          labels: {
            colors: '#FFF'
          }
        },
        chart: {
          type: 'bar',
          height: 430
        },
        plotOptions: {
          bar: {
            horizontal: true,
            dataLabels: {
              position: 'top'
            }
          }
        },
        dataLabels: {
          enabled: true,
          offsetX: -6,
          style: {
            fontSize: '12px',
            colors: ['#fff']
          }
        },
        stroke: {
          show: true,
          width: 1,
          colors: ['#fff']
        },
        xaxis: {
          categories: [2001, 2002, 2003],
          labels: {
            style: {
              colors: '#fff'
            }
          }
        },
        yaxis: {
          labels: {
            style: {
              colors: '#fff'
            }
          }
        }
      }
    }
  }
}
</script>
