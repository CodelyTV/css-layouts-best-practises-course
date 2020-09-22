<template>
  <header class="header">
    <nav class="nav">
      <nuxt-link to="/">
        <img
          class="nav-logo"
          src="~/assets/images/logo-codelytv.png"
          alt="CodelyTV"
        />
      </nuxt-link>

      <button aria-label="Ver menú" class="burger">
        <Burger />
      </button>
      <ul class="nav-menu">
        <li v-for="link in links" :key="link.name">
          <a v-bind="link.attributes">{{ link.name }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.header {
  position: sticky;
  top: 0;
  width: 100%;
  background: var(--dark-color);
  box-shadow: 0 0 1rem var(--dark-color);
}

.nav {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 1rem;
}
.nav-logo {
  display: block;
  max-width: 15rem;
  margin-top: 0.2rem;
  padding: 0.2rem;
}
.nav > a:focus .nav-logo {
  outline: 2px solid var(--primary-color);
}
.nav-menu {
  display: none;
  flex-wrap: wrap;
  margin: 0;
  margin-left: auto;
  padding: 0;
  column-gap: 1rem;
  list-style: none;
}
.nav-menu a {
  color: #eee;
  white-space: nowrap;
  text-decoration: none;
}
.nav-menu a:hover,
.nav-menu a:focus {
  border-bottom: 2px solid var(--primary-color);
  outline: none;
}
.burger {
  width: 2rem;
  height: 2rem;
  margin: 0;
  margin-left: auto;
  padding: 0.1rem;
  color: #fff;
  background: transparent;
  border: none;
}
@media (min-width: 50rem) {
  .burger {
    display: none;
  }
  .nav-menu {
    display: flex;
  }
}
</style>

<script>
import Burger from '~/assets/images/burger.svg'

export default {
  components: {
    Burger,
  },
  data() {
    return {
      links: [
        {
          name: 'Cursos',
          attributes: {
            href: 'https://codely.tv/pro/cursos',
            rel: 'noopener',
          },
        },
        {
          name: 'Empresas',
          attributes: {
            href: 'https://codely.tv/pro/teams',
            rel: 'noopener',
          },
        },
        {
          name: 'Comunidades',
          attributes: {
            href: 'https://codely.tv/pro/comunidades',
            title: 'Patrocinio comunidades de desarrollo',
            rel: 'noopener',
          },
        },
        {
          name: 'YouTube',
          attributes: {
            href:
              'https://www.youtube.com/CodelyTV?utm_source=home&amp;utm_medium=landing&amp;utm_campaign=internal&amp;utm_content=header-menu',
            rel: 'nofollow noopener',
            target: '_blank',
          },
        },
        {
          name: 'Blog',
          attributes: {
            href: 'https://codely.tv/blog',
            rel: 'noopener',
          },
        },
        {
          name: 'Contacta',
          attributes: {
            href: 'mailto:soporte@codely.tv?Subject=[CodelyTV] Contacto web',
            rel: 'nofollow noopener',
          },
        },
        {
          name: 'Inicia sesión',
          attributes: {
            href:
              'https://pro.codely.tv/auth/sign-in/?utm_source=home&amp;utm_medium=landing&amp;utm_campaign=internal&amp;utm_content=header-menu',
            rel: 'nofollow noopener',
          },
        },
        {
          name: 'Suscríbete',
          attributes: {
            href: 'https://codely.tv//pro/cursos',
            rel: 'noopener',
          },
        },
      ],
    }
  },
}
</script>
