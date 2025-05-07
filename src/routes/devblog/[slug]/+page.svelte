<!-- src/routes/devblog/[slug]/+page.svelte -->
<script>
    /** @type {import('./$types').PageData} */
    export let data;
  </script>
  
  <article class="prose">
    <h1>{data.title}</h1>
    <p>Published: {data.date}</p>
    <svelte:component this={data.content} />
  </article>

  <style>
    article {
      max-width: 800px;
      margin: 0 auto;
      padding: 1rem;
      background: linear-gradient(-45deg, #c609c6, #6a5959);
    }

  </style>