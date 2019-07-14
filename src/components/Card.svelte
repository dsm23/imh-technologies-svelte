<script>
  export let href;
  export let title;
  export let text;
</script>

<div class="col-xl-3 col-lg-4 col-md-6 col-sm-12 card primary mb-3">
  <div class="card-body">
    <h4 class="card-title">{title}</h4>
    <p class="card-text">{text}</p>
    <a href={href} class="btn btn-primary">
      {title}
    </a>
  </div>
</div>