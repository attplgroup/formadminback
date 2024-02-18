<!-- Sidebar.svelte -->
<script>
    import { Link } from 'svelte-routing';
    import Admin from './routes/Admin/Admin.svelte';
    import Forms from './routes/Forms/Forms.svelte';
    import Trial from './routes/Admin/Trial.svelte';

    export const ABC = "";
</script>

<nav class="sidebar">
    <ul>
        <li class="sidebar-header">Admin Panel</li>
        <li><Link to="/admin" class="sidebar-link" component={Admin}>Admin</Link></li>
        <li><Link to="/forms" class="sidebar-link" component={Forms}>Forms</Link></li>
        <li><Link to="/trial" class="sidebar-link" component={Trial}>Trial</Link></li>
    </ul>
</nav>

<style>
    .sidebar {
        position: fixed;
        top: 0;
        bottom: 0;
        left: 0;
        width: 250px;
        background-color: #2a2a2a;
        padding: 20px;
        overflow-y: auto;
    }

    .sidebar ul {
        list-style-type: none;
        padding: 0;
    }

    .sidebar-header {
        font-size: 24px;
        font-weight: bold;
        color: #fff;
        padding: 20px;
        text-transform: uppercase;
        border-bottom: 2px solid white;
    }

    .sidebar-link {
        display: block;
        color: #ccc;
        text-decoration: none;
        padding: 10px 0;
        transition: color 0.3s ease;
    }

    .sidebar-link:hover {
        color: #fff;
    }
</style>
