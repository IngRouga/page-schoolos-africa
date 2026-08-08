import React, { useEffect, useRef, useState } from "react";
import {
  ArrowRight,
  ArrowUpRight,
  Check,
  ChevronDown,
  Menu,
  X,
  Users,
  CreditCard,
  LayoutDashboard,
  FileBarChart2,
  School,
  ShieldCheck,
} from "lucide-react";

/* =====================================================================
   ART DIRECTION — SchoolOS Africa
   -----------------------------------------------------------------
   Thesis: the product's real unit of value is the RECEIPT — the
   moment a fee payment becomes proof. Everything visual is built
   around that object: a perforated / torn-edge ticket, a mono
   ledger typeface for amounts, a running stub down the page.

   Ink       #111111   text / primary
   Emerald   #10B981   accent, "paid" state
   Amber     #D97706   "pending" state (used sparingly, never as accent)
   Paper     #FFFFFF   background
   Bone      #F3F4F1   section tint (warmer than typical gray-50)
   Line      #E4E6E1
   Slate     #5B6157

   Display : Fraunces (serif, editorial — NOT the default AI sans-serif look)
   Body    : Inter
   Ledger  : JetBrains Mono — every FCFA figure, every index number
   ===================================================================== */

const FONTS = `@import url('https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,500;9..144,600;9..144,700&family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@500;600;700&display=swap');`;

function useReveal(threshold = 0.15) {
  const ref = useRef(null);
  const [visible, setVisible] = useState(false);
  useEffect(() => {
    const el = ref.current;
    if (!el) return;
    if (window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
      setVisible(true);
      return;
    }
    const obs = new IntersectionObserver(
      ([e]) => {
        if (e.isIntersecting) {
          setVisible(true);
          obs.unobserve(el);
        }
      },
      { threshold }
    );
    obs.observe(el);
    return () => obs.disconnect();
  }, [threshold]);
  return [ref, visible];
}

function Reveal({ children, delay = 0, className = "" }) {
  const [ref, visible] = useReveal();
  return (
    <div
      ref={ref}
      className={className}
      style={{
        opacity: visible ? 1 : 0,
        transform: visible ? "translateY(0)" : "translateY(18px)",
        transition: `opacity .7s cubic-bezier(.16,1,.3,1) ${delay}ms, transform .7s cubic-bezier(.16,1,.3,1) ${delay}ms`,
      }}
    >
      {children}
    </div>
  );
}

function useCountUp(target, visible, duration = 1300) {
  const [v, setV] = useState(0);
  useEffect(() => {
    if (!visible) return;
    let raf;
    const start = performance.now();
    const tick = (now) => {
      const t = Math.min(1, (now - start) / duration);
      setV(Math.floor((1 - Math.pow(1 - t, 3)) * target));
      if (t < 1) raf = requestAnimationFrame(tick);
    };
    raf = requestAnimationFrame(tick);
    return () => cancelAnimationFrame(raf);
  }, [visible, target, duration]);
  return v;
}
const fmt = (n) => n.toLocaleString("fr-FR").replace(/,/g, " ");

/* ---------- perforated ticket edge, reused as the signature device ---------- */
function TicketEdge({ flip = false, color = "#FFFFFF" }) {
  const dots = new Array(28).fill(0);
  return (
    <svg
      className={`w-full block ${flip ? "rotate-180" : ""}`}
      height="10"
      viewBox="0 0 560 10"
      preserveAspectRatio="none"
    >
      {dots.map((_, i) => (
        <circle key={i} cx={10 + i * 20} cy="0" r="6" fill={color} />
      ))}
    </svg>
  );
}

/* ============================== NAV ============================== */
function Nav() {
  const [open, setOpen] = useState(false);
  const [scrolled, setScrolled] = useState(false);
  useEffect(() => {
    const f = () => setScrolled(window.scrollY > 8);
    window.addEventListener("scroll", f);
    return () => window.removeEventListener("scroll", f);
  }, []);
  const links = [
    ["Fonctionnalités", "#fonctionnalites"],
    ["Méthode", "#methode"],
    ["Tarifs", "#tarifs"],
    ["FAQ", "#faq"],
  ];
  return (
    <header
      className={`fixed top-0 inset-x-0 z-50 transition-colors duration-300 ${
        scrolled ? "bg-white/90 backdrop-blur-md border-b border-[#E4E6E1]" : "bg-transparent"
      }`}
    >
      <div className="max-w-[1240px] mx-auto px-6 lg:px-10 h-[76px] flex items-center justify-between">
        <a href="#top" className="flex items-center gap-2">
          <span className="font-[Fraunces] font-semibold text-[19px] text-[#111111]">
            SchoolOS<span className="text-[#10B981]">.</span>
          </span>
        </a>
        <nav className="hidden md:flex items-center gap-10">
          {links.map(([l, h]) => (
            <a key={h} href={h} className="text-[14px] text-[#5B6157] hover:text-[#111111] font-[Inter] font-medium transition-colors">
              {l}
            </a>
          ))}
        </nav>
        <div className="hidden md:flex items-center gap-5">
          <a href="#connexion" className="text-[14px] font-[Inter] font-medium text-[#5B6157] hover:text-[#111111] transition-colors">
            Connexion
          </a>
          <a
            href="#cta-principal"
            className="inline-flex items-center gap-1.5 text-[14px] font-[Inter] font-semibold text-white bg-[#111111] px-4 py-2.5 rounded-full hover:bg-[#10B981] transition-colors duration-300"
          >
            Essayer gratuitement
          </a>
        </div>
        <button className="md:hidden" onClick={() => setOpen((v) => !v)} aria-label="Menu">
          {open ? <X size={22} /> : <Menu size={22} />}
        </button>
      </div>
      {open && (
        <div className="md:hidden bg-white border-t border-[#E4E6E1] px-6 py-5 flex flex-col gap-4">
          {links.map(([l, h]) => (
            <a key={h} href={h} onClick={() => setOpen(false)} className="text-[15px] font-[Inter] font-medium text-[#374151]">
              {l}
            </a>
          ))}
          <a href="#cta-principal" onClick={() => setOpen(false)} className="text-[15px] font-[Inter] font-semibold bg-[#111111] text-white text-center px-4 py-3 rounded-full">
            Essayer gratuitement
          </a>
        </div>
      )}
    </header>
  );
}

/* ============================== HERO ============================== */
function ReceiptMock() {
  const [ref, visible] = useReveal(0.3);
  const encaisse = useCountUp(4820000, visible);
  const rows = [
    { name: "Aïcha Diallo", classe: "6ème B", montant: "45 000", statut: "payé" },
    { name: "Moussa Traoré", classe: "3ème A", montant: "30 000", statut: "payé" },
    { name: "Fatou Ndiaye", classe: "Term. C", montant: "60 000", statut: "attente" },
    { name: "Ousmane Bâ", classe: "5ème A", montant: "45 000", statut: "payé" },
  ];
  return (
    <div ref={ref} className="relative" style={{ perspective: "1400px" }}>
      <div
        className="relative"
        style={{
          transform: visible ? "rotate(-2.2deg) rotate3d(1,-1,0,4deg)" : "rotate(0deg)",
          transition: "transform 1s cubic-bezier(.16,1,.3,1)",
        }}
      >
        {/* the ticket */}
        <div className="bg-white shadow-[0_40px_80px_-30px_rgba(17,17,17,0.35)] max-w-[400px] mx-auto">
          <div className="bg-[#111111] px-6 py-5">
            <p className="text-[10.5px] tracking-[0.16em] uppercase text-[#9CA3AF] font-[Inter] font-medium">
              Reçu de scolarité — Trimestre 1
            </p>
            <p className="font-[Fraunces] text-white text-[18px] mt-1">Collège Sainte-Aminata</p>
          </div>
          <div className="px-6 py-5">
            <p className="text-[10.5px] tracking-[0.14em] uppercase text-[#9CA3AF] font-[Inter] font-medium mb-1">
              Total encaissé
            </p>
            <p className="font-[JetBrains_Mono] font-bold text-[30px] text-[#111111] leading-none">
              {fmt(encaisse)} <span className="text-[15px] text-[#9CA3AF] font-medium">FCFA</span>
            </p>
          </div>
          <TicketEdge color="#F3F4F1" />
          <div className="bg-[#F3F4F1] px-6 py-4">
            <div className="divide-y divide-[#E4E6E1]">
              {rows.map((r, i) => (
                <div
                  key={r.name}
                  className="flex items-center justify-between py-2.5"
                  style={{
                    opacity: visible ? 1 : 0,
                    transform: visible ? "translateX(0)" : "translateX(-8px)",
                    transition: `all .5s cubic-bezier(.16,1,.3,1) ${i * 110 + 300}ms`,
                  }}
                >
                  <div>
                    <p className="text-[12.5px] font-[Inter] font-medium text-[#111111]">{r.name}</p>
                    <p className="text-[11px] font-[Inter] text-[#9CA3AF]">{r.classe}</p>
                  </div>
                  <div className="text-right">
                    <p className="font-[JetBrains_Mono] text-[12.5px] font-semibold text-[#111111]">{r.montant} F</p>
                    <p className={`text-[10px] font-[Inter] font-medium ${r.statut === "payé" ? "text-[#059669]" : "text-[#D97706]"}`}>
                      {r.statut}
                    </p>
                  </div>
                </div>
              ))}
            </div>
          </div>
        </div>
        {/* torn bottom edge */}
        <svg width="400" height="16" viewBox="0 0 400 16" className="mx-auto block max-w-[400px] w-full" preserveAspectRatio="none">
          <path d="M0 0 L20 15 L40 0 L60 15 L80 0 L100 15 L120 0 L140 15 L160 0 L180 15 L200 0 L220 15 L240 0 L260 15 L280 0 L300 15 L320 0 L340 15 L360 0 L380 15 L400 0 L400 0 L0 0 Z" fill="#F3F4F1" />
        </svg>
      </div>

      {/* floating emerald badge */}
      <div
        className="hidden lg:block absolute -right-6 top-10 bg-[#10B981] text-[#111111] rounded-2xl px-4 py-3 shadow-[0_20px_40px_-15px_rgba(16,185,129,0.5)]"
        style={{
          opacity: visible ? 1 : 0,
          transform: visible ? "translateY(0) rotate(3deg)" : "translateY(10px) rotate(3deg)",
          transition: "all .8s cubic-bezier(.16,1,.3,1) 700ms",
        }}
      >
        <p className="text-[11px] font-[Inter] font-semibold">+18% ce trimestre</p>
      </div>
    </div>
  );
}

function Hero() {
  return (
    <section id="top" className="relative pt-40 pb-28 lg:pt-48 overflow-hidden bg-white">
      <div className="absolute top-0 inset-x-0 h-[560px] -z-10" style={{ background: "linear-gradient(180deg, #F3F4F1 0%, #FFFFFF 100%)" }} />
      <div className="max-w-[1240px] mx-auto px-6 lg:px-10 grid lg:grid-cols-[1.15fr_1fr] gap-16 items-start">
        <div>
          <Reveal>
            <p className="font-[JetBrains_Mono] text-[12.5px] text-[#059669] font-semibold tracking-wide mb-6">
              N°01 — GESTION DES FRAIS SCOLAIRES
            </p>
          </Reveal>
          <Reveal delay={80}>
            <h1 className="font-[Fraunces] font-semibold text-[#111111] text-[42px] sm:text-[54px] lg:text-[64px] leading-[1.02] tracking-[-0.01em]">
              Gérez les frais de
              <br />
              scolarité en toute
              <br />
              <span className="italic text-[#10B981]">simplicité.</span>
            </h1>
          </Reveal>
          <Reveal delay={200}>
            <p className="mt-8 text-[17px] leading-[1.65] text-[#5B6157] max-w-[480px] font-[Inter]">
              SchoolOS Africa aide les écoles africaines à suivre les paiements, réduire les
              impayés et générer des rapports financiers en quelques clics.
            </p>
          </Reveal>
          <Reveal delay={300}>
            <div className="mt-10 flex flex-col sm:flex-row gap-3.5">
              <a
                id="cta-principal"
                href="#tarifs"
                className="group inline-flex items-center justify-center gap-2 bg-[#111111] text-white font-[Inter] font-semibold text-[15px] px-6 py-3.5 rounded-full hover:bg-[#10B981] transition-colors duration-300"
              >
                Créer une école gratuitement
                <ArrowRight size={16} className="group-hover:translate-x-1 transition-transform" />
              </a>
              <a
                href="#demo"
                className="inline-flex items-center justify-center gap-2 text-[#111111] font-[Inter] font-semibold text-[15px] px-6 py-3.5 rounded-full border border-[#111111]/15 hover:border-[#111111] transition-colors duration-300"
              >
                Voir une démonstration
              </a>
            </div>
          </Reveal>
          <Reveal delay={420}>
            <div className="mt-16 grid grid-cols-3 max-w-[420px] border-t border-[#E4E6E1] pt-6">
              {[
                ["230+", "écoles"],
                ["4,2 Md", "FCFA suivis"],
                ["–37%", "d'impayés"],
              ].map(([n, l]) => (
                <div key={l}>
                  <p className="font-[JetBrains_Mono] font-bold text-[20px] text-[#111111]">{n}</p>
                  <p className="text-[12px] font-[Inter] text-[#9CA3AF] mt-0.5">{l}</p>
                </div>
              ))}
            </div>
          </Reveal>
        </div>
        <Reveal delay={160}>
          <ReceiptMock />
        </Reveal>
      </div>
    </section>
  );
}

/* ============================== TRUST ============================== */
function Trust() {
  const noms = ["Académie Kayes", "Groupe Scolaire Liberté", "Institut Cheikh Anta", "Complexe Le Flambeau", "École Nouvelle Génération", "Lycée Horizon"];
  return (
    <section className="py-14 bg-[#111111]">
      <Reveal>
        <p className="text-center text-[12.5px] font-[Inter] font-medium text-[#6B7280] mb-8 tracking-wide">
          DÉJÀ ADOPTÉ PAR DES ÉCOLES EN AFRIQUE
        </p>
      </Reveal>
      <div className="max-w-[1100px] mx-auto px-6 flex flex-wrap justify-center gap-x-10 gap-y-5">
        {noms.map((n, i) => (
          <Reveal key={n} delay={i * 60}>
            <span className="font-[Fraunces] text-[16px] text-[#9CA3AF] hover:text-white transition-colors">{n}</span>
          </Reveal>
        ))}
      </div>
    </section>
  );
}

/* ============================== FEATURES — bento ============================== */
function Features() {
  return (
    <section id="fonctionnalites" className="py-24 lg:py-32 bg-white">
      <div className="max-w-[1240px] mx-auto px-6 lg:px-10">
        <Reveal className="max-w-lg mb-16">
          <p className="font-[JetBrains_Mono] text-[12.5px] text-[#059669] font-semibold tracking-wide mb-4">
            N°02 — FONCTIONNALITÉS
          </p>
          <h2 className="font-[Fraunces] font-semibold text-[32px] sm:text-[40px] text-[#111111] leading-[1.1]">
            Pourquoi choisir <span className="italic">SchoolOS Africa</span> ?
          </h2>
        </Reveal>

        <div className="grid lg:grid-cols-3 gap-5">
          {/* large card */}
          <Reveal className="lg:col-span-2 lg:row-span-2">
            <div className="h-full bg-[#111111] rounded-[24px] p-9 flex flex-col justify-between min-h-[340px]">
              <div>
                <span className="inline-flex w-11 h-11 rounded-full bg-[#10B981] items-center justify-center mb-8">
                  <CreditCard size={19} className="text-[#111111]" />
                </span>
                <h3 className="font-[Fraunces] text-white text-[24px] mb-3">Gestion des paiements</h3>
                <p className="text-[14.5px] leading-[1.7] text-[#9CA3AF] font-[Inter] max-w-[380px]">
                  Enregistrez rapidement chaque paiement de scolarité, en espèces ou par mobile
                  money, et laissez SchoolOS calculer les soldes automatiquement.
                </p>
              </div>
              <div className="flex items-end gap-1.5 h-16 mt-8">
                {[30, 46, 38, 58, 50, 70, 62, 82, 74, 90].map((h, i) => (
                  <div key={i} className="flex-1 bg-white/10 rounded-sm" style={{ height: `${h}%` }}>
                    <div className="w-full bg-[#10B981] rounded-sm" style={{ height: "35%" }} />
                  </div>
                ))}
              </div>
            </div>
          </Reveal>

          {[
            { icon: Users, title: "Gestion des élèves", desc: "Ajoutez, recherchez et gérez tous vos élèves facilement." },
            { icon: LayoutDashboard, title: "Tableau de bord", desc: "Visualisez les montants attendus, encaissés et les impayés." },
            { icon: FileBarChart2, title: "Rapports", desc: "Exportez vos rapports en PDF et Excel." },
            { icon: School, title: "Gestion des classes", desc: "Organisez vos élèves par classe." },
          ].map((it, i) => (
            <Reveal key={it.title} delay={i * 80}>
              <div className="h-full bg-[#F3F4F1] rounded-[24px] p-7 min-h-[160px] hover:bg-[#ECFDF5] transition-colors duration-300">
                <it.icon size={20} className="text-[#111111] mb-5" />
                <h3 className="font-[Fraunces] text-[17px] text-[#111111] mb-1.5">{it.title}</h3>
                <p className="text-[13.5px] leading-[1.6] text-[#5B6157] font-[Inter]">{it.desc}</p>
              </div>
            </Reveal>
          ))}

          <Reveal className="lg:col-span-1">
            <div className="h-full bg-white border-2 border-[#111111] rounded-[24px] p-7 min-h-[160px]">
              <ShieldCheck size={20} className="text-[#10B981] mb-5" />
              <h3 className="font-[Fraunces] text-[17px] text-[#111111] mb-1.5">Sécurité</h3>
              <p className="text-[13.5px] leading-[1.6] text-[#5B6157] font-[Inter]">
                Chaque école possède ses propres données sécurisées.
              </p>
            </div>
          </Reveal>
        </div>
      </div>
    </section>
  );
}

/* ============================== METHOD ============================== */
function Method() {
  const steps = [
    { n: "01", title: "Créez votre école", desc: "Renseignez le nom, le logo et les informations de votre établissement." },
    { n: "02", title: "Ajoutez classes et élèves", desc: "Importez ou saisissez vos classes, puis inscrivez chaque élève." },
    { n: "03", title: "Enregistrez les paiements", desc: "Suivez chaque versement en temps réel, soldes calculés automatiquement." },
  ];
  return (
    <section id="methode" className="py-24 lg:py-32 bg-[#F3F4F1]">
      <div className="max-w-[1240px] mx-auto px-6 lg:px-10">
        <Reveal className="mb-16">
          <p className="font-[JetBrains_Mono] text-[12.5px] text-[#059669] font-semibold tracking-wide mb-4">
            N°03 — MÉTHODE
          </p>
          <h2 className="font-[Fraunces] font-semibold text-[32px] sm:text-[40px] text-[#111111]">
            Trois étapes pour démarrer
          </h2>
        </Reveal>
        <div className="divide-y divide-[#D8DAD4] border-y border-[#D8DAD4]">
          {steps.map((s, i) => (
            <Reveal key={s.n} delay={i * 100}>
              <div className="grid sm:grid-cols-[100px_1fr_2fr] gap-4 sm:gap-8 py-9 items-baseline">
                <span className="font-[JetBrains_Mono] text-[14px] text-[#9CA3AF] font-semibold">{s.n}</span>
                <h3 className="font-[Fraunces] text-[22px] text-[#111111]">{s.title}</h3>
                <p className="text-[14.5px] leading-[1.6] text-[#5B6157] font-[Inter] max-w-[440px]">{s.desc}</p>
              </div>
            </Reveal>
          ))}
        </div>
      </div>
    </section>
  );
}

/* ============================== BENEFITS — ledger style ============================== */
function Benefits() {
  const [ref, visible] = useReveal(0.3);
  const rows = [
    { label: "Réduisez les erreurs de caisse.", stat: "–92%", statLabel: "erreurs de saisie" },
    { label: "Suivez chaque paiement.", stat: "100%", statLabel: "traçabilité" },
    { label: "Identifiez rapidement les impayés.", stat: "3 min", statLabel: "temps moyen" },
    { label: "Consultez vos rapports instantanément.", stat: "1 clic", statLabel: "export PDF/Excel" },
  ];
  return (
    <section className="py-24 lg:py-32 bg-white">
      <div className="max-w-[1240px] mx-auto px-6 lg:px-10 grid lg:grid-cols-[0.85fr_1fr] gap-16 items-start">
        <Reveal>
          <p className="font-[JetBrains_Mono] text-[12.5px] text-[#059669] font-semibold tracking-wide mb-4">
            N°04 — BÉNÉFICES
          </p>
          <h2 className="font-[Fraunces] font-semibold text-[32px] sm:text-[38px] text-[#111111] leading-[1.15] max-w-sm">
            Une comptabilité <span className="italic">sans zones d'ombre.</span>
          </h2>
        </Reveal>
        <div ref={ref} className="border-t border-[#E4E6E1]">
          {rows.map((r, i) => (
            <div
              key={r.label}
              className="grid grid-cols-[1fr_auto] items-center gap-6 py-6 border-b border-[#E4E6E1]"
              style={{
                opacity: visible ? 1 : 0,
                transform: visible ? "translateY(0)" : "translateY(10px)",
                transition: `all .6s cubic-bezier(.16,1,.3,1) ${i * 100}ms`,
              }}
            >
              <div className="flex items-center gap-4">
                <Check size={16} strokeWidth={3} className="text-[#10B981] flex-shrink-0" />
                <span className="text-[15.5px] font-[Inter] text-[#374151]">{r.label}</span>
              </div>
              <div className="text-right">
                <p className="font-[JetBrains_Mono] font-bold text-[18px] text-[#111111]">{r.stat}</p>
                <p className="text-[11px] font-[Inter] text-[#9CA3AF]">{r.statLabel}</p>
              </div>
            </div>
          ))}
        </div>
      </div>
    </section>
  );
}

/* ============================== TESTIMONIALS ============================== */
function Testimonials() {
  const data = [
    { quote: "Notre comptabilité est enfin claire. Nous savons exactement qui a payé et qui doit encore régler ses frais.", name: "Mariam Coulibaly", role: "Directrice, Groupe Scolaire Liberté", initials: "MC" },
    { quote: "Ce qui prenait deux jours de rapports se fait maintenant en quelques clics chaque mois.", name: "Ibrahim Sow", role: "Comptable, Institut Cheikh Anta", initials: "IS" },
    { quote: "L'équipe pédagogique et les caissiers travaillent enfin avec les mêmes chiffres.", name: "Aminata Kaboré", role: "Fondatrice, Complexe Le Flambeau", initials: "AK" },
  ];
  return (
    <section className="py-24 lg:py-32 bg-[#111111]">
      <div className="max-w-[1240px] mx-auto px-6 lg:px-10">
        <Reveal className="max-w-lg mb-16">
          <p className="font-[JetBrains_Mono] text-[12.5px] text-[#10B981] font-semibold tracking-wide mb-4">
            N°05 — TÉMOIGNAGES
          </p>
          <h2 className="font-[Fraunces] font-semibold text-[32px] sm:text-[38px] text-white">
            La confiance des équipes de direction
          </h2>
        </Reveal>
        <div className="grid md:grid-cols-3 gap-px bg-white/10 rounded-[24px] overflow-hidden">
          {data.map((t, i) => (
            <Reveal key={t.name} delay={i * 100}>
              <div className="h-full bg-[#111111] p-8 flex flex-col">
                <span className="font-[Fraunces] italic text-[#10B981] text-[34px] leading-none mb-4">”</span>
                <p className="text-[14.5px] leading-[1.7] text-[#D1D5DB] font-[Inter] flex-1">{t.quote}</p>
                <div className="flex items-center gap-3 mt-8 pt-6 border-t border-white/10">
                  <span className="w-9 h-9 rounded-full bg-[#10B981] text-[#111111] text-[11.5px] font-[Fraunces] font-semibold flex items-center justify-center">
                    {t.initials}
                  </span>
                  <div>
                    <p className="text-[13px] font-[Inter] font-semibold text-white">{t.name}</p>
                    <p className="text-[11.5px] font-[Inter] text-[#9CA3AF]">{t.role}</p>
                  </div>
                </div>
              </div>
            </Reveal>
          ))}
        </div>
      </div>
    </section>
  );
}

/* ============================== PRICING ============================== */
function Pricing() {
  const plans = [
    { name: "Starter", desc: "Pour les petites écoles", price: "15 000", features: ["Élèves illimités", "Paiements illimités", "Rapports PDF et Excel", "Support par e-mail"] },
    { name: "Professional", desc: "Pour les écoles privées", price: "35 000", highlight: true, features: ["Élèves illimités", "Paiements illimités", "Rapports PDF et Excel", "Support prioritaire", "Comptes caissiers multiples"] },
    { name: "Enterprise", desc: "Pour les grands établissements", price: "Sur mesure", features: ["Élèves illimités", "Paiements illimités", "Rapports PDF et Excel", "Support dédié", "Accompagnement à la mise en place"] },
  ];
  return (
    <section id="tarifs" className="py-24 lg:py-32 bg-[#F3F4F1]">
      <div className="max-w-[1240px] mx-auto px-6 lg:px-10">
        <Reveal className="text-center max-w-lg mx-auto mb-16">
          <p className="font-[JetBrains_Mono] text-[12.5px] text-[#059669] font-semibold tracking-wide mb-4">
            N°06 — TARIFS
          </p>
          <h2 className="font-[Fraunces] font-semibold text-[32px] sm:text-[40px] text-[#111111]">
            Un tarif simple, adapté à votre école
          </h2>
        </Reveal>
        <div className="grid lg:grid-cols-3 gap-6 items-stretch">
          {plans.map((p, i) => (
            <Reveal key={p.name} delay={i * 100}>
              <div className={`h-full rounded-[24px] p-8 flex flex-col ${p.highlight ? "bg-[#111111] text-white lg:-translate-y-3 shadow-[0_30px_60px_-25px_rgba(17,17,17,0.5)]" : "bg-white"}`}>
                {p.highlight && <span className="self-start text-[11px] font-[Inter] font-semibold bg-[#10B981] text-[#111111] px-2.5 py-1 rounded-full mb-4">Le plus populaire</span>}
                <h3 className={`font-[Fraunces] text-[20px] ${p.highlight ? "text-white" : "text-[#111111]"}`}>{p.name}</h3>
                <p className={`text-[13.5px] mt-1 font-[Inter] ${p.highlight ? "text-[#9CA3AF]" : "text-[#5B6157]"}`}>{p.desc}</p>
                <div className="mt-7 mb-8 flex items-baseline gap-1.5">
                  <span className="font-[JetBrains_Mono] font-bold text-[30px]">{p.price}</span>
                  {p.price !== "Sur mesure" && <span className="text-[13px] font-[Inter] text-[#9CA3AF]">FCFA / mois</span>}
                </div>
                <ul className="space-y-3.5 flex-1 mb-8">
                  {p.features.map((f) => (
                    <li key={f} className="flex items-start gap-2.5">
                      <Check size={15} strokeWidth={3} className="text-[#10B981] mt-0.5 flex-shrink-0" />
                      <span className={`text-[13.5px] font-[Inter] ${p.highlight ? "text-[#E5E7EB]" : "text-[#374151]"}`}>{f}</span>
                    </li>
                  ))}
                </ul>
                <a href="#cta-principal" className={`text-center font-[Inter] font-semibold text-[14.5px] px-5 py-3 rounded-full transition-colors duration-300 ${p.highlight ? "bg-[#10B981] text-[#111111] hover:bg-white" : "bg-[#F3F4F1] text-[#111111] hover:bg-[#111111] hover:text-white"}`}>
                  Commencer
                </a>
              </div>
            </Reveal>
          ))}
        </div>
      </div>
    </section>
  );
}

/* ============================== FAQ ============================== */
function FAQItem({ q, a, defaultOpen = false }) {
  const [open, setOpen] = useState(defaultOpen);
  return (
    <div className="border-b border-[#E4E6E1] py-6">
      <button onClick={() => setOpen((v) => !v)} className="w-full flex items-center justify-between text-left gap-4">
        <span className="text-[16px] font-[Fraunces] text-[#111111]">{q}</span>
        <ChevronDown size={18} className="text-[#9CA3AF] flex-shrink-0 transition-transform duration-300" style={{ transform: open ? "rotate(180deg)" : "rotate(0deg)" }} />
      </button>
      <div className="overflow-hidden transition-all duration-300" style={{ maxHeight: open ? "160px" : "0px", marginTop: open ? "12px" : "0px" }}>
        <p className="text-[14.5px] leading-[1.7] text-[#5B6157] font-[Inter] pr-8">{a}</p>
      </div>
    </div>
  );
}
function FAQ() {
  const items = [
    { q: "Est-ce que les données sont sécurisées ?", a: "Oui. Chaque école dispose de son propre espace isolé et sécurisé — vos données ne sont jamais partagées avec un autre établissement." },
    { q: "Puis-je exporter les rapports ?", a: "Oui, vous pouvez exporter tous vos rapports financiers au format PDF ou Excel en un seul clic, à tout moment." },
    { q: "Le logiciel fonctionne-t-il sur téléphone ?", a: "Oui, SchoolOS Africa est entièrement responsive et fonctionne sur ordinateur, tablette et smartphone." },
    { q: "Puis-je créer plusieurs classes ?", a: "Oui, vous pouvez créer autant de classes que nécessaire selon la structure de votre établissement." },
  ];
  return (
    <section id="faq" className="py-24 lg:py-32 bg-white">
      <div className="max-w-2xl mx-auto px-6">
        <Reveal className="mb-14">
          <p className="font-[JetBrains_Mono] text-[12.5px] text-[#059669] font-semibold tracking-wide mb-4">N°07 — FAQ</p>
          <h2 className="font-[Fraunces] font-semibold text-[32px] sm:text-[38px] text-[#111111]">Questions fréquentes</h2>
        </Reveal>
        <Reveal>
          <div>{items.map((it, i) => <FAQItem key={it.q} q={it.q} a={it.a} defaultOpen={i === 0} />)}</div>
        </Reveal>
      </div>
    </section>
  );
}

/* ============================== FINAL CTA ============================== */
function FinalCTA() {
  return (
    <section className="py-28 lg:py-36 px-6 bg-[#F3F4F1]">
      <Reveal>
        <div className="max-w-3xl mx-auto text-center">
          <p className="font-[JetBrains_Mono] text-[12.5px] text-[#059669] font-semibold tracking-wide mb-6">N°08 — DÉMARRER</p>
          <h2 className="font-[Fraunces] font-semibold text-[36px] sm:text-[52px] leading-[1.05] text-[#111111]">
            Prêt à simplifier la gestion <span className="italic">de votre école</span> ?
          </h2>
          <a
            id="cta-final"
            href="#top"
            className="mt-10 inline-flex items-center gap-2 bg-[#111111] text-white font-[Inter] font-semibold text-[15px] px-7 py-4 rounded-full hover:bg-[#10B981] hover:text-[#111111] transition-colors duration-300"
          >
            Créer mon école gratuitement
            <ArrowUpRight size={17} />
          </a>
        </div>
      </Reveal>
    </section>
  );
}

/* ============================== FOOTER ============================== */
function Footer() {
  return (
    <footer className="bg-[#111111] pt-16 pb-8 px-6">
      <div className="max-w-[1240px] mx-auto grid sm:grid-cols-2 lg:grid-cols-4 gap-12">
        <div className="lg:col-span-2">
          <span className="font-[Fraunces] font-semibold text-[19px] text-white">SchoolOS<span className="text-[#10B981]">.</span></span>
          <p className="text-[13.5px] text-[#9CA3AF] font-[Inter] max-w-xs leading-[1.6] mt-4">
            La plateforme de gestion des frais de scolarité pensée pour les écoles africaines.
          </p>
        </div>
        <div>
          <p className="text-[12px] font-[Inter] font-semibold text-white mb-4 tracking-wide">PRODUIT</p>
          <ul className="space-y-3">
            {["Accueil", "Fonctionnalités", "Tarifs", "FAQ"].map((l) => (
              <li key={l}><a href="#" className="text-[13.5px] text-[#9CA3AF] hover:text-white font-[Inter] transition-colors">{l}</a></li>
            ))}
          </ul>
        </div>
        <div>
          <p className="text-[12px] font-[Inter] font-semibold text-white mb-4 tracking-wide">ENTREPRISE</p>
          <ul className="space-y-3">
            {["Contact", "Politique de confidentialité"].map((l) => (
              <li key={l}><a href="#" className="text-[13.5px] text-[#9CA3AF] hover:text-white font-[Inter] transition-colors">{l}</a></li>
            ))}
          </ul>
        </div>
      </div>
      <div className="max-w-[1240px] mx-auto mt-14 pt-6 border-t border-white/10 text-[12.5px] text-[#6B7280] font-[Inter]">
        © 2026 SchoolOS Africa.
      </div>
    </footer>
  );
}

/* ============================== APP ============================== */
export default function App() {
  return (
    <div className="min-h-screen bg-white antialiased" style={{ fontFamily: "Inter, sans-serif" }}>
      <style>{`
        ${FONTS}
        html { scroll-behavior: smooth; }
        ::selection { background: #10B981; color: #111111; }
        a:focus-visible, button:focus-visible { outline: 2px solid #10B981; outline-offset: 2px; border-radius: 6px; }
        @media (prefers-reduced-motion: reduce) {
          * { animation-duration: .001ms !important; transition-duration: .001ms !important; }
        }
      `}</style>
      <Nav />
      <main>
        <Hero />
        <Trust />
        <Features />
        <Method />
        <Benefits />
        <Testimonials />
        <Pricing />
        <FAQ />
        <FinalCTA />
      </main>
      <Footer />
    </div>
  );
}
