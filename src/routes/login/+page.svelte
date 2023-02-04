<script lang="ts" >
	import Layout from "../+layout.svelte";
    let username = "";
    let password = ""; 

    function submit(password: string){
        
        if(password.length<8){
            alert("NB: Password cannot be less than 8 characters!")
        }else{

            alert("Your password " + password + " is acceptible!");
        }

    }

</script>

<body>

    <div class="d-flex flex-column justify-content-center w-600 h-800">
        <form>
                <label for="username"> Username:</label> <br>
                <input type="text" bind:value={username}/><br>
    
                <label for="password"> Password:</label> <br>
                <input type="password" bind:value={password}/><br><br>

                <button type="submit" on:click={submit(password)}>Login</button>
    
        </form>
        
    </div>

    <div style="background-color:white; ">
        <!-- svelte-ignore empty-block -->
        {#if username == ""}     
               
        {:else}
            <h1 style="color:black;"> Welcome {username}</h1>

        {/if}

    </div>
</body>


