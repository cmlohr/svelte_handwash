<script>import ProgressBar from "./ProgressBar.svelte";</script>

<style>
    h2 {
        margin: 0;
    }
    .start {
        	background-color: #0e9dc9;
	border-radius: 5px;
    transition:0.15s;
    width: 80%;
    margin: auto;
    padding: 10px;
    }
    .start:hover {
        background-color: #1086aa;
        transform: scale(.99);
    }
</style>
<div bp="grid">
    <h2 bp="offset-5@md 4@md 12@sm">Seconds Left:</h2>
    </div>  
<ProgressBar/>
<div bp="grid">
<button bp="offset-5@md 4@md 12@sm" class="start">Start</button>
</div>