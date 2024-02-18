<script>
    import { Router, Route, Link } from 'svelte-routing';
    import Sidebar from './Sidebare.svelte';
    import Admin from './routes/Admin/Admin.svelte'
    import Forms from './routes/Forms/Forms.svelte'
  import Trial from './routes/Admin/Trial.svelte';
  import Sidebare from './Sidebare.svelte';

    let currentRoute = '';
    export let URL = "" ; 

    function handleRouteChange(event) {
        currentRoute = event.detail.location.pathname.split('/')[1];
        console.log('Route changed:', currentRoute);
    }

</script>

<div class="container">
   

    <Router {URL}>

        <Link  to="/" >
            
        </Link>

        <Route path= "/" component= {Sidebare} />

        <Link  to="/admin" >
            
        </Link>

        <Route path= "/admin" component= {Admin} />
    
             
        <Link  to="/trial" >
            
        </Link>
    
        <Route path= "/trial" component= {Trial} />

        <Link  to="/forms" >
            
        </Link>
    
        <Route path= "/forms" component= {Forms} />
        
    </Router>
</div>

<style>
    
</style>
