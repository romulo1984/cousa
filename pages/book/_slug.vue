<template>
  <article>
    <h1>{{ title }}</h1>
  </article>
</template>

<script>
  export default {
    async asyncData({ params }) {
      // const bookPromise = process.BROWSER_BUILD
      //   ? import('~/_content/books/' + params.slug + '.json')
      //   : Promise.resolve(
      //       require('~/_content/books/' + params.slug + '.json')
      //     );
      let book = await import('~/_content/books/' + params.slug + '.json');
      return book;
    }
  };
</script>
