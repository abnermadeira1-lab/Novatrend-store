import { motion } from 'framer-motion'; import { Sparkles, ShoppingCart, MessageCircleMore, Zap } from 'lucide-react';

export default function DropShippingStore() { const products = [ { name: 'Smartwatch Ultra X', price: 'R$ 299,90', image: 'https://images.unsplash.com/photo-1523275335684-37898b6baf30?q=80&w=1200&auto=format&fit=crop' }, { name: 'Fone Bluetooth Pro', price: 'R$ 149,90', image: 'https://images.unsplash.com/photo-1505740420928-5e560c06d30e?q=80&w=1200&auto=format&fit=crop' }, { name: 'Mini Projetor HD', price: 'R$ 399,90', image: 'https://images.unsplash.com/photo-1516321318423-f06f85e504b3?q=80&w=1200&auto=format&fit=crop' }, { name: 'Câmera Inteligente WiFi', price: 'R$ 249,90', image: 'https://images.unsplash.com/photo-1516035069371-29a1b244cc32?q=80&w=1200&auto=format&fit=crop' } ];

return ( <div className="min-h-screen bg-zinc-950 text-white overflow-hidden"> <div className="fixed inset-0 opacity-20 pointer-events-none"> <div className="absolute top-0 left-0 w-96 h-96 bg-indigo-500 rounded-full blur-3xl animate-pulse" /> <div className="absolute bottom-0 right-0 w-96 h-96 bg-purple-500 rounded-full blur-3xl animate-pulse" /> </div> <header className="sticky top-0 z-50 backdrop-blur-xl bg-black/50 border-b border-zinc-800"> <div className="max-w-7xl mx-auto flex items-center justify-between px-6 py-4"> <h1 className="text-2xl font-bold tracking-tight">NovaTrend</h1>

<nav className="hidden md:flex gap-8 text-sm text-zinc-300">
        <a href="#inicio" className="hover:text-white transition shadow-2xl shadow-indigo-500/10">Início</a>
        <a href="#produtos" className="hover:text-white transition shadow-2xl shadow-indigo-500/10">Produtos</a>
        <a href="#beneficios" className="hover:text-white transition shadow-2xl shadow-indigo-500/10">Benefícios</a>
        <a href="#contato" className="hover:text-white transition shadow-2xl shadow-indigo-500/10">Contato</a>
      </nav>

      <button className="bg-white text-black px-5 py-2 rounded-2xl font-semibold hover:scale-105 transition shadow-2xl shadow-indigo-500/10">
        Comprar Agora
      </button>
    </div>
  </header>

  <section
    id="inicio"
    className="relative overflow-hidden"
  >
    <div className="absolute inset-0 bg-gradient-to-br from-indigo-700/30 via-purple-700/10 to-transparent blur-3xl" />

    <motion.div
      initial={{ opacity: 0, y: 50 }}
      animate={{ opacity: 1, y: 0 }}
      transition={{ duration: 1 }}
      className="max-w-7xl mx-auto grid md:grid-cols-2 gap-10 items-center px-6 py-24 relative z-10"
    >
      <div>
        <span className="bg-white/10 border border-white/10 px-4 py-2 rounded-full text-sm text-zinc-300">
          Loja Premium de Dropshipping
        </span>

        <h2 className="text-5xl md:text-7xl font-black mt-6 leading-tight">
          Produtos Virais
          <span className="block text-indigo-400">Que Vendem Todos os Dias</span>
        </h2>

        <p className="text-zinc-400 mt-6 text-lg leading-relaxed max-w-xl">
          Monte sua marca com produtos modernos, entrega rápida e uma experiência premium para seus clientes.
        </p>

        <div className="flex gap-4 mt-8 flex-wrap">
          <button className="bg-indigo-500 hover:bg-indigo-400 px-7 py-4 rounded-2xl font-bold transition shadow-2xl shadow-indigo-500/20">
            Explorar Produtos
          </button>

          <button className="border border-zinc-700 hover:border-white px-7 py-4 rounded-2xl font-bold transition shadow-2xl shadow-indigo-500/10">
            Ver Catálogo
          </button>
        </div>
      </div>

      <div className="relative">
        <img
          src="https://images.unsplash.com/photo-1556740749-887f6717d7e4?q=80&w=1400&auto=format&fit=crop"
          alt="Store"
          className="rounded-3xl shadow-2xl border border-zinc-800"
        />

        <div className="absolute -bottom-8 -left-8 bg-zinc-900 border border-zinc-800 p-5 rounded-3xl shadow-2xl">
          <p className="text-zinc-400 text-sm">Pedidos Hoje</p>
          <h3 className="text-3xl font-bold">+1.284</h3>
        </div>
      </div>
    </motion.div>
  </section>

  <section id="beneficios" className="max-w-7xl mx-auto px-6 py-20">
    <div className="grid md:grid-cols-3 gap-6">
      {[
        {
          title: 'Entrega Rápida',
          desc: 'Integração com fornecedores internacionais e rastreamento em tempo real.'
        },
        {
          title: 'Pagamento Seguro',
          desc: 'Checkout moderno com PIX, cartão e proteção antifraude.'
        },
        {
          title: 'Design Premium',
          desc: 'Experiência profissional focada em conversão e vendas.'
        }
      ].map((item, index) => (
        <motion.div
          initial={{ opacity: 0, y: 40 }}
          whileInView={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.6, delay: index * 0.2 }}
          viewport={{ once: true }}
          key={index}
          className="bg-zinc-900 border border-zinc-800 p-8 rounded-3xl hover:-translate-y-2 transition shadow-2xl shadow-indigo-500/10">
          <h3 className="text-2xl font-bold mb-4">{item.title}</h3>
          <p className="text-zinc-400 leading-relaxed">{item.desc}</p>
        </motion.div>
      ))}
    </div>
  </section>

  <section id="produtos" className="max-w-7xl mx-auto px-6 py-20 relative z-10">
    <div className="flex items-center justify-between mb-12 flex-wrap gap-4">
      <div>
        <h2 className="text-4xl font-black">Produtos em Alta</h2>
        <p className="text-zinc-400 mt-2">Escolhidos para maximizar conversão e lucro.</p>
      </div>

      <input
        type="text"
        placeholder="Pesquisar produto..."
        className="bg-zinc-900 border border-zinc-800 rounded-2xl px-5 py-3 outline-none focus:border-indigo-500"
      />
    </div>

    <div className="grid sm:grid-cols-2 lg:grid-cols-4 gap-8">
      {products.map((product, index) => (
        <motion.div
          initial={{ opacity: 0, scale: 0.9 }}
          whileInView={{ opacity: 1, scale: 1 }}
          transition={{ duration: 0.5, delay: index * 0.15 }}
          viewport={{ once: true }}
          key={index}
          whileHover={{ y: -10 }}
          className="bg-zinc-900 border border-zinc-800 rounded-3xl overflow-hidden hover:scale-[1.02] transition-all duration-300 shadow-xl hover:shadow-indigo-500/20"
        >
          <img
            src={product.image}
            alt={product.name}
            className="h-72 w-full object-cover"
          />

          <div className="p-6">
            <h3 className="text-xl font-bold">{product.name}</h3>
            <p className="text-indigo-400 text-2xl font-black mt-3">{product.price}</p>

            <div className="mt-6 space-y-3">
              <button className="w-full bg-white text-black py-3 rounded-2xl font-bold hover:opacity-90 transition shadow-2xl shadow-indigo-500/10">
                Comprar com Cartão
              </button>

              <button className="w-full bg-emerald-500 text-white py-3 rounded-2xl font-bold hover:bg-emerald-400 transition shadow-lg shadow-emerald-500/20">
                Pagar com PIX
              </button>
            </div>
          </div>
        </motion.div>
      ))}
    </div>
  </section>

  <section className="py-24 px-6">
    <div className="max-w-6xl mx-auto bg-gradient-to-r from-indigo-600 to-purple-600 rounded-[40px] p-12 text-center shadow-2xl relative overflow-hidden">
      <div className="absolute inset-0 opacity-20 animate-pulse bg-[radial-gradient(circle_at_top,_white,_transparent_60%)]" />
      <h2 className="text-5xl font-black leading-tight">
        Transforme Visitantes
        <span className="block">Em Clientes</span>
      </h2>

      <p className="text-lg text-white/80 mt-6 max-w-2xl mx-auto">
        Estrutura moderna com checkout integrado via PIX e cartão, focada em aumentar autoridade, conversão e escalabilidade.
      </p>

      <div className="flex justify-center gap-4 mt-8 flex-wrap">
        <div className="bg-white/10 border border-white/20 backdrop-blur-xl px-6 py-4 rounded-2xl animate-bounce">
          ⚡ PIX Instantâneo
        </div>

        <div className="bg-white/10 border border-white/20 backdrop-blur-xl px-6 py-4 rounded-2xl hover:scale-105 transition shadow-2xl shadow-indigo-500/10">
          💳 Cartão em até 12x
        </div>

        <div className="bg-white/10 border border-white/20 backdrop-blur-xl px-6 py-4 rounded-2xl animate-pulse">
          🤖 IA de Conversão
        </div>
      </div>

      <button className="mt-8 bg-white text-black px-8 py-4 rounded-2xl font-bold hover:scale-105 transition shadow-2xl shadow-indigo-500/10">
        Começar Agora
      </button>
    </div>
  </section>

  <section className="max-w-7xl mx-auto px-6 pb-24">
    <div className="bg-zinc-900 border border-zinc-800 rounded-[40px] p-10 relative overflow-hidden">
      <div className="absolute right-0 top-0 h-full w-1/2 bg-gradient-to-l from-indigo-500/10 to-transparent" />

      <div className="relative z-10 grid md:grid-cols-2 gap-10 items-center">
        <div>
          <span className="bg-indigo-500/10 text-indigo-300 px-4 py-2 rounded-full text-sm border border-indigo-500/20">
            IA de Vendas Integrada
          </span>

          <h2 className="text-4xl font-black mt-6 leading-tight">
            Assistente Inteligente
            <span className="block text-indigo-400">Para Converter Mais</span>
          </h2>

          <p className="text-zinc-400 mt-6 leading-relaxed text-lg">
            Chat automatizado com inteligência artificial para responder clientes, recomendar produtos e aumentar conversões em tempo real.
          </p>
        </div>

        <div className="bg-black/40 border border-zinc-800 rounded-3xl p-6 backdrop-blur-xl shadow-2xl">
          <div className="space-y-4">
            <div className="bg-zinc-800 rounded-2xl p-4 w-fit max-w-xs animate-pulse">
              Olá 👋 Posso ajudar você a escolher o melhor produto?
            </div>

            <div className="bg-indigo-500 rounded-2xl p-4 w-fit ml-auto max-w-xs">
              Quero um smartwatch premium.
            </div>

            <div className="bg-zinc-800 rounded-2xl p-4 w-fit max-w-xs animate-pulse">
              Recomendamos o Smartwatch Ultra X com entrega rápida 🚀
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section className="max-w-6xl mx-auto px-6 py-24">
    <motion.div
      initial={{ opacity: 0, y: 50 }}
      whileInView={{ opacity: 1, y: 0 }}
      transition={{ duration: 0.8 }}
      viewport={{ once: true }}
      className="bg-zinc-900 border border-zinc-800 rounded-[40px] p-10 relative overflow-hidden"
    >
      <div className="absolute top-0 right-0 w-72 h-72 bg-indigo-500/20 blur-3xl rounded-full" />

      <div className="relative z-10 grid md:grid-cols-2 gap-10 items-center">
        <div>
          <div className="flex items-center gap-3 mb-5">
            <Sparkles className="text-indigo-400" />
            <span className="text-indigo-400 font-semibold uppercase tracking-widest text-sm">
              IA de Conversão
            </span>
          </div>

          <h2 className="text-5xl font-black leading-tight">
            Assistente Inteligente
            <span className="block text-indigo-400">Para Vender Mais</span>
          </h2>

          <p className="text-zinc-400 mt-6 text-lg leading-relaxed">
            Sistema automatizado de vendas com inteligência artificial para responder clientes, recomendar produtos e aumentar conversões em tempo real.
          </p>

          <div className="grid grid-cols-2 gap-4 mt-8">
            <div className="bg-black/40 border border-zinc-800 p-5 rounded-2xl">
              <ShoppingCart className="mb-3 text-indigo-400" />
              <h3 className="font-bold">Checkout Inteligente</h3>
            </div>

            <div className="bg-black/40 border border-zinc-800 p-5 rounded-2xl">
              <MessageCircleMore className="mb-3 text-indigo-400" />
              <h3 className="font-bold">Chat IA 24h</h3>
            </div>

            <div className="bg-black/40 border border-zinc-800 p-5 rounded-2xl">
              <Zap className="mb-3 text-indigo-400" />
              <h3 className="font-bold">Upsell Automático</h3>
            </div>

            <div className="bg-black/40 border border-zinc-800 p-5 rounded-2xl">
              <Sparkles className="mb-3 text-indigo-400" />
              <h3 className="font-bold">Recomendação IA</h3>
            </div>
          </div>
        </div>

        <div className="bg-black border border-zinc-800 rounded-3xl p-6 shadow-2xl">
          <div className="flex items-center gap-3 mb-6">
            <div className="w-3 h-3 bg-green-400 rounded-full animate-pulse" />
            <span className="text-sm text-zinc-400">IA Online</span>
          </div>

          <div className="space-y-4">
            <div className="bg-zinc-900 p-4 rounded-2xl text-zinc-300 max-w-sm">
              Olá 👋 Posso te ajudar a encontrar o produto ideal?
            </div>

            <div className="bg-indigo-500 p-4 rounded-2xl ml-auto max-w-sm text-white">
              Quero um smartwatch premium.
            </div>

            <div className="bg-zinc-900 p-4 rounded-2xl text-zinc-300 max-w-sm">
              Recomendamos o Smartwatch Ultra X com desconto exclusivo hoje 🚀
            </div>
          </div>
        </div>
      </div>
    </motion.div>
  </section>

  <footer id="contato" className="border-t border-zinc-800 py-12 px-6">
    <div className="max-w-7xl mx-auto grid md:grid-cols-3 gap-10">
      <div>
        <h3 className="text-2xl font-black">NovaTrend</h3>
        <p className="text-zinc-400 mt-4 leading-relaxed">
          Loja focada em produtos inovadores, tecnologia e tendências globais.
        </p>
      </div>

      <div>
        <h4 className="font-bold text-lg mb-4">Links</h4>
        <div className="flex flex-col gap-3 text-zinc-400">
          <a href="#">Início</a>
          <a href="#">Produtos</a>
          <a href="#">Política de Privacidade</a>
          <a href="#">Termos</a>
        </div>
      </div>

      <div>
        <h4 className="font-bold text-lg mb-4">Contato</h4>
        <p className="text-zinc-400">suporte@novatrend.com</p>
        <p className="text-zinc-400 mt-2">WhatsApp: (11) 99999-9999</p>
      </div>
    </div>

    <div className="text-center text-zinc-500 mt-12 text-sm">
      © 2026 NovaTrend — Todos os direitos reservados.
    </div>
  </footer>
</div>

); }
