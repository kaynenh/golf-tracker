<script>
	import Header from '$lib/components/header.svelte';
	import Nav from '$lib/components/nav.svelte';
  import Chart from 'svelte-frappe-charts';

  let data = {
    labels: ['July 2', 'July 9', 'July 16', 'July 23', 'July 30', 'Aug 5', 'Aug 12'],
    datasets: [
      {
        values: [39, 41, 40, 36, 38, 34, 35]
      }
    ]
  };
</script>


<div>
<Nav />
<Header title='My Scores' />
<main>
  <div class="max-w-7xl mx-auto py-6 sm:px-6 lg:px-8">
    <!-- Replace with your content -->
    <div class="px-4 py-6 sm:px-0">
      <div class="border-4 border-dashed border-gray-200 rounded-lg h-96">
        <Chart data={data} type="donut" />
      </div>
    </div>
    <!-- /End replace -->
  </div>
</main>
</div>
