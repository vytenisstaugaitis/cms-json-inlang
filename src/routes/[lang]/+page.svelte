<script>
    import { i } from '@inlang/sdk-js'
</script>

<h1>{i('home.title')}</h1>

<ul>
  {#each {length: 3} as _, index}
    <li>{i('home.about_list_'+index)}</li>
  {/each}
</ul>