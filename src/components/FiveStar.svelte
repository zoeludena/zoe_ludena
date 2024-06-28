<script>

  export let message = "Expert, I love these tools!";

</script>
  
  <div class="rating">
    <span title={message}>&#9733;</span>
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
  </style>
  