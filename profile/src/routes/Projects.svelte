

  <script lang ="ts">
	let projects = [
		{
			title: 'project1',
			description: 'BLA bla bla1',
			link: 'path'
		},
		 {
			title: 'project2',
			description: 'BLA bla bla2',
			link: 'path'
		},
		 {
			title: 'project3',
			description: 'BLA bla bla3',
			link: 'path'
		}
    ];
	let index= 0;

function handleChangee(e){
	index = e.target.value
}


</script>



<select class ="custom-select"  on:change={handleChangee}  >
	{#each projects as project , id} 

<option class ="projs" value={id}>{project.title}</option>

{/each}
</select>    

<h2 > <strong>=:{projects[index].description}</strong></h2>



<style>


	  /* Style for the select element */
	  .custom-select {
    display: inline-block;
    position: relative;
    width: 100px; /* Adjust the width as needed */
    font-family: Arial, sans-serif;
    font-size: 16px;
    color: #333;
    border: 1px solid #ccc;
    border-radius: 50px;
    padding: 8px;
	
    background-color: #fff;
    appearance: none; /* Hides default arrow in modern browsers */
    -webkit-appearance: none; /* Hides default arrow in older WebKit browsers */
    -moz-appearance: none; /* Hides default arrow in older Firefox */
  }

  /* Style for the select arrow */
  .custom-select::after {
    content: '▼'; /* Arrow character */
    position: absolute;
    top: 50%;
	transform: translateY(-50%);
    right: 10px;
   
    pointer-events: none; /* Ensures click events pass through */
  }

  
  

  /* Show the dropdown options when the select is clicked */
  
  
  h2 {
    font-family: Arial, sans-serif;
    font-size: 24px; /* Adjust the font size as needed */
    color: #333;
    margin-bottom: 20px; /* Adjust the margin as needed */
    border-bottom: 2px solid #ccc; /* Optional: Adding a bottom border */
    padding-bottom: 8px; /* Optional: Adding padding for separation */
  }
</style>