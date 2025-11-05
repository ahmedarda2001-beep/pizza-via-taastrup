import React from "react";

// Pizza Via Taastrup - Single-file React + Tailwind preview
// - Tailwind classes are used (assumes Tailwind available in host preview)
// - All menu categories and items included exactly as provided
// - Color palette: deep red primary, white, black, natural accents

const BRAND = {
  name: "Pizza Via Taastrup",
  primary: "#C1272D", // deep Italian red
  accent: "#DAB68C", // warm beige
  dark: "#0B0B0B",
};

const menu = [
  {
    category: "Drikkevarer",
    items: [
      { name: "DÅSE SODAVAND", sub: "0.33 Liter", price: "Fra 20 kr." },
      { name: "SODAVAND", sub: "1.5 Liter", price: "Fra 40 kr." },
      { name: "KILDEVAND", sub: "0.5 Liter", price: "18 kr." },
      { name: "AYRAN", sub: "250 ml", price: "15 kr." },
    ],
  },
  {
    category: "Menu",
    items: [
      { name: "PITA MENU", sub: "Med pommes frites, dyppelse & dåse sodavand", price: "100 kr." },
      { name: "DURUM MENU", sub: "Med pommes frites, dyppelse & dåse sodavand", price: "115 kr." },
      { name: "PIZZA SANDWICH MENU", sub: "Med pommes frites, dyppelse & dåse sodavand", price: "115 kr." },
      { name: "BURGER MENU", sub: "Med pommes frites, dyppelse & dåse sodavand", price: "115 kr." },
    ],
  },
  {
    category: "Pizza",
    note: "Alle pizzaer er med tomatsauce og ost",
    items: [
      { id: 1, name: "Margherita", price: "Fra 70 kr." },
      { id: 2, name: "Al Fungi", sub: "Champignon", price: "Fra 75 kr." },
      { id: 3, name: "VESUVIO", sub: "Skinke", price: "Fra 75 kr." },
      { id: 4, name: "PEPPERONI", sub: "Pepperoni", price: "Fra 75 kr." },
      { id: 5, name: "BOLOGNESE", sub: "Kødsauce", price: "Fra 80 kr." },
      { id: 6, name: "ALTONO", sub: "Tun og løg", price: "Fra 80 kr." },
      { id: 7, name: "HAWAII", sub: "Skinke og ananas", price: "Fra 80 kr." },
      { id: 8, name: "CAPRICCIOSSA", sub: "Skinke og champignon", price: "Fra 80 kr." },
      { id: 9, name: "BUSSOLA", sub: "Skinke og rejer", price: "Fra 80 kr." },
      { id: 10, name: "JUVENTUS", sub: "Kødstrimler, paprika, jalapeño, pesto og creme fraiche", price: "Fra 80 kr." },
      { id: 11, name: "AMIGO", sub: "Pepperoni og løg", price: "Fra 80 kr." },
      { id: 12, name: "RIVIERA", sub: "Skinke, champignon og rejer", price: "Fra 85 kr." },
      { id: 13, name: "POMPEI", sub: "Bacon, løg, æg og pepperoni", price: "Fra 85 kr." },
      { id: 14, name: "LA POLISEN", sub: "Skinke, kebab og bearnaise", price: "Fra 85 kr." },
      { id: 15, name: "COPENHAGEN", sub: "Skinke og pepperoni", price: "Fra 85 kr." },
      { id: 16, name: "ALPACINO", sub: "Skinke, champignon, gorgonzola og bearnaise", price: "Fra 87 kr." },
      { id: 17, name: "ACAPULCO", sub: "Kødstrimler, hvidløg, champignon, jalapeño og tacosauce", price: "Fra 87 kr." },
      { id: 18, name: "AZTECA", sub: "Skinke, jalapeño, tacosauce og hvidløgsdressing", price: "Fra 87 kr." },
      { id: 19, name: "MEXICANA", sub: "Hakket oksekød, jalapeño, løg, tacosauce og hvidløg", price: "Fra 87 kr." },
      { id: 20, name: "TEO'S", sub: "Fetaost, kødstrimler, champignon, tomat, chili og rucola", price: "Fra 87 kr." },
      { id: 21, name: "ZLATAN", sub: "Skinke, bacon, kødstrimler og bearnaise", price: "Fra 87 kr." },
      { id: 22, name: "MAMAMIA", sub: "Kylling, paprika, pesto, kartoffel og chili", price: "Fra 87 kr." },
    ],
  },
  {
    category: "Salat Pizza",
    note: "Alle pizzaer er med tomatsauce og ost",
    items: [
      { id: 23, name: "KEBAB", sub: "Kebab, salat & dressing", price: "Fra 85 kr." },
      { id: 24, name: "KYLLING", sub: "Kylling, salat & dressing", price: "Fra 85 kr." },
      { id: 25, name: "KØDSTRIMLER", sub: "Kødstrimler, salat & dressing", price: "Fra 85 kr." },
      { id: 26, name: "FALAFEL", sub: "Falafel, salat & dressing", price: "Fra 85 kr." },
      { id: 27, name: "SKINKE", sub: "Skinke, salat & dressing", price: "Fra 85 kr." },
      { id: 28, name: "VIA SPECIAL", sub: "Kebab, pommes & dressing", price: "Fra 85 kr." },
    ],
  },
  {
    category: "Indbagt Pizza",
    items: [
      { id: 29, name: "CALZONE", sub: "Skinke", price: "75 kr." },
      { id: 30, name: "PAPAGALO", sub: "Gorgonzola, pepperoni og hvidløg", price: "80 kr." },
      { id: 31, name: "SPAGETTI CALZONE", sub: "Spaghetti og kødsauce", price: "85 kr." },
      { id: 32, name: "CALZONE VIA", sub: "Kebab, champignon, pepperoni og hvidløg", price: "85 kr." },
    ],
  },
  {
    category: "Halv Indbagte Pizzaer",
    items: [
      { id: 33, name: "UBOT", sub: "Kebab, løg, champignon, paprika og bearnaise", price: "85 kr." },
      { id: 34, name: "KEBABBO", sub: "Kebab, salat, pommes og dressing", price: "85 kr." },
      { id: 35, name: "INCOW", sub: "Kødstrimler, champignon, løg og bearnaise", price: "85 kr." },
    ],
  },
  {
    category: "Hjemmelavet Pizza Sandwich",
    note: "Alle er med ost, salat, tomat, agurk og dressing",
    items: [
      { id: 36, name: "Vælg mellem", price: "Fra 75 kr." },
      { id: 37, name: "MIX", sub: "Kebab & Kylling", price: "Fra 85 kr." },
    ],
  },
  {
    category: "Hjemmelavet Durum",
    note: "Alle er med salat, tomat, agurk og dressing",
    items: [
      { id: 38, name: "Vælg mellem", price: "Fra 70 kr." },
      { id: 39, name: "MIX", price: "Fra 80 kr." },
    ],
  },
  {
    category: "Hjemmelavet Pitabrød",
    note: "Alle er med salat, tomat, agurk og dressing",
    items: [
      { id: 40, name: "Vælg mellem", price: "Fra 55 kr." },
      { id: 41, name: "MIX", price: "Fra 65 kr." },
    ],
  },
  {
    category: "Børne Menu",
    items: [
      { id: 42, name: "SALAT PIZZA", sub: "Kebab, salat og dressing", price: "65 kr." },
      { id: 43, name: "HUGO PIZZA", sub: "Skinke", price: "65 kr." },
      { id: 44, name: "BATMAN PIZZA", sub: "Cocktailpølser", price: "65 kr." },
      { id: 45, name: "MALIK PIZZA", sub: "Kødsauce", price: "65 kr." },
      { id: 46, name: "PEPPERONI PIZZA", sub: "Pepperoni", price: "65 kr." },
    ],
  },
  {
    category: "Diverse",
    items: [
      { id: 47, name: "KEBAB BOX", sub: "Med pommes frites, salat og dressing", price: "55 kr." },
      { id: 48, name: "KEBAB BOX", sub: "Med ris, salat og dressing", price: "55 kr." },
      { id: 49, name: "TYRKISK BRØD", sub: "Med kebab, chili, salat og dressing", price: "60 kr." },
      { id: 50, name: "HVIDLØGSBRØD", sub: "Med tomatsauce, ost og hvidløg", price: "50 kr." },
      { id: 51, name: "POMMES FRITES", sub: "Lille", price: "40 kr." },
      { id: 52, name: "POMMES FRITES", sub: "Stor", price: "50 kr." },
    ],
  },
  {
    category: "A La Carte",
    note: "Vælg mellem ris eller pommes frites",
    items: [
      { id: 53, name: "SHAWARMA RET", sub: "Med hvidløgsdressing", price: "Fra 95 kr." },
      { id: 54, name: "1/2 Grill Kylling", sub: "Uden tilbehør", price: "Fra 80 kr." },
      { id: 55, name: "1/2 Grill Kylling", sub: "Med salat, pommes frites, remoulade", price: "Fra 95 kr." },
      { id: 56, name: "NUGGETS MENU", sub: "Med pommes frites", price: "Fra 95 kr." },
    ],
  },
  {
    category: "Hjemmelavet Burger",
    note: "Alle burgere er med 100g bøf",
    items: [
      { id: 57, name: "08 SPECIAL BURGER", sub: "Burgerdressing, chili cheese tops, ost og salat", price: "60 kr." },
      { id: 58, name: "OST & BACON BURGER", sub: "Med ost, bacon, salat, sennep og ketchup", price: "65 kr." },
      { id: 59, name: "LINA'S BURGER", sub: "Med ost, chili dressing, jalapeño og salat", price: "70 kr." },
      { id: 60, name: "CHILI BEARNAISE BURGER", sub: "Med chilibearnaisesauce, løgringe og salat", price: "70 kr." },
      { id: 61, name: "TAASTRUP SPECIAL BURGER", sub: "Med ost, bacon, æg, sennep, ketchup og salat", price: "70 kr." },
      { id: 62, name: "KYLLINGE BURGER", price: "65 kr." },
      { id: 63, name: "VEGO BURGER", price: "65 kr." },
    ],
  },
  {
    category: "Salat",
    items: [
      { id: 64, name: "KØDSTRIMLER SALAT", sub: "Med champignon, aubergine, courgette, crouton, rucola og brød", price: "85 kr." },
      { id: 65, name: "TUNFISK SALAT", sub: "Med oliven, citron, æg, majs, rejer", price: "85 kr." },
      { id: 66, name: "AVOCADO SALAT", sub: "Med rejer, skinke, ost, citron, rucola", price: "85 kr." },
      { id: 67, name: "CÆSAR SALAT", sub: "Med kylling, bacon, løg, rucola og fetaost", price: "85 kr." },
      { id: 68, name: "GRÆSK SALAT", sub: "Med fetaost, løg, paprika, oliven, majs og rucola", price: "80 kr." },
      { id: 69, name: "Vælg mellem", price: "Fra 80 kr." },
    ],
  },
  {
    category: "Snacks & Diverse",
    items: [
      { id: 70, name: "HOTDOG", price: "40 kr." },
      { id: 71, name: "LØGRINGE", sub: "6 stk", price: "35 kr." },
      { id: 72, name: "CHILI CHEESE TOPS", sub: "6 stk", price: "35 kr." },
      { id: 73, name: "HOT WINGS", sub: "6 stk", price: "50 kr." },
      { id: 74, name: "MOZZARELLA STICKS", sub: "6 stk.", price: "35 kr." },
      { id: 75, name: "SNACK KURV", sub: "3 chili cheese tops, 3 løgringe, 3 hot wings, 3 mozzarella sticks", price: "35 kr." },
    ],
  },
];

function LogoSVG({ className = "w-40 h-auto" }) {
  return (
    <div className={className}>
      <svg viewBox="0 0 400 80" xmlns="http://www.w3.org/2000/svg">
        <rect width="400" height="80" rx="12" fill="none" />
        <text x="20" y="50" fontFamily="Poppins, sans-serif" fontWeight="700" fontSize="30" fill={BRAND.primary}>
          Pizza Via
        </text>
        <text x="220" y="50" fontFamily="Inter, sans-serif" fontSize="14" fill="#222">Taastrup</text>
      </svg>
    </div>
  );
}

export default function PizzaViaSite() {
  return (
    <div className="min-h-screen bg-gray-50 text-gray-900">
      {/* Header */}
      <header className="bg-white shadow sticky top-0 z-30">
        <div className="max-w-6xl mx-auto px-4 py-4 flex items-center justify-between">
          <div className="flex items-center gap-4">
            <LogoSVG />
            <div className="hidden md:block">
              <nav className="flex gap-6 text-sm font-medium text-gray-700">
                <a href="#hero" className="hover:text-[color:var(--primary)]">Home</a>
                <a href="#menu" className="hover:text-[color:var(--primary)]">Menu</a>
                <a href="#about" className="hover:text-[color:var(--primary)]">About</a>
                <a href="#contact" className="hover:text-[color:var(--primary)]">Contact</a>
              </nav>
            </div>
          </div>
          <div className="flex items-center gap-3">
            <a href="#order" className="px-4 py-2 bg-[color:var(--primary)] text-white rounded shadow-sm text-sm">Order Now</a>
            <a href="#reservation" className="px-4 py-2 border border-gray-200 rounded text-sm">Reservation</a>
          </div>
        </div>
      </header>

      {/* Hero */}
      <section id="hero" className="bg-[length:cover] bg-center" style={{ backgroundImage: 'linear-gradient(rgba(0,0,0,0.25), rgba(0,0,0,0.25)), url(https://images.unsplash.com/photo-1601924582975-7a9f4b3c1b0b?auto=format&fit=crop&w=1400&q=60)' }}>
        <div className="max-w-6xl mx-auto px-4 py-28 text-white">
          <div className="max-w-3xl">
            <h1 className="text-4xl md:text-6xl font-extrabold drop-shadow">Pizza Via Taastrup</h1>
            <p className="mt-4 text-lg md:text-xl opacity-90">Autentisk smag fra Italien — friskbagte pizzaer, gode råvarer og rar stemning.</p>
            <div className="mt-6 flex gap-3">
              <a href="#menu" className="px-5 py-3 bg-[color:var(--primary)] rounded text-white font-semibold">Se menu</a>
              <a href="#contact" className="px-5 py-3 bg-white rounded text-[color:var(--primary)] font-semibold">Find os</a>
            </div>
          </div>
        </div>
      </section>

      {/* Main layout */}
      <main className="max-w-6xl mx-auto px-4 py-12">
        {/* About */}
        <section id="about" className="grid md:grid-cols-3 gap-8 items-center mb-12">
          <div className="md:col-span-2">
            <h2 className="text-2xl font-bold">Om Pizza Via Taastrup</h2>
            <p className="mt-3 text-gray-700">Pizza Via Taastrup serverer klassiske og kreative pizzaer lavet med kærlighed. Vi bruger friske råvarer, hjemmelavede saucer og bager til perfektion.</p>
            <ul className="mt-4 space-y-2 text-gray-700">
              <li>Åbningstider: Man-Søn 11:00 - 22:00</li>
              <li>Adresse: Taastrup (indsæt præcis adresse ved lancering)</li>
              <li>Telefon: +45 XX XX XX XX</li>
            </ul>
          </div>
          <div className="rounded-lg overflow-hidden shadow-lg">
            <img alt="Pizza" src="https://images.unsplash.com/photo-1548365328-9a7f0b9a7f3a?auto=format&fit=crop&w=800&q=60" className="w-full h-56 object-cover" />
          </div>
        </section>

        {/* Menu */}
        <section id="menu" className="mb-12">
          <div className="flex items-center justify-between">
            <h2 className="text-2xl font-bold">Menu</h2>
            <div className="text-sm text-gray-600">Alle priser er angivet i danske kroner</div>
          </div>

          <div className="mt-6 grid md:grid-cols-3 gap-6">
            {menu.map((cat, idx) => (
              <div key={cat.category} className="bg-white rounded-lg shadow p-4">
                <h3 className="text-lg font-semibold text-[color:var(--primary)]">{cat.category}</h3>
                {cat.note && <div className="mt-1 text-sm text-gray-500">{cat.note}</div>}
                <ul className="mt-3 space-y-2">
                  {cat.items.map((item, i) => (
                    <li key={i} className="flex justify-between items-start gap-4">
                      <div>
                        <div className="font-medium">{item.name}</div>
                        {item.sub && <div className="text-sm text-gray-500">{item.sub}</div>}
                      </div>
                      <div className="text-sm font-semibold">{item.price}</div>
                    </li>
                  ))}
                </ul>
              </div>
            ))}
          </div>
        </section>

        {/* Reservation / Order callout */}
        <section id="reservation" className="bg-white rounded-lg shadow p-6 mb-12 flex flex-col md:flex-row items-center justify-between">
          <div>
            <h3 className="text-xl font-bold">Book et bord eller bestil takeaway</h3>
            <p className="mt-2 text-gray-700">Vi tilbyder afhentning og bordreservation. Klik på knapperne for at komme i gang (integration kan tilføjes senere).</p>
          </div>
          <div className="mt-4 md:mt-0 flex gap-3">
            <button className="px-4 py-2 bg-[color:var(--primary)] text-white rounded">Bestil nu</button>
            <button className="px-4 py-2 border border-gray-200 rounded">Reserver bord</button>
          </div>
        </section>

        {/* Contact */}
        <section id="contact" className="grid md:grid-cols-2 gap-6">
          <div className="bg-white rounded-lg shadow p-6">
            <h3 className="text-lg font-bold">Kontakt</h3>
            <p className="mt-2 text-gray-700">Har du spørgsmål? Ring eller skriv til os.</p>
            <dl className="mt-4 text-sm text-gray-700 space-y-2">
              <div>
                <dt className="font-semibold">Adresse</dt>
                <dd>Indsæt adresse, Taastrup</dd>
              </div>
              <div>
                <dt className="font-semibold">Telefon</dt>
                <dd>+45 XX XX XX XX</dd>
              </div>
              <div>
                <dt className="font-semibold">Åbningstider</dt>
                <dd>Man-Søn 11:00 - 22:00</dd>
              </div>
            </dl>
          </div>

          <div className="bg-white rounded-lg shadow p-6">
            <h3 className="text-lg font-bold">Find os</h3>
            <p className="mt-2 text-gray-700">Kort og vejbeskrivelse kan indsættes her.</p>
            <div className="mt-4 h-48 bg-gray-100 rounded flex items-center justify-center text-gray-400">Map placeholder</div>
          </div>
        </section>
      </main>

      {/* Footer */}
      <footer className="bg-[color:var(--dark)] text-white">
        <div className="max-w-6xl mx-auto px-4 py-8 grid md:grid-cols-3 gap-6">
          <div>
            <LogoSVG className="w-36 h-auto text-white" />
            <p className="mt-2 text-sm opacity-80">© {new Date().getFullYear()} Pizza Via Taastrup</p>
          </div>
          <div>
            <h4 className="font-semibold">Åbningstider</h4>
            <p className="text-sm mt-2">Man-Søn 11:00 - 22:00</p>
          </div>
          <div>
            <h4 className="font-semibold">Kontakt</h4>
            <p className="text-sm mt-2">Telefon: +45 XX XX XX XX</p>
            <p className="text-sm">Adresse: Taastrup (indsæt adresse)</p>
          </div>
        </div>
      </footer>

      {/* Inline CSS variables for colors */}
      <style jsx>{`
        :root{ --primary: ${BRAND.primary}; --accent: ${BRAND.accent}; --dark: ${BRAND.dark} }
      `}</style>
    </div>
  );
}
