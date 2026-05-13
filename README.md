import { useState } from 'react';

export default function TokoOnline() { const [showAuth, setShowAuth] = useState(false); const [isLogin, setIsLogin] = useState(true); const products = [ { name: 'Paid Edit JJ Soft Spoken', price: 'Rp1.000 - Rp5.000', image: 'https://images.unsplash.com/photo-1492691527719-9d1e07e534b4?q=80&w=1200&auto=format&fit=crop' }, { name: 'Paid Edit Seleksi', price: 'Rp15.000 - Rp30.000', image: 'https://images.unsplash.com/photo-1516321318423-f06f85e504b3?q=80&w=1200&auto=format&fit=crop' }, { name: 'Mega Collab Simpel', price: 'Rp10.000', image: 'https://images.unsplash.com/photo-1521737604893-d14cc237f11d?q=80&w=1200&auto=format&fit=crop' }, { name: 'Mega Collab Drop', price: 'Rp20.000', image: 'https://images.unsplash.com/photo-1519389950473-47ba0277781c?q=80&w=1200&auto=format&fit=crop' }, { name: 'Mega Collab JJ x 3D', price: 'Rp30.000', image: 'https://images.unsplash.com/photo-1498050108023-c5249f4df085?q=80&w=1200&auto=format&fit=crop' }, { name: 'Buy CC HD', price: 'Rp5.000', image: 'https://images.unsplash.com/photo-1545239351-1141bd82e8a6?q=80&w=1200&auto=format&fit=crop' }, { name: 'Buy Watermark Bebas Req', price: 'Rp5.000', image: 'https://images.unsplash.com/photo-1558655146-d09347e92766?q=80&w=1200&auto=format&fit=crop' } ];

return ( <> {showAuth && ( <div className="fixed inset-0 bg-black/70 backdrop-blur-sm flex items-center justify-center z-[100] px-4"> <div className="bg-zinc-900 border border-white/10 rounded-3xl w-full max-w-md p-8 relative shadow-2xl"> <button onClick={() => setShowAuth(false)} className="absolute top-4 right-4 text-gray-400 hover:text-white text-xl" > ✕ </button>

<h2 className="text-3xl font-bold mb-2 text-center">
          {isLogin ? 'Login Account' : 'Create Account'}
        </h2>

        <p className="text-gray-400 text-center mb-8">
          {isLogin
            ? 'Masuk ke akun toko kamu'
            : 'Daftar akun baru sekarang'}
        </p>

        <div className="space-y-4">
          {!isLogin && (
            <input
              type="text"
              placeholder="Username"
              className="w-full bg-black/40 border border-white/10 rounded-2xl px-5 py-4 outline-none focus:border-purple-500"
            />
          )}

          <input
            type="email"
            placeholder="Email"
            className="w-full bg-black/40 border border-white/10 rounded-2xl px-5 py-4 outline-none focus:border-purple-500"
          />

          <input
            type="password"
            placeholder="Password"
            className="w-full bg-black/40 border border-white/10 rounded-2xl px-5 py-4 outline-none focus:border-purple-500"
          />

          <button className="w-full bg-purple-600 hover:bg-purple-700 py-4 rounded-2xl font-semibold transition">
            {isLogin ? 'Login' : 'Register'}
          </button>
        </div>

        <p className="text-center text-gray-400 mt-6">
          {isLogin ? 'Belum punya akun?' : 'Sudah punya akun?'}{' '}
          <button
            onClick={() => setIsLogin(!isLogin)}
            className="text-purple-400 hover:text-purple-300"
          >
            {isLogin ? 'Register' : 'Login'}
          </button>
        </p>
      </div>
    </div>
  )}

  <div className="min-h-screen bg-black text-white font-sans">
<div className="min-h-screen bg-black text-white font-sans">
  <header className="flex items-center justify-between px-8 py-5 border-b border-white/10 backdrop-blur-md sticky top-0 bg-black/70 z-50">
    <h1 className="text-2xl font-bold tracking-wide">DANZ EDITS</h1>
    <div className="flex items-center gap-5">
      <nav className="flex gap-6 text-sm">
      <a href="#produk" className="hover:text-purple-400 transition">Produk</a>
      <a href="#tentang" className="hover:text-purple-400 transition">Tentang</a>
      <a href="#kontak" className="hover:text-purple-400 transition">Kontak</a>
    </nav>

      <button
        onClick={() => setShowAuth(true)}
        className="bg-purple-600 hover:bg-purple-700 px-5 py-2 rounded-xl text-sm font-semibold transition"
      >
        Login
      </button>
    </div>
  </header>

  <section className="px-8 md:px-16 py-20 grid md:grid-cols-2 gap-10 items-center">
    <div>
      <p className="text-purple-400 mb-3 uppercase tracking-[4px] text-sm">Welcome To</p>
      <h2 className="text-5xl md:text-7xl font-black leading-tight mb-6">
        TOKO <span className="text-purple-500">ONLINE</span>
      </h2>
      <p className="text-gray-300 text-lg mb-8 max-w-xl">
        Website jasa edit modern dengan tampilan aesthetic, cocok untuk jual jasa edit video, foto, desain, preset, dan konten sosial media.
      </p>

      <div className="flex gap-4">
        <button className="bg-purple-600 hover:bg-purple-700 px-6 py-3 rounded-2xl font-semibold transition shadow-lg shadow-purple-500/20">
          Belanja Sekarang
        </button>

        <button className="border border-white/20 hover:border-purple-500 px-6 py-3 rounded-2xl font-semibold transition">
          Lihat Produk
        </button>
      </div>
    </div>

    <div className="relative">
      <img
        src="https://images.unsplash.com/photo-1523398002811-999ca8dec234?q=80&w=1200&auto=format&fit=crop"
        alt="fashion"
        className="rounded-3xl shadow-2xl object-cover h-[500px] w-full"
      />

      <div className="absolute -bottom-6 -left-6 bg-purple-600 px-6 py-4 rounded-2xl shadow-xl">
        <p className="text-sm text-white/80">Produk Terjual</p>
        <h3 className="text-3xl font-bold">1.2K+</h3>
      </div>
    </div>
  </section>

  <section id="produk" className="px-8 md:px-16 py-16">
    <div className="flex items-center justify-between mb-10">
      <h2 className="text-4xl font-bold">Layanan Populer</h2>
      <p className="text-gray-400">Top Services</p>
    </div>

    <div className="grid sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
      {products.map((item, index) => (
        <div
          key={index}
          className="bg-white/5 border border-white/10 rounded-3xl overflow-hidden hover:scale-[1.02] transition duration-300 shadow-lg"
        >
          <div className="h-40 w-full bg-gradient-to-br from-purple-700 to-black flex items-center justify-center text-center px-4">
            <h3 className="text-2xl font-bold text-white">{item.name}</h3>
          </div>

          <div className="p-6">
            <h3 className="text-2xl font-semibold mb-2 text-center">{item.name}</h3>
            <p className="text-purple-400 text-lg mb-5">{item.price}</p>

            <a
              href={`https://wa.me/62882016327769?text=${encodeURIComponent('Min mau buy')}`}
              target="_blank"
              rel="noopener noreferrer"
              className="block text-center w-full bg-green-600 hover:bg-green-700 py-3 rounded-2xl font-semibold transition"
            >
              Pesan via WhatsApp
            </a>
          </div>
        </div>
      ))}
    </div>
  </section>

  <section id="tentang" className="px-8 md:px-16 py-20">
    <div className="bg-white/5 border border-white/10 rounded-3xl p-10 text-center">
      <h2 className="text-4xl font-bold mb-5">Tentang Toko</h2>
      <p className="text-gray-300 max-w-3xl mx-auto text-lg leading-relaxed">
        DANZ EDITS menyediakan produk fashion modern dengan kualitas premium dan desain kekinian. Cocok untuk anak muda yang suka style aesthetic dan streetwear.
      </p>
    </div>
  </section>

  <footer id="kontak" className="border-t border-white/10 px-8 md:px-16 py-10 text-center text-gray-400">
    <h3 className="text-2xl font-bold text-white mb-3">DANZ EDITS</h3>
    <p>Instagram: @danzedits</p>
    <p>WhatsApp: 08xxxxxxxxxx</p>
    <p className="mt-5 text-sm text-gray-500">© 2026 DANZ EDITS. All rights reserved.</p>
  </footer>
  </div>
</>
</div>

); }
