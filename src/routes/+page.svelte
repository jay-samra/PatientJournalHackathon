<script lang="ts">
    import { supabase } from '$lib/supabaseClient';
    import { onMount } from 'svelte';
  
    // Declare `data` as a reactive variable
    let data = $state<any[]>([]);
  
    onMount(async () => {
      const { data: tableData, error } = await supabase.from('countries').select('*');
      if (error) {
        console.error('Error fetching data:', error);
      } else {
        console.log('Fetched data:', tableData);
        data = tableData; // This will now trigger UI updates
      }
    });
  </script>
  
  <h1>Supabase Data</h1>
  <ul>
    {#each data as item}
      <li>{JSON.stringify(item)}</li>
    {/each}
  </ul>
