---
import Layout from '~/layouts/PageLayout.astro';

import Header from '~/components/widgets/Header.astro';
import Hero2 from '~/components/widgets/Hero2.astro';
import Features from '~/components/widgets/Features.astro';
import Steps2 from '~/components/widgets/Steps2.astro';
import Content from '~/components/widgets/Content.astro';

import { headerData } from '~/navigation';
import FAQs from '~/components/widgets/FAQs.astro';
import BlogLatestPosts from '~/components/widgets/BlogLatestPosts.astro';

const metadata = {
  title: 'Receita Grátis - Saúde e Culinária Natural',
};
---

<Layout metadata={metadata}>
  <Fragment slot="header">
    <Header
      {...headerData}
      actions={[
        {
          variant: 'primary',
          text: 'Ver Receitas',
          href: '#blog',
        },
      ]}
      isSticky
    />
  </Fragment>

  <!-- Hero Principal: Foco na Série Cura Natureza -->

  <Hero2
    tagline="Portal Receita Grátis"
    actions={[
      { variant: 'primary', text: 'Começar Agora', href: '#blog' },
      { text: 'Saber Mais', href: '#features' },
    ]}
    image={{
      src: 'https://images.unsplash.com/photo-1512621776951-a57141f2eefd?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80',
      alt: 'Alimentos Saudáveis e Naturais',
    }}
  >
    <Fragment slot="title">
      Transforme sua saúde com a <br /> série <span class="text-accent dark:text-white">Cura Natureza</span><br />
    </Fragment>

    <Fragment slot="subtitle">
      Descubra o poder dos alimentos funcionais e receitas práticas que nutrem o corpo e a alma. 
      Liderado por <span class="font-semibold">Anderson Kochanski</span>, o portal combina tradição e bem-estar.
    </Fragment>
  </Hero2>

  <!-- Diferenciais do Portal -->

  <Features
    id="features"
    title="Por que seguir o Receita Grátis?"
    subtitle="Unimos praticidade na cozinha com os segredos da medicina natural."
    columns={2}
    items={[
      {
        title: 'Série Cura Natureza',
        description:
          'Conteúdos exclusivos sobre como utilizar ervas, raízes e alimentos integrais como aliados da sua saúde.',
        icon: 'tabler:leaf',
      },
      {
        title: 'Mais de 15 mil Receitas',
        description: `Um acervo completo que vai do café da manhã ao jantar, sempre focando em ingredientes acessíveis.`,
        icon: 'tabler:ToolsKitchen2',
      },
      {
        title: 'Foco em Bem-estar',
        description:
          'Não é apenas sobre comer, é sobre viver melhor. Dicas de hábitos saudáveis para toda a família.',
        icon: 'tabler:heart-plus',
      },
      {
        title: 'Leitura Rápida e Limpa',
        description: `Portal otimizado para carregar instantaneamente no seu celular, facilitando a consulta enquanto você cozinha.`,
        icon: 'tabler:device-mobile',
      },
    ]}
  />

  <!-- Seção de Conteúdo: Exemplos de Uso (Receitas e Saúde) -->

  <Content
    title="O que você encontrará aqui"
    subtitle="Explore as diferentes vertentes do nosso portal focado em uma vida mais plena."
    isReversed
    items={[
      {
        title: 'Alimentação como Remédio:',
        description:
          'Entenda como ingredientes simples do seu dia a dia podem ajudar a prevenir doenças e aumentar sua imunidade através da série Cura Natureza.',
      },
      {
        title: 'Benefícios:',
        description: `Receitas testadas e aprovadas. <br /> Guia de substituições saudáveis. <br /> Explicações claras sobre os benefícios de cada alimento.`,
      },
    ]}
    image={{
      src: 'https://images.unsplash.com/photo-1540420773420-3366772f4999?ixlib=rb-4.0.3&auto=format&fit=crop&w=1671&q=80',
      alt: 'Salada Saudável',
    }}
  >
    <Fragment slot="content">
      <h3 class="text-2xl font-bold tracking-tight dark:text-white sm:text-3xl mb-2">
        Cozinha Funcional: <br /><span class="text-2xl">Saúde no seu prato</span>
      </h3>
    </Fragment>
  </Content>

  <!-- FAQs do Portal -->

  <FAQs
    title="Dúvidas Frequentes"
    items={[
      {
        title: 'As receitas são realmente gratuitas?',
        description:
          'Sim! Todo o conteúdo do portal Receita Grátis é aberto ao público, financiado através de nossos parceiros e anúncios não invasivos.',
        icon: 'tabler:chevrons-right',
      },
      {
        title: 'O conteúdo da série Cura Natureza tem base técnica?',
        description: `Sim, Anderson Kochanski preza pela curadoria de informações baseadas em conhecimentos tradicionais e estudos sobre alimentos funcionais.`,
        icon: 'tabler:chevrons-right',
      },
      {
        title: 'Posso sugerir uma receita ou tema?',
        description:
          'Com certeza! Adoramos ouvir nossos leitores. Você pode entrar em contato conosco através de nossas redes sociais ou e-mail.',
        icon: 'tabler:chevrons-right',
      },
    ]}
  />

  <!-- Contato/Redes Sociais -->

  <Steps2
    title="Acompanhe nossas novidades"
    subtitle="Fique por dentro de cada nova receita e capítulo da série Cura Natureza."
    items={[
      {
        title: 'Siga-nos',
        description: '@receitagratis',
        icon: 'tabler:brand-instagram',
      },
      {
        title: 'Localização',
        description: 'Telêmaco Borba, PR',
        icon: 'tabler:map-pin',
      },
    ]}
  />

  <!-- Últimas Postagens do Blog (Receitas) -->

  <BlogLatestPosts
    id="blog"
    title="Últimas Receitas e Dicas de Saúde"
    information={`Explore nosso blog para encontrar as receitas mais recentes e guias detalhados sobre saúde natural.`}
  />
</Layout>
