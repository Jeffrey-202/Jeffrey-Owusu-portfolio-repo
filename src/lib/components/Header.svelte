<!-- Header -->
<header>
    <nav>
        <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/about_page">About</a></li>
            <li><a href="/contacts_page">Contact</a></li>
            <li class="dropdown">
                <a href="/projects_page" class="dropdown-toggle">Projects</a>
                <ul class="dropdown-content">
                    <li><a href="/3d-art">3D Art</a></li>
                    <li><a href="/graphic-design">Graphic Design</a></li>
                    <li><a href="/music">Music</a></li>
                    <li><a href="/digital-art">Digital art</a></li>
                    <li><a href="/drawings-page">Drawings</a></li>
                    <li><a href="/food rush">food rush game</a></li>
                    <li><a href="/video-editing">Video Editing</a></li>
                </ul>
            </li>
        </ul>
    </nav>
</header>

<style>
    header {
        background-color: #034918;
        padding: 2rem;
        text-align: center;
    }
    
    nav ul {
        list-style: none;
        padding: 0;
        margin: 0;
        display: flex;
        justify-content: center;
    }
    
    nav ul li {
        margin: 0 15px;
        position: relative;
    }
    
    nav ul li a {
        font-family: "Audiowide", sans-serif;
        color: white;
        font-weight: bold;
        text-decoration: none;
        display: block;
        padding: 10px;
        transition: all 0.3s ease;
    }
    
    /* Dropdown styles */
    .dropdown-content {
        display: none;
        position: absolute;
        background-color: #027a3a;
        min-width: 160px;
        box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
        z-index: 1;
        left: 50%;
        transform: translateX(-50%);
        border-radius: 4px;
    }
    
    .dropdown-content li {
        margin: 0;
        padding: 0;
        border-bottom: 1px solid #034918;
    }
    
    .dropdown-content li:last-child {
        border-bottom: none;
    }
    
    .dropdown-content a {
        padding: 12px 16px;
        text-decoration: none;
        display: block;
        text-align: center;
        white-space: nowrap;
    }
    
    .dropdown-content a:hover {
        background-color: #034918;
    }
    
    .dropdown:hover .dropdown-content {
        display: block;
    }
    
    .dropdown-toggle::after {
        content: " ▼";
        font-size: 0.7em;
    }
    
    nav ul li a:hover {
        color: #a5d6a7;
    }
</style>