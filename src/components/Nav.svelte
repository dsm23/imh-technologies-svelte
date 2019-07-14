<script>
  import { ROUTER } from '../constants';

	export let segment;

  let isOpen = false;

  const handleToggle = () => {
    isOpen = !isOpen;
  }

  const close = () => {
    isOpen = false;
  }

  const arrNav = [
    // {href: ROUTER.HOME, label: 'Home'},
    {href: ROUTER.ABOUT, label: 'About'},
    {href: ROUTER.CONTACT, label: 'Contact'},
    {href: ROUTER.NEWS_AND_EVENTS, label: 'News and Events'},
    {href: ROUTER.TECHNICAL_HELP, label: 'Technical Help'},
    {href: ROUTER.PRODUCTS_AND_SERVICES, label: 'Products and Services'},
  ];
</script>

<nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <a class="navbar-brand" href={ROUTER.HOME}>IMH Technologies Ltd.</a>
  <button
    class="navbar-toggler"
    on:click={handleToggle}
    type="button"
    data-toggle="collapse"
    data-target="#navbarColor01"
    aria-controls="navbarColor01"
    aria-expanded={isOpen}
    aria-label="Toggle navigation"
  >
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class:collapse={!isOpen} class="navbar-collapse" id="navbarColor01">
    <ul class="navbar-nav ml-auto">
      <li class='nav-item'>
        <a class="nav-link" class:active={ !segment } href={ROUTER.HOME}>
          Home <span class="sr-only">(current)</span>
        </a>
      </li>
      {#each arrNav as { href, label }}
        <li class="nav-item" on:click={close}>
          <a class="nav-link" class:active={segment === href} href={href}>
            {label} {#if segment === href}<span class="sr-only">(current)</span>{/if}
          </a>
        </li>
      {/each}
		</ul>
  </div>
</nav>