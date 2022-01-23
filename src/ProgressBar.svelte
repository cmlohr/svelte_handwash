<script>
    export let progress = 0;
    
</script>

<style>.progress-container{
    margin: 20px 0; 
    border: solid #0e8ce1;
    border-radius: 5px;
    
} 
.progress-bar {
    height: 10px; 
    width:10%; 
    background-color: #0e8ce1;
   
}
    </style>

<div bp="grid">
<div bp="offset-5@md 4@md 12@sm" class="progress-container">
<div class="progress-bar" style="width: {progress}%;">
<span class="sr-only">{progress}%</span>
</div>
</div>
</div>
