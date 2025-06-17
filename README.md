import Image from "next/image";

export default function Home() {
  return (
    <div className="min-h-screen bg-gradient-to-r from-black via-[#0f0f4f] to-blue-800 text-white p-8">
      <header className="flex flex-col md:flex-row justify-between items-center mb-12">
        <h1 className="text-4xl md:text-5xl font-bold">Raye – Virtual Assistant 🔥</h1>
        <a href="#contact" className="mt-4 md:mt-0 bg-white text-blue-700 font-semibold px-4 py-2 rounded hover:bg-blue-100">Contactez-moi</a>
      </header>

      <section className="grid md:grid-cols-2 gap-8 mb-16">
        <div>
          <h2 className="text-3xl font-semibold mb-4">Qui suis-je ?</h2>
          <p className="text-lg">
            Je suis Raye, un Assistant Virtuel & Business Developer multi-compétent,
            passionné par le digital et la performance. Je vous accompagne dans la
            gestion, la communication et le développement de votre activité.
          </p>
        </div>
        <div className="flex items-center justify-center">
          <Image src="/profile.jpg" alt="Raye" width={256} height={256} className="rounded-2xl shadow-lg" />
        </div>
      </section>

      <section className="mb-16">
        <h2 className="text-3xl font-semibold mb-6">Mes Services</h2>
        <ul className="grid grid-cols-1 md:grid-cols-2 gap-4 text-lg">
          {[
            \"Marketing digital\",
            \"Télécommunications\",
            \"Assistance virtuelle\",
            \"Email marketing\",
            \"Customer support manager\",
            \"Conception Web\",
            \"Transcription\",
          ].map((service, i) => (
            <li key={i} className="bg-white text-blue-800 p-4 rounded-xl shadow">✅ {service}</li>
          ))}
        </ul>
      </section>

      <section className="text-center" id="contact">
        <h2 className="text-3xl font-semibold mb-4">Prêt à collaborer ?</h2>
        <p className="text-lg mb-6">Contactez-moi pour booster votre activité avec un vrai soutien pro.</p>
        <a href="mailto:tonmail@example.com" className="bg-white text-blue-700 font-semibold px-6 py-2 rounded hover:bg-blue-100">
          Discutons !
        </a>
      </section>

      <footer className="mt-16 text-center text-sm text-gray-400">
        © {new Date().getFullYear()} Raye – Tous droits réservés
      </footer>
    </div>
  );
}

