<script>
  import { i } from '@inlang/sdk-js'
  import { language } from "@inlang/sdk-js"
  import { switchLanguage } from "@inlang/sdk-js"

  let lang = language

  lang = lang === 'de' ? 'en' : 'de'

  async function switchLang() {
    switchLanguage(lang)
  }
</script>

<h1>{i('home.title')}</h1>

<ul>
  {#each {length: 3} as _, index}
    <li>{i('home.about_list_'+index)}</li>
  {/each}
</ul>

<button on:click={switchLang}>
  {i('header.switchLang')} <span style="text-transform:uppercase">{lang}</span>
</button>