<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#111827">

<title>Creativos One</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

:root {
    --bg: #f4f6f8;
    --card: #ffffff;
    --text: #17202a;
    --muted: #6b7280;
    --border: #e5e7eb;
    --primary: #111827;
    --primary-light: #1f2937;
    --success: #15803d;
    --warning: #b45309;
    --danger: #b91c1c;
    --blue: #1d4ed8;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
}

button {
    font-family: inherit;
    cursor: pointer;
}

.app {
    display: flex;
    min-height: 100vh;
}

/* SIDEBAR */

.sidebar {
    width: 250px;
    background: #111827;
    color: white;
    padding: 24px 16px;
    position: fixed;
    left: 0;
    top: 0;
    bottom: 0;
    z-index: 20;
}

.logo {
    padding: 8px 12px 26px;
}

.logo h1 {
    font-size: 22px;
    letter-spacing: -0.5px;
}

.logo span {
    color: #9ca3af;
    font-size: 12px;
    display: block;
    margin-top: 5px;
}

.nav-title {
    color: #6b7280;
    font-size: 11px;
    text-transform: uppercase;
    margin: 15px 12px 8px;
    letter-spacing: 1px;
}

.nav button {
    width: 100%;
    border: 0;
    background: transparent;
    color: #d1d5db;
    padding: 12px;
    border-radius: 9px;
    text-align: left;
    margin-bottom: 3px;
    font-size: 14px;
}

.nav button:hover,
.nav button.active {
    background: #1f2937;
    color: white;
}

.sidebar-footer {
    position: absolute;
    bottom: 20px;
    left: 16px;
    right: 16px;
    border-top: 1px solid #374151;
    padding: 16px 12px;
    color: #9ca3af;
    font-size: 12px;
}

/* MAIN */

.main {
    margin-left: 250px;
    width: calc(100% - 250px);
    min-height: 100vh;
}

.topbar {
    height: 72px;
    background: white;
    border-bottom: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 30px;
}

.topbar-title {
    font-size: 18px;
    font-weight: 700;
}

.user {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 13px;
}

.avatar {
    width: 36px;
    height: 36px;
    border-radius: 50%;
    background: #111827;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: bold;
}

.content {
    padding: 30px;
    max-width: 1500px;
    margin: auto;
}

.page {
    display: none;
}

.page.active {
    display: block;
}

.page-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 24px;
}

.page-header h2 {
    font-size: 25px;
}

.page-header p {
    color: var(--muted);
    font-size: 13px;
    margin-top: 5px;
}

/* BUTTONS */

.primary-btn {
    border: 0;
    background: var(--primary);
    color: white;
    padding: 11px 17px;
    border-radius: 8px;
    font-size: 13px;
    font-weight: 600;
}

.primary-btn:hover {
    background: var(--primary-light);
}

.secondary-btn {
    border: 1px solid var(--border);
    background: white;
    color: var(--text);
    padding: 10px 15px;
    border-radius: 8px;
    font-size: 13px;
}

/* CARDS */

.metrics {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 16px;
    margin-bottom: 24px;
}

.metric {
    background: white;
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
}

.metric-label {
    color: var(--muted);
    font-size: 12px;
    margin-bottom: 10px;
}

.metric-value {
    font-size: 25px;
    font-weight: 700;
}

.metric-note {
    font-size: 11px;
    margin-top: 9px;
}

.green {
    color: var(--success);
}

.orange {
    color: var(--warning);
}

.red {
    color: var(--danger);
}

.blue {
    color: var(--blue);
}

/* DASHBOARD GRID */

.dashboard-grid {
    display: grid;
    grid-template-columns: 1.5fr 1fr;
    gap: 20px;
}

.card {
    background: white;
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
}

.card-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 18px;
}

.card-header h3 {
    font-size: 15px;
}

/* TABLE */

.table-container {
    background: white;
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow-x: auto;
}

table {
    width: 100%;
    border-collapse: collapse;
    min-width: 700px;
}

th {
    text-align: left;
    color: var(--muted);
    font-size: 11px;
    font-weight: 600;
    text-transform: uppercase;
    padding: 14px 18px;
    border-bottom: 1px solid var(--border);
}

td {
    padding: 15px 18px;
    font-size: 13px;
    border-bottom: 1px solid var(--border);
}

tr:last-child td {
    border-bottom: none;
}

.status {
    display: inline-block;
    padding: 5px 9px;
    border-radius: 20px;
    font-size: 11px;
    font-weight: 600;
}

.status.green-bg {
    background: #dcfce7;
    color: #166534;
}

.status.orange-bg {
    background: #ffedd5;
    color: #9a3412;
}

.status.red-bg {
    background: #fee2e2;
    color: #991b1b;
}

.status.blue-bg {
    background: #dbeafe;
    color: #1e40af;
}

.status.gray-bg {
    background: #f3f4f6;
    color: #374151;
}

/* ALERTS */

.alert {
    padding: 14px;
    border-radius: 9px;
    margin-bottom: 10px;
    font-size: 13px;
    display: flex;
    justify-content: space-between;
    gap: 10px;
}

.alert-danger {
    background: #fef2f2;
    color: #991b1b;
}

.alert-warning {
    background: #fffbeb;
    color: #92400e;
}

.alert-info {
    background: #eff6ff;
    color: #1e40af;
}

/* QUICK ACTIONS */

.quick-actions {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 12px;
    margin-bottom: 24px;
}

.quick-action {
    border: 1px solid var(--border);
    background: white;
    border-radius: 10px;
    padding: 16px;
    text-align: left;
}

.quick-action strong {
    display: block;
    font-size: 13px;
    margin-bottom: 5px;
}

.quick-action span {
    color: var(--muted);
    font-size: 11px;
}

/* EMPTY MODULE */

.module-empty {
    background: white;
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 50px 20px;
    text-align: center;
}

.module-empty .icon {
    font-size: 35px;
    margin-bottom: 15px;
}

.module-empty h3 {
    margin-bottom: 7px;
}

.module-empty p {
    color: var(--muted);
    font-size: 13px;
}

/* MOBILE */

.mobile-header {
    display: none;
}

@media (max-width: 900px) {

    .sidebar {
        display: none;
    }

    .main {
        margin-left: 0;
        width: 100%;
    }

    .topbar {
        display: none;
    }

    .mobile-header {
        display: flex;
        height: 65px;
        background: #111827;
        color: white;
        align-items: center;
        justify-content: space-between;
        padding: 0 18px;
        position: sticky;
        top: 0;
        z-index: 30;
    }

    .mobile-header strong {
        font-size: 17px;
    }

    .mobile-menu {
        background: #1f2937;
        border: 0;
        color: white;
        padding: 9px 11px;
        border-radius: 7px;
    }

    .content {
        padding: 18px;
        padding-bottom: 90px;
    }

    .metrics {
        grid-template-columns: repeat(2, 1fr);
        gap: 10px;
    }

    .metric {
        padding: 15px;
    }

    .metric-value {
        font-size: 19px;
    }

    .dashboard-grid {
        grid-template-columns: 1fr;
    }

    .quick-actions {
        grid-template-columns: repeat(2, 1fr);
    }

    .page-header {
        align-items: flex-start;
        gap: 15px;
    }

    .page-header h2 {
        font-size: 21px;
    }
}

/* MOBILE NAV */

.mobile-nav {
    display: none;
}

@media (max-width: 900px) {

    .mobile-nav {
        display: flex;
        position: fixed;
        bottom: 0;
        left: 0;
        right: 0;
        background: white;
        border-top: 1px solid var(--border);
        height: 65px;
        z-index: 40;
        justify-content: space-around;
    }

    .mobile-nav button {
        border: 0;
        background: white;
        color: var(--muted);
        font-size: 10px;
        padding: 8px;
        min-width: 65px;
    }

    .mobile-nav button.active {
        color: #111827;
        font-weight: bold;
    }
}
</style>
</head>

<body>

<div class="app">

<!-- SIDEBAR -->

<aside class="sidebar">

    <div class="logo">
        <h1>Creativos One</h1>
        <span>Sistema empresarial v0.1</span>
    </div>

    <div class="nav-title">Principal</div>

    <nav class="nav">

        <button class="active" onclick="showPage('dashboard', this)">
            🏠 &nbsp; Inicio
        </button>

        <button onclick="showPage('clientes', this)">
            👥 &nbsp; Clientes
        </button>

        <button onclick="showPage('cotizaciones', this)">
            💰 &nbsp; Cotizaciones
        </button>

        <button onclick="showPage('pedidos', this)">
            📋 &nbsp; Pedidos
        </button>

        <button onclick="showPage('cobros', this)">
            💵 &nbsp; Cobros
        </button>

    </nav>

    <div class="nav-title">Próximamente</div>

    <nav class="nav">

        <button onclick="showPage('produccion', this)">
            🏭 &nbsp; Producción
        </button>

        <button onclick="showPage('inventario', this)">
            📦 &nbsp; Inventario
        </button>

        <button onclick="showPage('finanzas', this)">
            📊 &nbsp; Finanzas
        </button>

        <button onclick="showPage('ia', this)">
            🤖 &nbsp; IA
        </button>

    </nav>

    <div class="sidebar-footer">
        Creativos One<br>
        Construyendo una empresa, no solamente un negocio.
    </div>

</aside>

<!-- MAIN -->

<main class="main">

    <header class="mobile-header">
        <strong>Creativos One</strong>
        <button class="mobile-menu">☰</button>
    </header>

    <header class="topbar">
        <div class="topbar-title" id="topTitle">
            Inicio
        </div>

        <div class="user">
            Director
            <div class="avatar">D</div>
        </div>
    </header>

    <div class="content">

        <!-- DASHBOARD -->

        <section id="dashboard" class="page active">

            <div class="page-header">
                <div>
                    <h2>Buenos días 👋</h2>
                    <p>Este es el estado general de tu empresa.</p>
                </div>

                <button class="primary-btn"
                        onclick="showPage('cotizaciones')">
                    + Nueva cotización
                </button>
            </div>

            <div class="metrics">

                <div class="metric">
                    <div class="metric-label">Ventas del mes</div>
                    <div class="metric-value">$8.450.000</div>
                    <div class="metric-note green">
                        ↑ Meta mensual: $15.000.000
                    </div>
                </div>

                <div class="metric">
                    <div class="metric-label">Cobrado</div>
                    <div class="metric-value">$6.900.000</div>
                    <div class="metric-note green">
                        82% de las ventas
                    </div>
                </div>

                <div class="metric">
                    <div class="metric-label">Por cobrar</div>
                    <div class="metric-value">$1.550.000</div>
                    <div class="metric-note orange">
                        Requiere seguimiento
                    </div>
                </div>

                <div class="metric">
                    <div class="metric-label">Cartera vencida</div>
                    <div class="metric-value">$7.000.000</div>
                    <div class="metric-note red">
                        Atención prioritaria
                    </div>
                </div>

            </div>

            <div class="quick-actions">

                <button class="quick-action"
                        onclick="showPage('clientes')">
                    <strong>👥 Nuevo cliente</strong>
                    <span>Registrar información</span>
                </button>

                <button class="quick-action"
                        onclick="showPage('cotizaciones')">
                    <strong>💰 Cotizar</strong>
                    <span>Crear nueva cotización</span>
                </button>

                <button class="quick-action"
                        onclick="showPage('pedidos')">
                    <strong>📋 Ver pedidos</strong>
                    <span>Revisar trabajos</span>
                </button>

                <button class="quick-action"
                        onclick="showPage('cobros')">
                    <strong>💵 Cobros</strong>
                    <span>Revisar cartera</span>
                </button>

            </div>

            <div class="dashboard-grid">

                <div class="card">

                    <div class="card-header">
                        <h3>Pedidos recientes</h3>
                        <button class="secondary-btn"
                                onclick="showPage('pedidos')">
                            Ver todos
                        </button>
                    </div>

                    <div class="table-container">

                        <table>

                            <thead>
                                <tr>
                                    <th>OT</th>
                                    <th>Cliente</th>
                                    <th>Servicio</th>
                                    <th>Estado</th>
                                    <th>Total</th>
                                </tr>
                            </thead>

                            <tbody>

                                <tr>
                                    <td>OT-0048</td>
                                    <td>Empresa A</td>
                                    <td>Normativa vehicular</td>
                                    <td>
                                        <span class="status blue-bg">
                                            Producción
                                        </span>
                                    </td>
                                    <td>$1.000.000</td>
                                </tr>

                                <tr>
                                    <td>OT-0049</td>
                                    <td>Empresa B</td>
                                    <td>Aviso comercial</td>
                                    <td>
                                        <span class="status orange-bg">
                                            Diseño
                                        </span>
                                    </td>
                                    <td>$2.000.000</td>
                                </tr>

                                <tr>
                                    <td>OT-0050</td>
                                    <td>Empresa C</td>
                                    <td>Calcomanías</td>
                                    <td>
                                        <span class="status green-bg">
                                            Listo
                                        </span>
                                    </td>
                                    <td>$600.000</td>
                                </tr>

                            </tbody>

                        </table>

                    </div>

                </div>

                <div class="card">

                    <div class="card-header">
                        <h3>Alertas</h3>
                    </div>

                    <div class="alert alert-danger">
                        <span>🔴 Cliente con cartera vencida</span>
                        <strong>$4M</strong>
                    </div>

                    <div class="alert alert-danger">
                        <span>🔴 Pedido atrasado</span>
                        <strong>OT-0046</strong>
                    </div>

                    <div class="alert alert-warning">
                        <span>🟠 Cobro pendiente</span>
                        <strong>$1.2M</strong>
                    </div>

                    <div class="alert alert-info">
                        <span>🔵 5 cotizaciones requieren seguimiento</span>
                    </div>

                </div>

            </div>

        </section>


        <!-- CLIENTES -->

        <section id="clientes" class="page">

            <div class="page-header">

                <div>
                    <h2>Clientes</h2>
                    <p>Base central de clientes de la empresa.</p>
                </div>

                <button class="primary-btn">
                    + Nuevo cliente
                </button>

            </div>

            <div class="module-empty">

                <div class="icon">👥</div>

                <h3>Módulo de clientes</h3>

                <p>
                    Aquí construiremos la base de datos de clientes,
                    empresas, contactos, vehículos, historial y cartera.
                </p>

                <br>

                <button class="primary-btn">
                    Próximamente
                </button>

            </div>

        </section>


        <!-- COTIZACIONES -->

        <section id="cotizaciones" class="page">

            <div class="page-header">

                <div>
                    <h2>Cotizaciones</h2>
                    <p>Control comercial y seguimiento de oportunidades.</p>
                </div>

                <button class="primary-btn">
                    + Nueva cotización
                </button>

            </div>

            <div class="module-empty">

                <div class="icon">💰</div>

                <h3>Módulo de cotizaciones</h3>

                <p>
                    Aquí construiremos el sistema para crear,
                    enviar y hacer seguimiento a cada cotización.
                </p>

                <br>

                <button class="primary-btn">
                    Próximamente
                </button>

            </div>

        </section>


        <!-- PEDIDOS -->

        <section id="pedidos" class="page">

            <div class="page-header">

                <div>
                    <h2>Pedidos</h2>
                    <p>Trabajos vendidos y pendientes de ejecución.</p>
                </div>

                <button class="primary-btn">
                    + Nuevo pedido
                </button>

            </div>

            <div class="module-empty">

                <div class="icon">📋</div>

                <h3>Módulo de pedidos</h3>

                <p>
                    Cada cotización aprobada podrá convertirse
                    automáticamente en una orden de trabajo.
                </p>

                <br>

                <button class="primary-btn">
                    Próximamente
                </button>

            </div>

        </section>


        <!-- COBROS -->

        <section id="cobros" class="page">

            <div class="page-header">

                <div>
                    <h2>Cobros</h2>
                    <p>Anticipos, saldos y cartera.</p>
                </div>

                <button class="primary-btn">
                    + Registrar pago
                </button>

            </div>

            <div class="module-empty">

                <div class="icon">💵</div>

                <h3>Módulo de cobros</h3>

                <p>
                    El sistema calculará automáticamente cuánto debe
                    cada cliente y qué pagos están pendientes.
                </p>

                <br>

                <button class="primary-btn">
                    Próximamente
                </button>

            </div>

        </section>


        <!-- PRODUCCIÓN -->

        <section id="produccion" class="page">

            <div class="page-header">
                <div>
                    <h2>Producción</h2>
                    <p>Control de trabajos en fabricación e instalación.</p>
                </div>
            </div>

            <div class="module-empty">
                <div class="icon">🏭</div>
                <h3>Producción</h3>
                <p>Este módulo será desarrollado en la versión 0.2.</p>
            </div>

        </section>


        <!-- INVENTARIO -->

        <section id="inventario" class="page">

            <div class="page-header">
                <div>
                    <h2>Inventario</h2>
                    <p>Materiales, existencias y compras.</p>
                </div>
            </div>

            <div class="module-empty">
                <div class="icon">📦</div>
                <h3>Inventario</h3>
                <p>Este módulo será desarrollado posteriormente.</p>
            </div>

        </section>


        <!-- FINANZAS -->

        <section id="finanzas" class="page">

            <div class="page-header">
                <div>
                    <h2>Finanzas</h2>
                    <p>Control financiero de la empresa.</p>
                </div>
            </div>

            <div class="module-empty">
                <div class="icon">📊</div>
                <h3>Finanzas</h3>
                <p>Construiremos aquí costos, utilidad, caja y resultados.</p>
            </div>

        </section>


        <!-- IA -->

        <section id="ia" class="page">

            <div class="page-header">
                <div>
                    <h2>Inteligencia Artificial</h2>
                    <p>El cerebro inteligente de Creativos One.</p>
                </div>
            </div>

            <div class="module-empty">
                <div class="icon">🤖</div>
                <h3>IA de Creativos One</h3>
                <p>
                    Aquí conectaremos posteriormente asistentes,
                    análisis, automatizaciones y herramientas de IA.
                </p>
            </div>

        </section>

    </div>

</main>

</div>


<!-- MOBILE NAV -->

<nav class="mobile-nav">

    <button class="active"
            onclick="showPage('dashboard', this)">
        🏠<br>Inicio
    </button>

    <button onclick="showPage('clientes', this)">
        👥<br>Clientes
    </button>

    <button onclick="showPage('cotizaciones', this)">
        💰<br>Cotizar
    </button>

    <button onclick="showPage('pedidos', this)">
        📋<br>Pedidos
    </button>

    <button onclick="showPage('cobros', this)">
        💵<br>Cobros
    </button>

</nav>


<script>

function showPage(pageId, button) {

    const pages = document.querySelectorAll('.page');

    pages.forEach(function(page) {
        page.classList.remove('active');
    });

    const selectedPage = document.getElementById(pageId);

    if (selectedPage) {
        selectedPage.classList.add('active');
    }

    const buttons = document.querySelectorAll('.nav button, .mobile-nav button');

    buttons.forEach(function(btn) {
        btn.classList.remove('active');
    });

    if (button) {
        button.classList.add('active');
    }

    const titles = {
        dashboard: "Inicio",
        clientes: "Clientes",
        cotizaciones: "Cotizaciones",
        pedidos: "Pedidos",
        cobros: "Cobros",
        produccion: "Producción",
        inventario: "Inventario",
        finanzas: "Finanzas",
        ia: "Inteligencia Artificial"
    };

    const title = document.getElementById("topTitle");

    if (title) {
        title.textContent = titles[pageId] || "Creativos One";
    }

    window.scrollTo({
        top: 0,
        behavior: "smooth"
    });
}

</script>

</body>
</html>
