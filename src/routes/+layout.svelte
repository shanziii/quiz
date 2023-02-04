

<!-- CSS Styling extracted from codepen-->
<style> 
    body {
        background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
        background-size: 400% 400%;
        animation: gradient 15s ease infinite;
        height: 100vh;
    }

    @keyframes gradient {
        0% {
            background-position: 0% 50%;
        }
        50% {
            background-position: 100% 50%;
        }
        100% {
            background-position: 0% 50%;
        }
    }   

    nav{

        font-family: Georgia, 'Times New Roman', Times, serif;
        font-size: large;
        background-color: beige;
        padding-inline: 50px;
        float:inherit;
    }

</style> 
<body>
    <nav>
        <a href="/">Home Page</a>
        <a href="/login">Login Page</a>
        <a href="/quiz">Quiz Page</a>
        <a href="/results">Results Page</a>
    
    </nav>

<slot>

</slot>
</body>