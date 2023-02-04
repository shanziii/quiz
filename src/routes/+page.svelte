<script>
    //Javascrip code goes here
    import img from '$lib/images/quizLogo.jpg';
    let name = "";
    let age = 0; 
    let persons=["John", "Lisa", "Karen"];

    let width = 200;
    let height = 200;

    
</script>

<!-- HTML Coding goes here-->

<div>
    <p>Enter Photo Width:</p>
    <input type="number" bind:value={width}/>

    <p>Enter Photo Height:</p>
    <input type="number" bind:value={height}/>

    {#if width<400} 
        <img id="logoimage" src={img} alt="logo" {width} height={height} />
    {:else}
        <p>Photo Width too large</p>
    {/if}

</div>
<div>
    Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
</div>
<div>   
    <p style="font-size: large; color:blueviolet;"><b>Welcome {name} To My Quiz</b></p>
    
    {#if age<18 }       <!--If statement in HTML for Svelte-->
     <p>You are underage!</p>
    {:else if age>90}
     <p>You are too old!</p>
    {:else}
     <p>You meet the age requirement!</p>
    {/if}

</div>

<div>
    <p>Enter Your Name:</p>
    <input type="text" bind:value={name}/>

    <p>Enter Your Age:</p>
    <input type="number" bind:value={age}/>
    {#each persons as person}   <!--Looping through an array to display its contents-->
    <h1>{person}</h1>
    {/each}
  <!--  <button id="startbtn"> Start Quiz</button> -->
</div>