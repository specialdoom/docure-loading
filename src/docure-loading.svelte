<svelte:options tag="docure-loading" />

<script>
  export let text = "";
</script>

<svg id="loading" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 78.2 105.5">
  <path class="cls-1" d="M229.1,304.5a6.5,6.5,0,0,1,0-13,39.3,39.3,0,0,0,0-78.5h-12v26.8h11.2a6.5,6.5,0,0,1,0,13H210.6a6.6,6.6,0,0,1-6.5-6.5V206.5a6.5,6.5,0,0,1,6.5-6.5h18.5a52.3,52.3,0,0,1,0,104.5Z" transform="translate(-203.6 -199.5)"/>
  <path class="cls-2" d="M228.3,283.8a6.5,6.5,0,0,1-6.5-6.5V227.2a6.5,6.5,0,0,1,13,0v50.1A6.5,6.5,0,0,1,228.3,283.8Z" transform="translate(-203.6 -199.5)"/>
  <circle class="cls-2" cx="47.3" cy="46.7" r="8.4"/>
</svg>
<span>{text}</span>

<style>
  :host {
    height: 100px;
    width: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  svg {
    height: 100px;
    margin-bottom: 4px;
  }

  .cls-1,.cls-2{fill:none;stroke-miterlimit:10;}
  .cls-1{stroke:#de4939;}
  .cls-2{stroke:#578cc9;}

  path{
    stroke-dasharray: 100;
    animation: draw 2s infinite;
  }
  
  @keyframes draw {
    from {
      stroke-dashoffset:0;
    } 
    to {
      stroke-dashoffset:200;
    }
  }
</style>