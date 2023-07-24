<script>
    import { i, language, switchLanguage } from '@inlang/sdk-js'
  
    let lang = language
  
    lang = lang === 'de' ? 'en' : 'de'
  
    async function switchLang() {
      switchLanguage(lang)
    }

    const buttonHandle = () => {
        window.open(
            'https://inlang.com/editor/github.com/vytenisstaugaitis/cms-json-inlang?lang=en&lang=de',
            '_blank'
        );
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

<button on:click={buttonHandle}>
    {i('header.edit_this_page')}
</button>