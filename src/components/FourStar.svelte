<script>
    export let message = "Advanced, very comfortable using!";
  </script>
  
  <div class="rating">
    <span class="gold" title={message}>&#9733;</span>
    <span title={message}>&#9733;</span>
    <span title={message}>&#9733;</span>
    <span title={message}>&#9733;</span>
    <span title={message}>&#9733;</span>
  </div>
  
  <style>
    .rating span {
      font-size: 1.5em;
      color: #FFCC33;
    }
    .gold {
      color: #aaa;
    }
  </style>
  