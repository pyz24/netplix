import React, { useState } from "react";
import "./App.css";

function App() {
  const [form, setForm] = useState({
    nama: "",
    wa: "",
    paket: "Paket 1 Bulan - Rp35.000",
    email: ""
  });

  const paketList = [
    { label: "Paket 1 Bulan - Rp35.000", value: "Paket 1 Bulan - Rp35.000" },
    { label: "Paket 3 Bulan - Rp90.000", value: "Paket 3 Bulan - Rp90.000" },
    { label: "Paket 1 Tahun - Rp300.000", value: "Paket 1 Tahun - Rp300.000" },
  ];

  const handleChange = (e) => {
    setForm({ ...form, [e.target.name]: e.target.value });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    const nomorAdmin = "6281125101826"; // ganti ke nomor WA kamu
    
    const pesan = `Halo min, mau order Netflix%0A%0A
Nama: ${form.nama}%0A
WA: ${form.wa}%0A
Paket: ${form.paket}%0A
Email: ${form.email}`;

    window.open(`https://wa.me/${nomorAdmin}?text=${pesan}`, "_blank");
  };

  return (
    <div className="container">
      <h1>🎬 Order Netflix</h1>
      <p className="sub">Hemat bareng, bayar ringan. Order langsung via WA</p>

      <form onSubmit={handleSubmit} className="card">
        <label>Nama Lengkap</label>
        <input type="text" name="nama" value={form.nama} onChange={handleChange} required />

        <label>Nomor WhatsApp</label>
        <input type="tel" name="wa" value={form.wa} onChange={handleChange} placeholder="628xxx" required />

        <label>Pilih Paket</label>
        <select name="paket" value={form.paket} onChange={handleChange}>
          {paketList.map((p) => (
            <option key={p.value} value={p.value}>{p.label}</option>
          ))}
        </select>

        <label>Email Netflix</label>
        <input type="email" name="email" value={form.email} onChange={handleChange} placeholder="email@gmail.com" required />

        <button type="submit">Order Sekarang</button>
      </form>

      <footer>© 2026 Netflix Order. Bukan website resmi Netflix</footer>
    </div>
  );
}

export default App;
