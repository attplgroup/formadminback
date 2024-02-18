<!-- src/Admin/+page.svelte -->
<script>
    import SvelteTable from 'svelte-table';
      import Table from 'svelte-table'; // Import the data table component
    
      // Define columns
      const columns = [
          { title: 'ID', key: 'id' , value : (v)=>v.id },
          { title: 'Name', key: 'name' ,value : (v)=>v.name  },
          { title: 'Age', key: 'age',value : (v)=>v.age  },
          { title: 'City', key: 'city' ,value : (v)=>v.city  }
      ];
    
      // Define rows
      let rows = [
          { id: 1, name: 'John', age: 30, city: 'New York' },
          { id: 2, name: 'Alice', age: 25, city: 'Los Angeles' },
          { id: 3, name: 'Bob', age: 35, city: 'Chicago' }
      ];

      console.log('Trial component rendered');
    </script>
    
    <SvelteTable {columns} {rows} />
    