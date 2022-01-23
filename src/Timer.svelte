<script>
import ProgressBar from "./ProgressBar.svelte";
// import ProgressBar from '@okrad/svelte-progressbar';
const totalSeconds = 20;
let secondLeft = totalSeconds;
let timerRunning = false;
$: progress = ((totalSeconds - secondLeft) / totalSeconds) * 100;

function start(){
timerRunning = true;

const timer = setInterval(() => {
    secondLeft-=1;
    if (secondLeft == 0) {
        clearInterval(timer);
        timerRunning = false;
        secondLeft = totalSeconds;
    } 
    }, 1000);

}








</script>

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
    .start[disabled] {
        background-color: #ccc;
        cursor: not-allowed;
    }
</style>
<div bp="grid">
    <h2 bp="offset-5@md 4@md 12@sm">Seconds Left: {secondLeft}</h2>
    </div>  

   
<ProgressBar style=radial {progress}/>
<div bp="grid">
<button disabled={timerRunning} bp="offset-5@md 4@md 12@sm" id="class" class="start" on:click={start} >Start</button>
</div>   