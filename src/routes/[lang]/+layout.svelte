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

<ul>
    <li><a href="/{language}">{i('header.menu.home')}</a></li>
    <li><a href="/{language}/about">{i('header.menu.about')}</a></li>
</ul>

<slot />

<button on:click={switchLang}>
    {i('header.switchLang')} <span style="text-transform:uppercase">{lang}</span>
</button>