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
    .rating {
      unicode-bidi: bidi-override;
      direction: rtl;
      text-align: center;
    }
    .rating span {
      padding: 0 0.2em;
      font-size: 1.5em;

      color: #FFCC33;
    }
    .rating span.gold {
      color: #aaa;
    }
  </style>
  