<template>
  <footer class="footer">
    <ul class="footer-nav">
      <li v-for="link in links" :key="link.name">
        <a v-bind="link.attributes">{{ link.name }}</a>
      </li>
    </ul>
  </footer>
</template>

<style scoped>
.footer {
  background: var(--dark-color);
}
.footer-nav {
  display: flex;
  flex-wrap: wrap;
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 2rem 1rem;
  font-size: 0.8rem;
  text-transform: uppercase;
  column-gap: 1rem;
  list-style: none;
}
.footer-nav a {
  color: #fff;
  text-decoration: none;
}
.footer-nav a:hover,
.footer-nav a:focus {
  border-bottom: 2px solid var(--primary-color);
  outline: none;
}
</style>

<script>
export default {
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
      ],
    }
  },
}
</script>
