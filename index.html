import { useState, useEffect } from "react";

// ─── DEMO DATA (reemplaza el fetch con tu endpoint /dashboard) ───
const DEMO = {
  clientes: [
    { id: 1, telefono: "573001234567", nombre_dueno: "Laura Gómez", nombre_mascota: "Firulais", especie: "Perro", raza: "Golden Retriever", creado_en: "2026-05-01T10:23:00Z" },
    { id: 2, telefono: "573009876543", nombre_dueno: "Carlos Ruiz", nombre_mascota: "Michi", especie: "Gato", raza: "Siamés", creado_en: "2026-05-02T14:10:00Z" },
    { id: 3, telefono: "573015554433", nombre_dueno: "Ana Torres", nombre_mascota: "Rocky", especie: "Perro", raza: "Bulldog", creado_en: "2026-05-03T09:05:00Z" },
    { id: 4, telefono: "573022221111", nombre_dueno: "Mario Díaz", nombre_mascota: "Luna", especie: "Perro", raza: "Labrador", creado_en: "2026-05-04T16:40:00Z" },
    { id: 5, telefono: "573033339999", nombre_dueno: "Sofía Mora", nombre_mascota: "Nala", especie: "Gato", raza: "Persa", creado_en: "2026-05-05T08:15:00Z" },
  ],
  citas: [
    { id: 1, telefono: "573001234567", nombre_dueno: "Laura Gómez", nombre_mascota: "Firulais", servicio: "Consulta veterinaria", horario_preferido: "Sábado 10am", estado: "confirmada", tipo: "normal", creado_en: "2026-05-01T10:30:00Z" },
    { id: 2, telefono: "573009876543", nombre_dueno: "Carlos Ruiz", nombre_mascota: "Michi", servicio: "Esterilización gato", horario_preferido: "Martes 3pm", estado: "pendiente", tipo: "normal", creado_en: "2026-05-02T14:20:00Z" },
    { id: 3, telefono: "573015554433", nombre_dueno: "Ana Torres", nombre_mascota: "Rocky", servicio: "Baño medicado + Peluquería", horario_preferido: "Miércoles 11am", estado: "confirmada", tipo: "normal", creado_en: "2026-05-03T09:15:00Z" },
    { id: 4, telefono: "573022221111", nombre_dueno: "Mario Díaz", nombre_mascota: "Luna", servicio: "Castración perro 10–20kg", horario_preferido: "Domingo 7am", estado: "confirmada", tipo: "fuera_horario", creado_en: "2026-05-04T16:50:00Z" },
    { id: 5, telefono: "573033339999", nombre_dueno: "Sofía Mora", nombre_mascota: "Nala", servicio: "Profilaxis dental 0–10kg", horario_preferido: "Sábado 7pm", estado: "pendiente", tipo: "fuera_horario", creado_en: "2026-05-05T08:25:00Z" },
  ],
  pagos: [
    { id: 1, telefono: "573009876543", cita_id: 2, monto: "$20.000", estado: "pendiente", creado_en: "2026-05-02T14:22:00Z" },
    { id: 2, telefono: "573022221111", cita_id: 4, monto: "$20.000", estado: "verificado", creado_en: "2026-05-04T16:55:00Z" },
  ],
  cotizaciones: [
    { id: 1, telefono: "573001234567", servicio: "Consulta veterinaria", precio: "$60.000", tipo: "normal", creado_en: "2026-05-01T10:25:00Z" },
    { id: 2, telefono: "573009876543", servicio: "Esterilización gata", precio: "$130.000", tipo: "normal", creado_en: "2026-05-02T14:15:00Z" },
    { id: 3, telefono: "573015554433", servicio: "Baño medicado + Peluquería", precio: "$90.000", tipo: "normal", creado_en: "2026-05-03T09:10:00Z" },
    { id: 4, telefono: "573022221111", servicio: "Castración perro 10–20kg (fuera horario)", precio: "$200.000", tipo: "fuera_horario", creado_en: "2026-05-04T16:45:00Z" },
    { id: 5, telefono: "573033339999", servicio: "Profilaxis dental 0–10kg (fuera horario)", precio: "$150.000", tipo: "fuera_horario", creado_en: "2026-05-05T08:20:00Z" },
    { id: 6, telefono: "573001234567", servicio: "Examen prequirúrgico", precio: "$100.000", tipo: "normal", creado_en: "2026-05-05T11:00:00Z" },
  ],
};

// Tabla de precios fuera de horario para referencia
const PRECIOS_FUERA_HORARIO = [
  { categoria: "🔪 Castración — Orquiectomía (machos)", items: [
    { servicio: "Gatos", precio: "$150.000" },
    { servicio: "Perros 0–10 kg", precio: "$150.000" },
    { servicio: "Perros 10–20 kg", precio: "$200.000" },
    { servicio: "Perros 20–30 kg", precio: "$240.000" },
    { servicio: "Perros 30–40 kg", precio: "$300.000" },
    { servicio: "Perros +40 kg", precio: "$390.000" },
  ]},
  { categoria: "✂️ Esterilización — Ovariohisterectomía (hembras)", items: [
    { servicio: "Gatas", precio: "$200.000" },
    { servicio: "Perras 0–10 kg", precio: "$230.000" },
    { servicio: "Perras 10–20 kg", precio: "$280.000" },
    { servicio: "Perras 20–30 kg", precio: "$320.000" },
    { servicio: "Perras 30–40 kg", precio: "$360.000" },
    { servicio: "Perras +40 kg", precio: "$400.000" },
  ]},
  { categoria: "🦷 Profilaxis dental (gatos y perros)", items: [
    { servicio: "0–10 kg", precio: "$150.000" },
    { servicio: "10–20 kg", precio: "$170.000" },
    { servicio: "20–30 kg", precio: "$200.000" },
    { servicio: "30–40 kg", precio: "$250.000" },
    { servicio: "40–50 kg", precio: "$300.000" },
  ]},
  { categoria: "📷 Diagnóstico por imagen", items: [
    { servicio: "Radiografía", precio: "$180.000" },
    { servicio: "Ecografía", precio: "$180.000" },
  ]},
];

const BASE_URL = "https://pet-capital-webhook-production.up.railway.app";

const TABS = ["Resumen", "Clientes", "Citas", "Pagos", "Cotizaciones", "Fuera de Horario"];

const ESTADO_COLORS = {
  confirmada:      { bg: "#d1fae5", color: "#065f46", label: "Confirmada"       },
  pendiente:       { bg: "#fef3c7", color: "#92400e", label: "Pendiente"        },
  pendiente_pago:  { bg: "#fee9d6", color: "#9a3412", label: "Pendiente de pago" },
  cancelada:       { bg: "#fee2e2", color: "#991b1b", label: "Cancelada"        },
  verificado:      { bg: "#d1fae5", color: "#065f46", label: "Verificado"       },
};

function fmt(iso) {
  return new Date(iso).toLocaleDateString("es-CO", { day: "2-digit", month: "short", year: "numeric" });
}

function StatCard({ icon, label, value, sub, color }) {
  return (
    <div style={{ background: "#fff", borderRadius: 16, padding: "22px 24px", boxShadow: "0 2px 12px rgba(0,0,0,0.07)", borderLeft: `4px solid ${color}`, display: "flex", alignItems: "center", gap: 18, animation: "fadeUp 0.4s ease both" }}>
      <div style={{ width: 52, height: 52, borderRadius: 14, background: color + "18", display: "flex", alignItems: "center", justifyContent: "center", fontSize: 26 }}>{icon}</div>
      <div>
        <div style={{ fontSize: 28, fontWeight: 900, color: "#1a1a2e", lineHeight: 1 }}>{value}</div>
        <div style={{ fontSize: 13, fontWeight: 700, color: "#666", marginTop: 3 }}>{label}</div>
        {sub && <div style={{ fontSize: 11, color: color, fontWeight: 700, marginTop: 2 }}>{sub}</div>}
      </div>
    </div>
  );
}

function Badge({ estado }) {
  const s = ESTADO_COLORS[estado] || { bg: "#f3f4f6", color: "#374151", label: estado };
  return (
    <span style={{ background: s.bg, color: s.color, borderRadius: 20, padding: "3px 10px", fontSize: 11, fontWeight: 800, letterSpacing: 0.3 }}>{s.label}</span>
  );
}

function EmptyState({ icon, text }) {
  return (
    <div style={{ textAlign: "center", padding: "48px 0", color: "#aaa" }}>
      <div style={{ fontSize: 40, marginBottom: 12 }}>{icon}</div>
      <div style={{ fontWeight: 700, fontSize: 14 }}>{text}</div>
    </div>
  );
}

export default function Dashboard() {
  const [tab, setTab] = useState("Resumen");
  const [data, setData] = useState({ clientes: [], citas: [], cotizaciones: [], pagos: [] });
  const [search, setSearch] = useState("");
  const [loading, setLoading] = useState(true);
  const [verificando, setVerificando] = useState(null);

  const cargarDatos = () => {
    fetch(`${BASE_URL}/dashboard`)
      .then(r => r.json())
      .then(d => { setData({ pagos: [], ...d }); setLoading(false); })
      .catch(() => { setData(DEMO); setLoading(false); });
  };

  useEffect(() => { cargarDatos(); }, []);

  const verificarPago = async (pagoId) => {
    setVerificando(pagoId);
    try {
      const res = await fetch(`${BASE_URL}/pagos/${pagoId}/verificar`, { method: "POST" });
      if (!res.ok) throw new Error("No se pudo verificar el pago");
      cargarDatos();
    } catch (err) {
      alert("No se pudo verificar el pago. Intenta de nuevo.");
      console.error(err);
    } finally {
      setVerificando(null);
    }
  };

  const confirmadas = data.citas.filter(c => c.estado === "confirmada").length;
  const pendientes  = data.citas.filter(c => c.estado === "pendiente" || c.estado === "pendiente_pago").length;
  const pagosPendientes = (data.pagos || []).filter(p => p.estado === "pendiente").length;

  const filter = arr => arr.filter(r =>
    Object.values(r).some(v => String(v).toLowerCase().includes(search.toLowerCase()))
  );

  return (
    <div style={{ minHeight: "100vh", background: "#f0f4f8", fontFamily: "'Outfit', sans-serif" }}>
      <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700;800;900&display=swap" rel="stylesheet" />
      <style>{`
        @keyframes fadeUp { from { opacity:0; transform:translateY(16px) } to { opacity:1; transform:translateY(0) } }
        * { box-sizing: border-box; margin: 0; padding: 0; }
        table { border-collapse: collapse; width: 100%; }
        th { text-align: left; }
        input::placeholder { color: #bbb; }
        ::-webkit-scrollbar { height: 4px; width: 4px; }
        ::-webkit-scrollbar-thumb { background: #d1d5db; border-radius: 4px; }
      `}</style>

      {/* Sidebar */}
      <div style={{ position: "fixed", top: 0, left: 0, width: 220, height: "100vh", background: "linear-gradient(180deg, #1b5e20 0%, #2e7d32 60%, #388e3c 100%)", display: "flex", flexDirection: "column", zIndex: 100, boxShadow: "4px 0 20px rgba(0,0,0,0.12)" }}>
        <div style={{ padding: "28px 20px 20px" }}>
          <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 32 }}>
            <div style={{ width: 40, height: 40, borderRadius: 12, background: "rgba(255,255,255,0.15)", display: "flex", alignItems: "center", justifyContent: "center", fontSize: 22 }}>🐾</div>
            <div>
              <div style={{ color: "#fff", fontWeight: 900, fontSize: 15, lineHeight: 1 }}>Pet Capital</div>
              <div style={{ color: "rgba(255,255,255,0.6)", fontSize: 11, fontWeight: 600 }}>Panel IA · Admin</div>
            </div>
          </div>
          {TABS.map(t => (
            <button key={t} onClick={() => { setTab(t); setSearch(""); }}
              style={{ width: "100%", display: "flex", alignItems: "center", gap: 10, padding: "11px 14px", borderRadius: 12, border: "none", cursor: "pointer", marginBottom: 4, fontFamily: "inherit", fontWeight: tab === t ? 800 : 600, fontSize: 14, transition: "all 0.18s",
                background: tab === t ? "rgba(255,255,255,0.18)" : "transparent",
                color: tab === t ? "#fff" : "rgba(255,255,255,0.65)",
              }}>
              <span style={{ fontSize: 17 }}>{t === "Resumen" ? "📊" : t === "Clientes" ? "👥" : t === "Citas" ? "📅" : t === "Pagos" ? "🧾" : t === "Cotizaciones" ? "💰" : "🌙"}</span>
              {t}
              {t === "Pagos" && pagosPendientes > 0 && (
                <span style={{ marginLeft: "auto", background: "#ff5252", color: "#fff", borderRadius: 20, padding: "1px 7px", fontSize: 10, fontWeight: 900 }}>{pagosPendientes}</span>
              )}
            </button>
          ))}
        </div>
        <div style={{ marginTop: "auto", padding: "16px 20px", borderTop: "1px solid rgba(255,255,255,0.1)" }}>
          <div style={{ color: "rgba(255,255,255,0.5)", fontSize: 11, fontWeight: 600 }}>Agente Milo activo 🟢</div>
          <div style={{ color: "rgba(255,255,255,0.35)", fontSize: 10, marginTop: 3 }}>WhatsApp Business</div>
        </div>
      </div>

      {/* Main */}
      <div style={{ marginLeft: 220, padding: "32px 28px", minHeight: "100vh" }}>

        {/* Header */}
        <div style={{ display: "flex", alignItems: "center", justifyContent: "space-between", marginBottom: 28, animation: "fadeUp 0.3s ease" }}>
          <div>
            <h1 style={{ fontSize: 26, fontWeight: 900, color: "#1a1a2e" }}>{tab}</h1>
            <p style={{ color: "#888", fontSize: 13, fontWeight: 500, marginTop: 2 }}>
              {tab === "Resumen" && "Visión general del agente IA"}
              {tab === "Clientes" && `${data.clientes.length} clientes registrados`}
              {tab === "Citas" && `${data.citas.filter(c => c.tipo !== "fuera_horario").length} citas en horario normal`}
              {tab === "Pagos" && `${pagosPendientes} comprobantes por verificar`}
              {tab === "Cotizaciones" && `${data.cotizaciones.length} cotizaciones enviadas`}
              {tab === "Fuera de Horario" && "Tarifas y citas fuera del horario del local"}
            </p>
          </div>
          {tab !== "Resumen" && (
            <input value={search} onChange={e => setSearch(e.target.value)} placeholder={`Buscar ${tab.toLowerCase()}...`}
              style={{ padding: "10px 16px", borderRadius: 12, border: "1.5px solid #e5e7eb", fontSize: 13, fontFamily: "inherit", background: "#fff", color: "#333", width: 220, fontWeight: 500 }} />
          )}
        </div>

        {/* RESUMEN */}
        {tab === "Resumen" && (
          <div>
            <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit, minmax(200px, 1fr))", gap: 16, marginBottom: 28 }}>
              <StatCard icon="👥" label="Clientes totales" value={data.clientes.length} sub="Desde WhatsApp" color="#2e7d32" />
              <StatCard icon="📅" label="Citas confirmadas" value={confirmadas} sub={`${pendientes} pendientes`} color="#1565c0" />
              <StatCard icon="💰" label="Cotizaciones" value={data.cotizaciones.length} sub="Enviadas por Milo" color="#e65100" />
              <StatCard icon="🤖" label="Conversiones" value={`${Math.round((confirmadas/data.citas.length)*100)}%`} sub="Tasa de cierre" color="#6a1b9a" />
            </div>

            {/* Últimas citas */}
            <div style={{ background: "#fff", borderRadius: 18, boxShadow: "0 2px 12px rgba(0,0,0,0.07)", overflow: "hidden", marginBottom: 20, animation: "fadeUp 0.5s ease both" }}>
              <div style={{ padding: "18px 22px", borderBottom: "1px solid #f3f4f6", display: "flex", alignItems: "center", gap: 8 }}>
                <span style={{ fontSize: 18 }}>📅</span>
                <span style={{ fontWeight: 800, fontSize: 15, color: "#1a1a2e" }}>Últimas citas</span>
              </div>
              <div style={{ overflowX: "auto" }}>
                <table>
                  <thead>
                    <tr style={{ background: "#f9fafb" }}>
                      {["Dueño", "Mascota", "Servicio", "Horario", "Estado"].map(h => (
                        <th key={h} style={{ padding: "10px 16px", fontSize: 11, color: "#9ca3af", fontWeight: 800, letterSpacing: 0.5, textTransform: "uppercase" }}>{h}</th>
                      ))}
                    </tr>
                  </thead>
                  <tbody>
                    {data.citas.slice(0, 4).map((c, i) => (
                      <tr key={c.id} style={{ borderTop: "1px solid #f3f4f6", animation: `fadeUp ${0.3 + i * 0.07}s ease both` }}>
                        <td style={{ padding: "12px 16px", fontWeight: 700, fontSize: 13, color: "#1a1a2e" }}>{c.nombre_dueno || "—"}</td>
                        <td style={{ padding: "12px 16px", fontSize: 13, color: "#555" }}>{c.nombre_mascota} <span style={{ color: "#bbb", fontSize: 11 }}>({c.especie || ""})</span></td>
                        <td style={{ padding: "12px 16px", fontSize: 13, color: "#555" }}>{c.servicio}</td>
                        <td style={{ padding: "12px 16px", fontSize: 13, color: "#888" }}>{c.horario_preferido}</td>
                        <td style={{ padding: "12px 16px" }}><Badge estado={c.estado} /></td>
                      </tr>
                    ))}
                  </tbody>
                </table>
              </div>
            </div>

            {/* Últimas cotizaciones */}
            <div style={{ background: "#fff", borderRadius: 18, boxShadow: "0 2px 12px rgba(0,0,0,0.07)", overflow: "hidden", animation: "fadeUp 0.6s ease both" }}>
              <div style={{ padding: "18px 22px", borderBottom: "1px solid #f3f4f6", display: "flex", alignItems: "center", gap: 8 }}>
                <span style={{ fontSize: 18 }}>💰</span>
                <span style={{ fontWeight: 800, fontSize: 15, color: "#1a1a2e" }}>Últimas cotizaciones</span>
              </div>
              <div style={{ overflowX: "auto" }}>
                <table>
                  <thead>
                    <tr style={{ background: "#f9fafb" }}>
                      {["Teléfono", "Servicio", "Precio", "Fecha"].map(h => (
                        <th key={h} style={{ padding: "10px 16px", fontSize: 11, color: "#9ca3af", fontWeight: 800, letterSpacing: 0.5, textTransform: "uppercase" }}>{h}</th>
                      ))}
                    </tr>
                  </thead>
                  <tbody>
                    {data.cotizaciones.slice(0, 4).map((c, i) => (
                      <tr key={c.id} style={{ borderTop: "1px solid #f3f4f6", animation: `fadeUp ${0.35 + i * 0.07}s ease both` }}>
                        <td style={{ padding: "12px 16px", fontSize: 13, color: "#555", fontFamily: "monospace" }}>+{c.telefono}</td>
                        <td style={{ padding: "12px 16px", fontWeight: 600, fontSize: 13, color: "#1a1a2e" }}>{c.servicio}</td>
                        <td style={{ padding: "12px 16px", fontSize: 13, color: "#2e7d32", fontWeight: 800 }}>{c.precio}</td>
                        <td style={{ padding: "12px 16px", fontSize: 12, color: "#aaa" }}>{fmt(c.creado_en)}</td>
                      </tr>
                    ))}
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        )}

        {/* CLIENTES */}
        {tab === "Clientes" && (
          <div style={{ background: "#fff", borderRadius: 18, boxShadow: "0 2px 12px rgba(0,0,0,0.07)", overflow: "hidden", animation: "fadeUp 0.3s ease" }}>
            <div style={{ overflowX: "auto" }}>
              <table>
                <thead>
                  <tr style={{ background: "#f9fafb" }}>
                    {["#", "Dueño", "Mascota", "Especie / Raza", "Teléfono", "Registro"].map(h => (
                      <th key={h} style={{ padding: "12px 16px", fontSize: 11, color: "#9ca3af", fontWeight: 800, letterSpacing: 0.5, textTransform: "uppercase" }}>{h}</th>
                    ))}
                  </tr>
                </thead>
                <tbody>
                  {filter(data.clientes).length === 0
                    ? <tr><td colSpan={6}><EmptyState icon="👥" text="Sin resultados" /></td></tr>
                    : filter(data.clientes).map((c, i) => (
                      <tr key={c.id} style={{ borderTop: "1px solid #f3f4f6", animation: `fadeUp ${0.1 + i * 0.06}s ease both` }}>
                        <td style={{ padding: "13px 16px", fontSize: 12, color: "#ccc", fontWeight: 700 }}>{c.id}</td>
                        <td style={{ padding: "13px 16px" }}>
                          <div style={{ display: "flex", alignItems: "center", gap: 10 }}>
                            <div style={{ width: 34, height: 34, borderRadius: 10, background: "#e8f5e9", display: "flex", alignItems: "center", justifyContent: "center", fontSize: 16 }}>
                              {c.especie === "Gato" ? "🐱" : "🐶"}
                            </div>
                            <div>
                              <div style={{ fontWeight: 700, fontSize: 13, color: "#1a1a2e" }}>{c.nombre_dueno || "Sin nombre"}</div>
                            </div>
                          </div>
                        </td>
                        <td style={{ padding: "13px 16px", fontWeight: 600, fontSize: 13, color: "#374151" }}>{c.nombre_mascota || "—"}</td>
                        <td style={{ padding: "13px 16px", fontSize: 12, color: "#888" }}>{c.especie} {c.raza ? `· ${c.raza}` : ""}</td>
                        <td style={{ padding: "13px 16px", fontSize: 12, color: "#555", fontFamily: "monospace" }}>+{c.telefono}</td>
                        <td style={{ padding: "13px 16px", fontSize: 12, color: "#aaa" }}>{fmt(c.creado_en)}</td>
                      </tr>
                    ))}
                </tbody>
              </table>
            </div>
          </div>
        )}

        {/* CITAS */}
        {tab === "Citas" && (
          <div style={{ background: "#fff", borderRadius: 18, boxShadow: "0 2px 12px rgba(0,0,0,0.07)", overflow: "hidden", animation: "fadeUp 0.3s ease" }}>
            <div style={{ overflowX: "auto" }}>
              <table>
                <thead>
                  <tr style={{ background: "#f9fafb" }}>
                    {["Dueño", "Mascota", "Servicio", "Horario", "Estado", "Fecha"].map(h => (
                      <th key={h} style={{ padding: "12px 16px", fontSize: 11, color: "#9ca3af", fontWeight: 800, letterSpacing: 0.5, textTransform: "uppercase" }}>{h}</th>
                    ))}
                  </tr>
                </thead>
                <tbody>
                  {filter(data.citas).length === 0
                    ? <tr><td colSpan={6}><EmptyState icon="📅" text="Sin resultados" /></td></tr>
                    : filter(data.citas).map((c, i) => (
                      <tr key={c.id} style={{ borderTop: "1px solid #f3f4f6", animation: `fadeUp ${0.1 + i * 0.06}s ease both` }}>
                        <td style={{ padding: "13px 16px", fontWeight: 700, fontSize: 13, color: "#1a1a2e" }}>{c.nombre_dueno || "—"}</td>
                        <td style={{ padding: "13px 16px", fontSize: 13, color: "#374151" }}>{c.nombre_mascota || "—"}</td>
                        <td style={{ padding: "13px 16px", fontSize: 13, color: "#555" }}>{c.servicio}</td>
                        <td style={{ padding: "13px 16px", fontSize: 13, color: "#888" }}>{c.horario_preferido}</td>
                        <td style={{ padding: "13px 16px" }}><Badge estado={c.estado} /></td>
                        <td style={{ padding: "13px 16px", fontSize: 12, color: "#aaa" }}>{fmt(c.creado_en)}</td>
                      </tr>
                    ))}
                </tbody>
              </table>
            </div>
          </div>
        )}

        {/* PAGOS */}
        {tab === "Pagos" && (
          <div style={{ background: "#fff", borderRadius: 18, boxShadow: "0 2px 12px rgba(0,0,0,0.07)", overflow: "hidden", animation: "fadeUp 0.3s ease" }}>
            <div style={{ overflowX: "auto" }}>
              <table>
                <thead>
                  <tr style={{ background: "#f9fafb" }}>
                    {["Teléfono", "Cita", "Monto", "Estado", "Fecha", ""].map(h => (
                      <th key={h} style={{ padding: "12px 16px", fontSize: 11, color: "#9ca3af", fontWeight: 800, letterSpacing: 0.5, textTransform: "uppercase" }}>{h}</th>
                    ))}
                  </tr>
                </thead>
                <tbody>
                  {filter(data.pagos || []).length === 0
                    ? <tr><td colSpan={6}><EmptyState icon="🧾" text="Sin comprobantes de pago" /></td></tr>
                    : filter(data.pagos || []).map((p, i) => (
                      <tr key={p.id} style={{ borderTop: "1px solid #f3f4f6", animation: `fadeUp ${0.1 + i * 0.06}s ease both` }}>
                        <td style={{ padding: "13px 16px", fontSize: 12, color: "#555", fontFamily: "monospace" }}>+{p.telefono}</td>
                        <td style={{ padding: "13px 16px", fontSize: 13, color: "#374151" }}>{p.cita_id ? `#${p.cita_id}` : "— sin cita asociada"}</td>
                        <td style={{ padding: "13px 16px", fontWeight: 800, fontSize: 13, color: "#2e7d32" }}>{p.monto}</td>
                        <td style={{ padding: "13px 16px" }}><Badge estado={p.estado} /></td>
                        <td style={{ padding: "13px 16px", fontSize: 12, color: "#aaa" }}>{fmt(p.creado_en)}</td>
                        <td style={{ padding: "13px 16px" }}>
                          {p.estado === "pendiente" ? (
                            <button onClick={() => verificarPago(p.id)} disabled={verificando === p.id}
                              style={{ background: verificando === p.id ? "#a5d6a7" : "#2e7d32", color: "#fff", border: "none", borderRadius: 10, padding: "8px 14px", fontSize: 12, fontWeight: 800, cursor: verificando === p.id ? "default" : "pointer", fontFamily: "inherit" }}>
                              {verificando === p.id ? "Verificando..." : "✓ Verificar"}
                            </button>
                          ) : (
                            <span style={{ color: "#aaa", fontSize: 12, fontWeight: 700 }}>Ya verificado</span>
                          )}
                        </td>
                      </tr>
                    ))}
                </tbody>
              </table>
            </div>
          </div>
        )}

        {/* COTIZACIONES */}
        {tab === "Cotizaciones" && (
          <div style={{ background: "#fff", borderRadius: 18, boxShadow: "0 2px 12px rgba(0,0,0,0.07)", overflow: "hidden", animation: "fadeUp 0.3s ease" }}>
            <div style={{ overflowX: "auto" }}>
              <table>
                <thead>
                  <tr style={{ background: "#f9fafb" }}>
                    {["Teléfono", "Servicio", "Precio", "Fecha"].map(h => (
                      <th key={h} style={{ padding: "12px 16px", fontSize: 11, color: "#9ca3af", fontWeight: 800, letterSpacing: 0.5, textTransform: "uppercase" }}>{h}</th>
                    ))}
                  </tr>
                </thead>
                <tbody>
                  {filter(data.cotizaciones).length === 0
                    ? <tr><td colSpan={4}><EmptyState icon="💰" text="Sin resultados" /></td></tr>
                    : filter(data.cotizaciones).map((c, i) => (
                      <tr key={c.id} style={{ borderTop: "1px solid #f3f4f6", animation: `fadeUp ${0.1 + i * 0.06}s ease both` }}>
                        <td style={{ padding: "13px 16px", fontSize: 12, color: "#555", fontFamily: "monospace" }}>+{c.telefono}</td>
                        <td style={{ padding: "13px 16px", fontWeight: 600, fontSize: 13, color: "#1a1a2e" }}>{c.servicio}</td>
                        <td style={{ padding: "13px 16px" }}>
                          <span style={{ background: "#e8f5e9", color: "#2e7d32", borderRadius: 8, padding: "4px 10px", fontWeight: 900, fontSize: 13 }}>{c.precio}</span>
                        </td>
                        <td style={{ padding: "13px 16px", fontSize: 12, color: "#aaa" }}>{fmt(c.creado_en)}</td>
                      </tr>
                    ))}
                </tbody>
              </table>
            </div>
          </div>
        )}

        {/* FUERA DE HORARIO */}
        {tab === "Fuera de Horario" && (
          <div style={{ display: "flex", flexDirection: "column", gap: 20, animation: "fadeUp 0.3s ease" }}>
            <div style={{ background: "linear-gradient(135deg, #1a237e, #283593)", borderRadius: 16, padding: "18px 22px", display: "flex", alignItems: "center", gap: 14 }}>
              <span style={{ fontSize: 28 }}>🌙</span>
              <div>
                <div style={{ color: "#fff", fontWeight: 800, fontSize: 15 }}>Tarifas fuera del horario normal</div>
                <div style={{ color: "rgba(255,255,255,0.7)", fontSize: 12, marginTop: 3 }}>Aplican antes de las 9am · después de las 6pm (semana) · después de las 5pm (dom/festivos)</div>
              </div>
            </div>
            {PRECIOS_FUERA_HORARIO.map((cat, ci) => (
              <div key={ci} style={{ background: "#fff", borderRadius: 18, boxShadow: "0 2px 12px rgba(0,0,0,0.07)", overflow: "hidden" }}>
                <div style={{ padding: "14px 20px", background: "#f8f9ff", borderBottom: "1px solid #e8eaf6", fontWeight: 800, fontSize: 14, color: "#1a237e" }}>{cat.categoria}</div>
                <table>
                  <tbody>
                    {cat.items.map((item, ii) => (
                      <tr key={ii} style={{ borderTop: ii > 0 ? "1px solid #f3f4f6" : "none" }}>
                        <td style={{ padding: "12px 20px", fontSize: 13, color: "#374151", fontWeight: 600 }}>{item.servicio}</td>
                        <td style={{ padding: "12px 20px", textAlign: "right" }}>
                          <span style={{ background: "#e8eaf6", color: "#1a237e", borderRadius: 8, padding: "4px 12px", fontWeight: 900, fontSize: 13 }}>{item.precio}</span>
                        </td>
                      </tr>
                    ))}
                  </tbody>
                </table>
              </div>
            ))}
            <div style={{ background: "#fff", borderRadius: 18, boxShadow: "0 2px 12px rgba(0,0,0,0.07)", overflow: "hidden" }}>
              <div style={{ padding: "14px 20px", background: "#f8f9ff", borderBottom: "1px solid #e8eaf6", fontWeight: 800, fontSize: 14, color: "#1a237e" }}>📅 Citas agendadas fuera de horario</div>
              <div style={{ overflowX: "auto" }}>
                <table>
                  <thead>
                    <tr style={{ background: "#f9fafb" }}>
                      {["Dueño", "Mascota", "Servicio", "Horario", "Estado"].map(h => (
                        <th key={h} style={{ padding: "10px 16px", fontSize: 11, color: "#9ca3af", fontWeight: 800, letterSpacing: 0.5, textTransform: "uppercase" }}>{h}</th>
                      ))}
                    </tr>
                  </thead>
                  <tbody>
                    {data.citas.filter(c => c.tipo === "fuera_horario").length === 0
                      ? <tr><td colSpan={5}><EmptyState icon="🌙" text="Sin citas fuera de horario" /></td></tr>
                      : data.citas.filter(c => c.tipo === "fuera_horario").map((c, i) => (
                        <tr key={c.id} style={{ borderTop: "1px solid #f3f4f6" }}>
                          <td style={{ padding: "12px 16px", fontWeight: 700, fontSize: 13, color: "#1a1a2e" }}>{c.nombre_dueno || "—"}</td>
                          <td style={{ padding: "12px 16px", fontSize: 13, color: "#374151" }}>{c.nombre_mascota}</td>
                          <td style={{ padding: "12px 16px", fontSize: 13, color: "#555" }}>{c.servicio}</td>
                          <td style={{ padding: "12px 16px", fontSize: 13, color: "#888" }}>{c.horario_preferido}</td>
                          <td style={{ padding: "12px 16px" }}><Badge estado={c.estado} /></td>
                        </tr>
                      ))}
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        )}
      </div>
    </div>
  );
}
