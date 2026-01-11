# index.html
<!doctype html>
<html lang="fr">

<head>
  <meta charset="UTF-8" />
  <link rel="icon" type="image/svg+xml" href="vite.svg" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>MyManager - Backoffice</title>
  <link rel="stylesheet" href="index.css">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <meta property="og:image" content="https://bolt.new/static/og_default.png">
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:image" content="https://bolt.new/static/og_default.png">
</head>

<body>
  <div id="app">
    <nav class="navbar navbar-dark bg-dark fixed-top">
      <div class="container-fluid">
        <a class="navbar-brand" href="#/">
          <i class="fas fa-briefcase me-2"></i>MyManager
        </a>
        <button class="navbar-toggler d-lg-none" type="button" data-bs-toggle="offcanvas" data-bs-target="#sidebar">
          <span class="navbar-toggler-icon"></span>
        </button>
      </div>
    </nav>

    <div class="container-fluid">
      <div class="row">
        <nav id="sidebar" class="col-md-3 col-lg-2 d-md-block bg-light sidebar offcanvas-md offcanvas-start"
          tabindex="-1">
          <div class="position-sticky pt-5 mt-3">
            <ul class="nav flex-column">
              <li class="nav-item">
                <a class="nav-link" href="#/" data-route="dashboard">
                  <i class="fas fa-chart-line me-2"></i>Dashboard
                </a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#/customers" data-route="customers">
                  <i class="fas fa-users me-2"></i>Clients
                </a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#/products" data-route="products">
                  <i class="fas fa-box me-2"></i>Produits
                </a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#/orders" data-route="orders">
                  <i class="fas fa-shopping-cart me-2"></i>Commandes
                </a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#/invoices" data-route="invoices">
                  <i class="fas fa-file-invoice me-2"></i>Factures
                </a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#/users" data-route="users">
                  <i class="fas fa-user-shield me-2"></i>Utilisateurs
                </a>
              </li>
            </ul>
          </div>
        </nav>

        <main class="col-md-9 ms-sm-auto col-lg-10 px-md-4">
          <div id="content" class="pt-5 mt-4">
          </div>
        </main>
      </div>
    </div>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js"></script>
  <script type="module" src="main.js"></script>
  <script src="index.js"></script>
</body>

</html>
#index .css
body{font-family:Segoe UI,Tahoma,Geneva,Verdana,sans-serif;background-color:#f8f9fa}
.sidebar{position:fixed;top:0;bottom:0;left:0;z-index:100;padding:0;box-shadow:2px 0 5px #0000001a}
.sidebar .nav-link{font-weight:500;color:#333;padding:.75rem 1rem;border-radius:.25rem;margin:.25rem .5rem;transition:all .3s ease}
.sidebar .nav-link:hover{background-color:#e9ecef;color:#0d6efd}
.sidebar .nav-link.active{background-color:#0d6efd;color:#fff}
.sidebar .nav-link i{width:20px}
.card{border:none;border-radius:10px;box-shadow:0 2px 4px #00000014;transition:transform .2s ease,box-shadow .2s ease}
.card:hover{transform:translateY(-2px);box-shadow:0 4px 12px #00000026}
.stat-card{padding:1.5rem;background:linear-gradient(135deg,#667eea,#764ba2);color:#fff;border-radius:10px}
.stat-card.primary{background:linear-gradient(135deg,#667eea,#764ba2)}
.stat-card.success{background:linear-gradient(135deg,#11998e,#38ef7d)}
.stat-card.warning{background:linear-gradient(135deg,#f093fb,#f5576c)}
.stat-card.info{background:linear-gradient(135deg,#4facfe,#00f2fe)}
.stat-card.danger{background:linear-gradient(135deg,#fa709a,#fee140)}
.stat-card h3{font-size:2rem;font-weight:700;margin-bottom:.5rem}
.stat-card p{margin:0;opacity:.9}
.chart-container{position:relative;height:300px;margin:1rem 0}
.table-container{background:#fff;border-radius:10px;padding:1.5rem;box-shadow:0 2px 4px #00000014}
.btn{border-radius:6px;padding:.5rem 1rem;font-weight:500;transition:all .2s ease}
.btn:hover{transform:translateY(-1px);box-shadow:0 4px 8px #00000026}
.page-header{margin-bottom:2rem;padding-bottom:1rem;border-bottom:2px solid #e9ecef}
.page-header h1{font-size:2rem;font-weight:600;color:#333}
.modal-content{border-radius:10px;border:none}
.form-label{font-weight:500;color:#495057}
.form-control,.form-select{border-radius:6px;border:1px solid #ced4da;transition:all .2s ease}
.form-control:focus,.form-select:focus{border-color:#667eea;box-shadow:0 0 0 .2rem #667eea40}
.badge{padding:.4rem .8rem;font-weight:500;border-radius:6px}
.table{margin-bottom:0}
.table thead th{background-color:#f8f9fa;border-bottom:2px solid #dee2e6;color:#495057;font-weight:600;text-transform:uppercase;font-size:.85rem;letter-spacing:.5px}
.table tbody tr{transition:background-color .2s ease}
.table tbody tr:hover{background-color:#f8f9fa}
.action-buttons{display:flex;gap:.5rem}
@media (max-width: 768px){.sidebar{position:relative}
.chart-container{height:250px}
.stat-card h3{font-size:1.5rem}}
.loading-spinner{display:flex;justify-content:center;align-items:center;min-height:200px}
.empty-state{text-align:center;padding:3rem;color:#6c757d}
.empty-state i{font-size:4rem;margin-bottom:1rem;opacity:.5}
#styl.css
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f8f9fa;
}

.sidebar {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  z-index: 100;
  padding: 0;
  box-shadow: 2px 0 5px rgba(0,0,0,0.1);
}

.sidebar .nav-link {
  font-weight: 500;
  color: #333;
  padding: 0.75rem 1rem;
  border-radius: 0.25rem;
  margin: 0.25rem 0.5rem;
  transition: all 0.3s ease;
}

.sidebar .nav-link:hover {
  background-color: #e9ecef;
  color: #0d6efd;
}

.sidebar .nav-link.active {
  background-color: #0d6efd;
  color: white;
}

.sidebar .nav-link i {
  width: 20px;
}

.card {
  border: none;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.08);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.stat-card {
  padding: 1.5rem;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border-radius: 10px;
}

.stat-card.primary {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.stat-card.success {
  background: linear-gradient(135deg, #11998e 0%, #38ef7d 100%);
}

.stat-card.warning {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}

.stat-card.info {
  background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
}

.stat-card.danger {
  background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);
}

.stat-card h3 {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
}

.stat-card p {
  margin: 0;
  opacity: 0.9;
}

.chart-container {
  position: relative;
  height: 300px;
  margin: 1rem 0;
}

.table-container {
  background: white;
  border-radius: 10px;
  padding: 1.5rem;
  box-shadow: 0 2px 4px rgba(0,0,0,0.08);
}

.btn {
  border-radius: 6px;
  padding: 0.5rem 1rem;
  font-weight: 500;
  transition: all 0.2s ease;
}

.btn:hover {
  transform: translateY(-1px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.15);
}

.page-header {
  margin-bottom: 2rem;
  padding-bottom: 1rem;
  border-bottom: 2px solid #e9ecef;
}

.page-header h1 {
  font-size: 2rem;
  font-weight: 600;
  color: #333;
}

.modal-content {
  border-radius: 10px;
  border: none;
}

.form-label {
  font-weight: 500;
  color: #495057;
}

.form-control, .form-select {
  border-radius: 6px;
  border: 1px solid #ced4da;
  transition: all 0.2s ease;
}

.form-control:focus, .form-select:focus {
  border-color: #667eea;
  box-shadow: 0 0 0 0.2rem rgba(102, 126, 234, 0.25);
}

.badge {
  padding: 0.4rem 0.8rem;
  font-weight: 500;
  border-radius: 6px;
}

.table {
  margin-bottom: 0;
}

.table thead th {
  background-color: #f8f9fa;
  border-bottom: 2px solid #dee2e6;
  color: #495057;
  font-weight: 600;
  text-transform: uppercase;
  font-size: 0.85rem;
  letter-spacing: 0.5px;
}

.table tbody tr {
  transition: background-color 0.2s ease;
}

.table tbody tr:hover {
  background-color: #f8f9fa;
}

.action-buttons {
  display: flex;
  gap: 0.5rem;
}

@media (max-width: 768px) {
  .sidebar {
    position: relative;
  }

  .chart-container {
    height: 250px;
  }

  .stat-card h3 {
    font-size: 1.5rem;
  }
}

.loading-spinner {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 200px;
}

.empty-state {
  text-align: center;
  padding: 3rem;
  color: #6c757d;
}

.empty-state i {
  font-size: 4rem;
  margin-bottom: 1rem;
  opacity: 0.5;
}
#customers.js
import { supabase } from './supabase.js';

export async function renderCustomers(container) {
  container.innerHTML = `
    <div class="page-header d-flex justify-content-between align-items-center">
      <div>
        <h1><i class="fas fa-users me-2"></i>Gestion des Clients</h1>
        <p class="text-muted">Liste complète des clients</p>
      </div>
      <button class="btn btn-primary" onclick="window.addCustomer()">
        <i class="fas fa-plus me-2"></i>Nouveau Client
      </button>
    </div>

    <div class="table-container">
      <div class="mb-3">
        <input type="text" class="form-control" id="searchCustomers" placeholder="Rechercher un client...">
      </div>
      <div class="table-responsive">
        <table class="table table-hover">
          <thead>
            <tr>
              <th>Nom</th>
              <th>Email</th>
              <th>Téléphone</th>
              <th>Adresse</th>
              <th>Date de création</th>
              <th>Actions</th>
            </tr>
          </thead>
          <tbody id="customers-table-body">
            <tr>
              <td colspan="6" class="text-center">
                <div class="loading-spinner">
                  <div class="spinner-border" role="status"></div>
                </div>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>

    <div class="modal fade" id="customerModal" tabindex="-1">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="customerModalTitle">Nouveau Client</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
          </div>
          <div class="modal-body">
            <form id="customerForm">
              <input type="hidden" id="customerId">
              <div class="mb-3">
                <label for="customerName" class="form-label">Nom</label>
                <input type="text" class="form-control" id="customerName" required>
              </div>
              <div class="mb-3">
                <label for="customerEmail" class="form-label">Email</label>
                <input type="email" class="form-control" id="customerEmail" required>
              </div>
              <div class="mb-3">
                <label for="customerPhone" class="form-label">Téléphone</label>
                <input type="tel" class="form-control" id="customerPhone">
              </div>
              <div class="mb-3">
                <label for="customerAddress" class="form-label">Adresse</label>
                <textarea class="form-control" id="customerAddress" rows="2"></textarea>
              </div>
            </form>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Annuler</button>
            <button type="button" class="btn btn-primary" onclick="window.saveCustomer()">Enregistrer</button>
          </div>
        </div>
      </div>
    </div>
  `;

  await loadCustomers();
  setupSearch();
}

async function loadCustomers() {
  try {
    const { data, error } = await supabase
      .from('customers')
      .select('*')
      .order('created_at', { ascending: false });

    if (error) throw error;

    const tbody = document.getElementById('customers-table-body');

    if (data.length === 0) {
      tbody.innerHTML = `
        <tr>
          <td colspan="6">
            <div class="empty-state">
              <i class="fas fa-users"></i>
              <p>Aucun client trouvé</p>
            </div>
          </td>
        </tr>
      `;
      return;
    }

    tbody.innerHTML = data.map(customer => `
      <tr>
        <td>${customer.name}</td>
        <td>${customer.email}</td>
        <td>${customer.phone || '-'}</td>
        <td>${customer.address || '-'}</td>
        <td>${new Date(customer.created_at).toLocaleDateString('fr-FR')}</td>
        <td>
          <div class="action-buttons">
            <button class="btn btn-sm btn-info" onclick="window.editCustomer('${customer.id}')">
              <i class="fas fa-edit"></i>
            </button>
            <button class="btn btn-sm btn-danger" onclick="window.deleteCustomer('${customer.id}')">
              <i class="fas fa-trash"></i>
            </button>
          </div>
        </td>
      </tr>
    `).join('');
  } catch (error) {
    console.error('Error loading customers:', error);
  }
}

function setupSearch() {
  document.getElementById('searchCustomers').addEventListener('input', async (e) => {
    const searchTerm = e.target.value.toLowerCase();

    const { data } = await supabase
      .from('customers')
      .select('*')
      .order('created_at', { ascending: false });

    const filtered = data.filter(customer =>
      customer.name.toLowerCase().includes(searchTerm) ||
      customer.email.toLowerCase().includes(searchTerm)
    );

    const tbody = document.getElementById('customers-table-body');
    tbody.innerHTML = filtered.map(customer => `
      <tr>
        <td>${customer.name}</td>
        <td>${customer.email}</td>
        <td>${customer.phone || '-'}</td>
        <td>${customer.address || '-'}</td>
        <td>${new Date(customer.created_at).toLocaleDateString('fr-FR')}</td>
        <td>
          <div class="action-buttons">
            <button class="btn btn-sm btn-info" onclick="window.editCustomer('${customer.id}')">
              <i class="fas fa-edit"></i>
            </button>
            <button class="btn btn-sm btn-danger" onclick="window.deleteCustomer('${customer.id}')">
              <i class="fas fa-trash"></i>
            </button>
          </div>
        </td>
      </tr>
    `).join('');
  });
}

window.addCustomer = function () {
  document.getElementById('customerModalTitle').textContent = 'Nouveau Client';
  document.getElementById('customerForm').reset();
  document.getElementById('customerId').value = '';
  new bootstrap.Modal(document.getElementById('customerModal')).show();
};

window.editCustomer = async function (id) {
  const { data } = await supabase
    .from('customers')
    .select('*')
    .eq('id', id)
    .single();

  document.getElementById('customerModalTitle').textContent = 'Modifier Client';
  document.getElementById('customerId').value = data.id;
  document.getElementById('customerName').value = data.name;
  document.getElementById('customerEmail').value = data.email;
  document.getElementById('customerPhone').value = data.phone || '';
  document.getElementById('customerAddress').value = data.address || '';

  new bootstrap.Modal(document.getElementById('customerModal')).show();
};

window.saveCustomer = async function () {
  const id = document.getElementById('customerId').value;
  const customerData = {
    name: document.getElementById('customerName').value,
    email: document.getElementById('customerEmail').value,
    phone: document.getElementById('customerPhone').value,
    address: document.getElementById('customerAddress').value
  };

  try {
    if (id) {
      await supabase.from('customers').update(customerData).eq('id', id);
    } else {
      await supabase.from('customers').insert([customerData]);
    }

    bootstrap.Modal.getInstance(document.getElementById('customerModal')).hide();
    await loadCustomers();
  } catch (error) {
    console.error('Error saving customer:', error);
    alert('Erreur lors de l\'enregistrement');
  }
};

window.deleteCustomer = async function (id) {
  if (confirm('Êtes-vous sûr de vouloir supprimer ce client ?')) {
    try {
      await supabase.from('customers').delete().eq('id', id);
      await loadCustomers();
    } catch (error) {
      console.error('Error deleting customer:', error);
      alert('Erreur lors de la suppression');
    }
  }
};
#dashboard.js
import { supabase } from './supabase.js';

export async function renderDashboard(container) {
  container.innerHTML = `
    <div class="page-header">
      <h1><i class="fas fa-chart-line me-2"></i>Dashboard</h1>
      <p class="text-muted">Vue d'ensemble des statistiques</p>
    </div>

    <div class="row g-3 mb-4" id="stats-cards">
      <div class="col-md-6 col-lg-3">
        <div class="stat-card primary">
          <h3 id="total-customers">-</h3>
          <p><i class="fas fa-users me-2"></i>Total Clients</p>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="stat-card success">
          <h3 id="total-products">-</h3>
          <p><i class="fas fa-box me-2"></i>Total Produits</p>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="stat-card warning">
          <h3 id="total-orders">-</h3>
          <p><i class="fas fa-shopping-cart me-2"></i>Commandes</p>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="stat-card info">
          <h3 id="total-revenue">-</h3>
          <p><i class="fas fa-dollar-sign me-2"></i>Revenus</p>
        </div>
      </div>
    </div>

    <div class="row g-3 mb-4">
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Statut des Commandes</h5>
            <div class="chart-container">
              <canvas id="orderStatusChart"></canvas>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Répartition des Produits</h5>
            <div class="chart-container">
              <canvas id="productCategoryChart"></canvas>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="row g-3 mb-4">
      <div class="col-md-8">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Évolution des Commandes</h5>
            <div class="chart-container">
              <canvas id="ordersLineChart"></canvas>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Statut des Factures</h5>
            <div class="chart-container">
              <canvas id="invoiceStatusChart"></canvas>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="row g-3">
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Distribution du Stock</h5>
            <div class="chart-container">
              <canvas id="stockBarChart"></canvas>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Répartition des Rôles</h5>
            <div class="chart-container">
              <canvas id="userRoleChart"></canvas>
            </div>
          </div>
        </div>
      </div>
    </div>
  `;

  await loadDashboardData();
}

async function loadDashboardData() {
  try {
    const [customersRes, productsRes, ordersRes, invoicesRes, usersRes] = await Promise.all([
      supabase.from('customers').select('*', { count: 'exact' }),
      supabase.from('products').select('*'),
      supabase.from('orders').select('*'),
      supabase.from('invoices').select('*'),
      supabase.from('users').select('*')
    ]);

    const customers = customersRes.data || [];
    const products = productsRes.data || [];
    const orders = ordersRes.data || [];
    const invoices = invoicesRes.data || [];
    const users = usersRes.data || [];

    document.getElementById('total-customers').textContent = customers.length;
    document.getElementById('total-products').textContent = products.length;
    document.getElementById('total-orders').textContent = orders.length;

    const totalRevenue = orders.reduce((sum, order) => sum + parseFloat(order.total_amount || 0), 0);
    document.getElementById('total-revenue').textContent = `${totalRevenue.toFixed(2)}€`;

    renderOrderStatusChart(orders);
    renderProductCategoryChart(products);
    renderOrdersLineChart(orders);
    renderInvoiceStatusChart(invoices);
    renderStockBarChart(products);
    renderUserRoleChart(users);
  } catch (error) {
    console.error('Error loading dashboard data:', error);
  }
}

function renderOrderStatusChart(orders) {
  const statusCounts = orders.reduce((acc, order) => {
    acc[order.status] = (acc[order.status] || 0) + 1;
    return acc;
  }, {});

  const ctx = document.getElementById('orderStatusChart');
  new Chart(ctx, {
    type: 'pie',
    data: {
      labels: Object.keys(statusCounts),
      datasets: [{
        data: Object.values(statusCounts),
        backgroundColor: ['#667eea', '#11998e', '#f093fb', '#fa709a']
      }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      plugins: {
        legend: { position: 'bottom' }
      }
    }
  });
}

function renderProductCategoryChart(products) {
  const categoryCounts = products.reduce((acc, product) => {
    acc[product.category] = (acc[product.category] || 0) + 1;
    return acc;
  }, {});

  const ctx = document.getElementById('productCategoryChart');
  new Chart(ctx, {
    type: 'doughnut',
    data: {
      labels: Object.keys(categoryCounts),
      datasets: [{
        data: Object.values(categoryCounts),
        backgroundColor: ['#4facfe', '#38ef7d', '#f5576c', '#fee140', '#764ba2']
      }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      plugins: {
        legend: { position: 'bottom' }
      }
    }
  });
}

function renderOrdersLineChart(orders) {
  const monthlyData = orders.reduce((acc, order) => {
    const month = new Date(order.order_date).toLocaleDateString('fr-FR', { month: 'short' });
    acc[month] = (acc[month] || 0) + 1;
    return acc;
  }, {});

  const ctx = document.getElementById('ordersLineChart');
  new Chart(ctx, {
    type: 'line',
    data: {
      labels: Object.keys(monthlyData),
      datasets: [{
        label: 'Commandes',
        data: Object.values(monthlyData),
        borderColor: '#667eea',
        backgroundColor: 'rgba(102, 126, 234, 0.1)',
        tension: 0.4,
        fill: true
      }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      plugins: {
        legend: { display: false }
      },
      scales: {
        y: { beginAtZero: true }
      }
    }
  });
}

function renderInvoiceStatusChart(invoices) {
  const statusCounts = invoices.reduce((acc, invoice) => {
    acc[invoice.status] = (acc[invoice.status] || 0) + 1;
    return acc;
  }, {});

  const ctx = document.getElementById('invoiceStatusChart');
  new Chart(ctx, {
    type: 'polarArea',
    data: {
      labels: Object.keys(statusCounts),
      datasets: [{
        data: Object.values(statusCounts),
        backgroundColor: ['#667eea', '#11998e', '#f093fb', '#fa709a']
      }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      plugins: {
        legend: { position: 'bottom' }
      }
    }
  });
}

function renderStockBarChart(products) {
  const topProducts = products.slice(0, 5);

  const ctx = document.getElementById('stockBarChart');
  new Chart(ctx, {
    type: 'bar',
    data: {
      labels: topProducts.map(p => p.name),
      datasets: [{
        label: 'Stock',
        data: topProducts.map(p => p.stock),
        backgroundColor: '#11998e',
        borderRadius: 5
      }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      plugins: {
        legend: { display: false }
      },
      scales: {
        y: { beginAtZero: true }
      }
    }
  });
}

function renderUserRoleChart(users) {
  const roleCounts = users.reduce((acc, user) => {
    acc[user.role] = (acc[user.role] || 0) + 1;
    return acc;
  }, {});

  const ctx = document.getElementById('userRoleChart');
  new Chart(ctx, {
    type: 'radar',
    data: {
      labels: Object.keys(roleCounts),
      datasets: [{
        label: 'Utilisateurs',
        data: Object.values(roleCounts),
        backgroundColor: 'rgba(102, 126, 234, 0.2)',
        borderColor: '#667eea',
        pointBackgroundColor: '#667eea'
      }]
    },
    options: {
      responsive: true,
      maintainAspectRatio: false,
      plugins: {
        legend: { display: false }
      }
    }
  });
}
#index.js
(function(){const e=document.createElement("link").relList;if(e&&e.supports&&e.supports("modulepreload"))return;for(const n of document.querySelectorAll('link[rel="modulepreload"]'))s(n);new MutationObserver(n=>{for(const i of n)if(i.type==="childList")for(const a of i.addedNodes)a.tagName==="LINK"&&a.rel==="modulepreload"&&s(a)}).observe(document,{childList:!0,subtree:!0});function t(n){const i={};return n.integrity&&(i.integrity=n.integrity),n.referrerPolicy&&(i.referrerPolicy=n.referrerPolicy),n.crossOrigin==="use-credentials"?i.credentials="include":n.crossOrigin==="anonymous"?i.credentials="omit":i.credentials="same-origin",i}function s(n){if(n.ep)return;n.ep=!0;const i=t(n);fetch(n.href,i)}})();class Gt{constructor(e){this.routes=e,this.currentRoute=null,window.addEventListener("hashchange",()=>this.handleRoute()),window.addEventListener("load",()=>this.handleRoute())}handleRoute(){const e=window.location.hash.slice(1)||"/",t=this.routes.find(s=>s.path===e)||this.routes[0];if(this.updateActiveNavLink(e),this.currentRoute!==t){this.currentRoute=t;const s=document.getElementById("content");s.innerHTML="",t.component(s)}}updateActiveNavLink(e){document.querySelectorAll(".sidebar .nav-link").forEach(s=>{s.getAttribute("href").slice(1)===e?s.classList.add("active"):s.classList.remove("active")})}navigate(e){window.location.hash=e}}function Ae(r,e){var t={};for(var s in r)Object.prototype.hasOwnProperty.call(r,s)&&e.indexOf(s)<0&&(t[s]=r[s]);if(r!=null&&typeof Object.getOwnPropertySymbols=="function")for(var n=0,s=Object.getOwnPropertySymbols(r);n<s.length;n++)e.indexOf(s[n])<0&&Object.prototype.propertyIsEnumerable.call(r,s[n])&&(t[s[n]]=r[s[n]]);return t}function zt(r,e,t,s){function n(i){return i instanceof t?i:new t(function(a){a(i)})}return new(t||(t=Promise))(function(i,a){function o(u){try{c(s.next(u))}catch(f){a(f)}}function l(u){try{c(s.throw(u))}catch(f){a(f)}}function c(u){u.done?i(u.value):n(u.value).then(o,l)}c((s=s.apply(r,e||[])).next())})}const Yt=r=>r?(...e)=>r(...e):(...e)=>fetch(...e);class Ye extends Error{constructor(e,t="FunctionsError",s){super(e),this.name=t,this.context=s}}class Xt extends Ye{constructor(e){super("Failed to send a request to the Edge Function","FunctionsFetchError",e)}}class at extends Ye{constructor(e){super("Relay Error invoking the Edge Function","FunctionsRelayError",e)}}class ot extends Ye{constructor(e){super("Edge Function returned a non-2xx status code","FunctionsHttpError",e)}}var Le;(function(r){r.Any="any",r.ApNortheast1="ap-northeast-1",r.ApNortheast2="ap-northeast-2",r.ApSouth1="ap-south-1",r.ApSoutheast1="ap-southeast-1",r.ApSoutheast2="ap-southeast-2",r.CaCentral1="ca-central-1",r.EuCentral1="eu-central-1",r.EuWest1="eu-west-1",r.EuWest2="eu-west-2",r.EuWest3="eu-west-3",r.SaEast1="sa-east-1",r.UsEast1="us-east-1",r.UsWest1="us-west-1",r.UsWest2="us-west-2"})(Le||(Le={}));class Qt{constructor(e,{headers:t={},customFetch:s,region:n=Le.Any}={}){this.url=e,this.headers=t,this.region=n,this.fetch=Yt(s)}setAuth(e){this.headers.Authorization=`Bearer ${e}`}invoke(e){return zt(this,arguments,void 0,function*(t,s={}){var n;let i,a;try{const{headers:o,method:l,body:c,signal:u,timeout:f}=s;let d={},{region:h}=s;h||(h=this.region);const p=new URL(`${this.url}/${t}`);h&&h!=="any"&&(d["x-region"]=h,p.searchParams.set("forceFunctionRegion",h));let m;c&&(o&&!Object.prototype.hasOwnProperty.call(o,"Content-Type")||!o)?typeof Blob<"u"&&c instanceof Blob||c instanceof ArrayBuffer?(d["Content-Type"]="application/octet-stream",m=c):typeof c=="string"?(d["Content-Type"]="text/plain",m=c):typeof FormData<"u"&&c instanceof FormData?m=c:(d["Content-Type"]="application/json",m=JSON.stringify(c)):c&&typeof c!="string"&&!(typeof Blob<"u"&&c instanceof Blob)&&!(c instanceof ArrayBuffer)&&!(typeof FormData<"u"&&c instanceof FormData)?m=JSON.stringify(c):m=c;let v=u;f&&(a=new AbortController,i=setTimeout(()=>a.abort(),f),u?(v=a.signal,u.addEventListener("abort",()=>a.abort())):v=a.signal);const w=yield this.fetch(p.toString(),{method:l||"POST",headers:Object.assign(Object.assign(Object.assign({},d),this.headers),o),body:m,signal:v}).catch(x=>{throw new Xt(x)}),b=w.headers.get("x-relay-error");if(b&&b==="true")throw new at(w);if(!w.ok)throw new ot(w);let g=((n=w.headers.get("Content-Type"))!==null&&n!==void 0?n:"text/plain").split(";")[0].trim(),S;return g==="application/json"?S=yield w.json():g==="application/octet-stream"||g==="application/pdf"?S=yield w.blob():g==="text/event-stream"?S=w:g==="multipart/form-data"?S=yield w.formData():S=yield w.text(),{data:S,error:null,response:w}}catch(o){return{data:null,error:o,response:o instanceof ot||o instanceof at?o.context:void 0}}finally{i&&clearTimeout(i)}})}}var Zt=class extends Error{constructor(r){super(r.message),this.name="PostgrestError",this.details=r.details,this.hint=r.hint,this.code=r.code}},er=class{constructor(r){var e,t;this.shouldThrowOnError=!1,this.method=r.method,this.url=r.url,this.headers=new Headers(r.headers),this.schema=r.schema,this.body=r.body,this.shouldThrowOnError=(e=r.shouldThrowOnError)!==null&&e!==void 0?e:!1,this.signal=r.signal,this.isMaybeSingle=(t=r.isMaybeSingle)!==null&&t!==void 0?t:!1,r.fetch?this.fetch=r.fetch:this.fetch=fetch}throwOnError(){return this.shouldThrowOnError=!0,this}setHeader(r,e){return this.headers=new Headers(this.headers),this.headers.set(r,e),this}then(r,e){var t=this;this.schema===void 0||(["GET","HEAD"].includes(this.method)?this.headers.set("Accept-Profile",this.schema):this.headers.set("Content-Profile",this.schema)),this.method!=="GET"&&this.method!=="HEAD"&&this.headers.set("Content-Type","application/json");const s=this.fetch;let n=s(this.url.toString(),{method:this.method,headers:this.headers,body:JSON.stringify(this.body),signal:this.signal}).then(async i=>{let a=null,o=null,l=null,c=i.status,u=i.statusText;if(i.ok){var f,d;if(t.method!=="HEAD"){var h;const w=await i.text();w===""||(t.headers.get("Accept")==="text/csv"||t.headers.get("Accept")&&(!((h=t.headers.get("Accept"))===null||h===void 0)&&h.includes("application/vnd.pgrst.plan+text"))?o=w:o=JSON.parse(w))}const m=(f=t.headers.get("Prefer"))===null||f===void 0?void 0:f.match(/count=(exact|planned|estimated)/),v=(d=i.headers.get("content-range"))===null||d===void 0?void 0:d.split("/");m&&v&&v.length>1&&(l=parseInt(v[1])),t.isMaybeSingle&&t.method==="GET"&&Array.isArray(o)&&(o.length>1?(a={code:"PGRST116",details:`Results contain ${o.length} rows, application/vnd.pgrst.object+json requires 1 row`,hint:null,message:"JSON object requested, multiple (or no) rows returned"},o=null,l=null,c=406,u="Not Acceptable"):o.length===1?o=o[0]:o=null)}else{var p;const m=await i.text();try{a=JSON.parse(m),Array.isArray(a)&&i.status===404&&(o=[],a=null,c=200,u="OK")}catch{i.status===404&&m===""?(c=204,u="No Content"):a={message:m}}if(a&&t.isMaybeSingle&&(!(a==null||(p=a.details)===null||p===void 0)&&p.includes("0 rows"))&&(a=null,c=200,u="OK"),a&&t.shouldThrowOnError)throw new Zt(a)}return{error:a,data:o,count:l,status:c,statusText:u}});return this.shouldThrowOnError||(n=n.catch(i=>{var a;let o="";const l=i==null?void 0:i.cause;if(l){var c,u,f,d;const p=(c=l==null?void 0:l.message)!==null&&c!==void 0?c:"",m=(u=l==null?void 0:l.code)!==null&&u!==void 0?u:"";o=`${(f=i==null?void 0:i.name)!==null&&f!==void 0?f:"FetchError"}: ${i==null?void 0:i.message}`,o+=`

Caused by: ${(d=l==null?void 0:l.name)!==null&&d!==void 0?d:"Error"}: ${p}`,m&&(o+=` (${m})`),l!=null&&l.stack&&(o+=`
${l.stack}`)}else{var h;o=(h=i==null?void 0:i.stack)!==null&&h!==void 0?h:""}return{error:{message:`${(a=i==null?void 0:i.name)!==null&&a!==void 0?a:"FetchError"}: ${i==null?void 0:i.message}`,details:o,hint:"",code:""},data:null,count:null,status:0,statusText:""}})),n.then(r,e)}returns(){return this}overrideTypes(){return this}},tr=class extends er{select(r){let e=!1;const t=(r??"*").split("").map(s=>/\s/.test(s)&&!e?"":(s==='"'&&(e=!e),s)).join("");return this.url.searchParams.set("select",t),this.headers.append("Prefer","return=representation"),this}order(r,{ascending:e=!0,nullsFirst:t,foreignTable:s,referencedTable:n=s}={}){const i=n?`${n}.order`:"order",a=this.url.searchParams.get(i);return this.url.searchParams.set(i,`${a?`${a},`:""}${r}.${e?"asc":"desc"}${t===void 0?"":t?".nullsfirst":".nullslast"}`),this}limit(r,{foreignTable:e,referencedTable:t=e}={}){const s=typeof t>"u"?"limit":`${t}.limit`;return this.url.searchParams.set(s,`${r}`),this}range(r,e,{foreignTable:t,referencedTable:s=t}={}){const n=typeof s>"u"?"offset":`${s}.offset`,i=typeof s>"u"?"limit":`${s}.limit`;return this.url.searchParams.set(n,`${r}`),this.url.searchParams.set(i,`${e-r+1}`),this}abortSignal(r){return this.signal=r,this}single(){return this.headers.set("Accept","application/vnd.pgrst.object+json"),this}maybeSingle(){return this.method==="GET"?this.headers.set("Accept","application/json"):this.headers.set("Accept","application/vnd.pgrst.object+json"),this.isMaybeSingle=!0,this}csv(){return this.headers.set("Accept","text/csv"),this}geojson(){return this.headers.set("Accept","application/geo+json"),this}explain({analyze:r=!1,verbose:e=!1,settings:t=!1,buffers:s=!1,wal:n=!1,format:i="text"}={}){var a;const o=[r?"analyze":null,e?"verbose":null,t?"settings":null,s?"buffers":null,n?"wal":null].filter(Boolean).join("|"),l=(a=this.headers.get("Accept"))!==null&&a!==void 0?a:"application/json";return this.headers.set("Accept",`application/vnd.pgrst.plan+${i}; for="${l}"; options=${o};`),i==="json"?this:this}rollback(){return this.headers.append("Prefer","tx=rollback"),this}returns(){return this}maxAffected(r){return this.headers.append("Prefer","handling=strict"),this.headers.append("Prefer",`max-affected=${r}`),this}};const lt=new RegExp("[,()]");var ie=class extends tr{eq(r,e){return this.url.searchParams.append(r,`eq.${e}`),this}neq(r,e){return this.url.searchParams.append(r,`neq.${e}`),this}gt(r,e){return this.url.searchParams.append(r,`gt.${e}`),this}gte(r,e){return this.url.searchParams.append(r,`gte.${e}`),this}lt(r,e){return this.url.searchParams.append(r,`lt.${e}`),this}lte(r,e){return this.url.searchParams.append(r,`lte.${e}`),this}like(r,e){return this.url.searchParams.append(r,`like.${e}`),this}likeAllOf(r,e){return this.url.searchParams.append(r,`like(all).{${e.join(",")}}`),this}likeAnyOf(r,e){return this.url.searchParams.append(r,`like(any).{${e.join(",")}}`),this}ilike(r,e){return this.url.searchParams.append(r,`ilike.${e}`),this}ilikeAllOf(r,e){return this.url.searchParams.append(r,`ilike(all).{${e.join(",")}}`),this}ilikeAnyOf(r,e){return this.url.searchParams.append(r,`ilike(any).{${e.join(",")}}`),this}regexMatch(r,e){return this.url.searchParams.append(r,`match.${e}`),this}regexIMatch(r,e){return this.url.searchParams.append(r,`imatch.${e}`),this}is(r,e){return this.url.searchParams.append(r,`is.${e}`),this}isDistinct(r,e){return this.url.searchParams.append(r,`isdistinct.${e}`),this}in(r,e){const t=Array.from(new Set(e)).map(s=>typeof s=="string"&&lt.test(s)?`"${s}"`:`${s}`).join(",");return this.url.searchParams.append(r,`in.(${t})`),this}notIn(r,e){const t=Array.from(new Set(e)).map(s=>typeof s=="string"&&lt.test(s)?`"${s}"`:`${s}`).join(",");return this.url.searchParams.append(r,`not.in.(${t})`),this}contains(r,e){return typeof e=="string"?this.url.searchParams.append(r,`cs.${e}`):Array.isArray(e)?this.url.searchParams.append(r,`cs.{${e.join(",")}}`):this.url.searchParams.append(r,`cs.${JSON.stringify(e)}`),this}containedBy(r,e){return typeof e=="string"?this.url.searchParams.append(r,`cd.${e}`):Array.isArray(e)?this.url.searchParams.append(r,`cd.{${e.join(",")}}`):this.url.searchParams.append(r,`cd.${JSON.stringify(e)}`),this}rangeGt(r,e){return this.url.searchParams.append(r,`sr.${e}`),this}rangeGte(r,e){return this.url.searchParams.append(r,`nxl.${e}`),this}rangeLt(r,e){return this.url.searchParams.append(r,`sl.${e}`),this}rangeLte(r,e){return this.url.searchParams.append(r,`nxr.${e}`),this}rangeAdjacent(r,e){return this.url.searchParams.append(r,`adj.${e}`),this}overlaps(r,e){return typeof e=="string"?this.url.searchParams.append(r,`ov.${e}`):this.url.searchParams.append(r,`ov.{${e.join(",")}}`),this}textSearch(r,e,{config:t,type:s}={}){let n="";s==="plain"?n="pl":s==="phrase"?n="ph":s==="websearch"&&(n="w");const i=t===void 0?"":`(${t})`;return this.url.searchParams.append(r,`${n}fts${i}.${e}`),this}match(r){return Object.entries(r).forEach(([e,t])=>{this.url.searchParams.append(e,`eq.${t}`)}),this}not(r,e,t){return this.url.searchParams.append(r,`not.${e}.${t}`),this}or(r,{foreignTable:e,referencedTable:t=e}={}){const s=t?`${t}.or`:"or";return this.url.searchParams.append(s,`(${r})`),this}filter(r,e,t){return this.url.searchParams.append(r,`${e}.${t}`),this}},rr=class{constructor(r,{headers:e={},schema:t,fetch:s}){this.url=r,this.headers=new Headers(e),this.schema=t,this.fetch=s}cloneRequestState(){return{url:new URL(this.url.toString()),headers:new Headers(this.headers)}}select(r,e){const{head:t=!1,count:s}=e??{},n=t?"HEAD":"GET";let i=!1;const a=(r??"*").split("").map(c=>/\s/.test(c)&&!i?"":(c==='"'&&(i=!i),c)).join(""),{url:o,headers:l}=this.cloneRequestState();return o.searchParams.set("select",a),s&&l.append("Prefer",`count=${s}`),new ie({method:n,url:o,headers:l,schema:this.schema,fetch:this.fetch})}insert(r,{count:e,defaultToNull:t=!0}={}){var s;const n="POST",{url:i,headers:a}=this.cloneRequestState();if(e&&a.append("Prefer",`count=${e}`),t||a.append("Prefer","missing=default"),Array.isArray(r)){const o=r.reduce((l,c)=>l.concat(Object.keys(c)),[]);if(o.length>0){const l=[...new Set(o)].map(c=>`"${c}"`);i.searchParams.set("columns",l.join(","))}}return new ie({method:n,url:i,headers:a,schema:this.schema,body:r,fetch:(s=this.fetch)!==null&&s!==void 0?s:fetch})}upsert(r,{onConflict:e,ignoreDuplicates:t=!1,count:s,defaultToNull:n=!0}={}){var i;const a="POST",{url:o,headers:l}=this.cloneRequestState();if(l.append("Prefer",`resolution=${t?"ignore":"merge"}-duplicates`),e!==void 0&&o.searchParams.set("on_conflict",e),s&&l.append("Prefer",`count=${s}`),n||l.append("Prefer","missing=default"),Array.isArray(r)){const c=r.reduce((u,f)=>u.concat(Object.keys(f)),[]);if(c.length>0){const u=[...new Set(c)].map(f=>`"${f}"`);o.searchParams.set("columns",u.join(","))}}return new ie({method:a,url:o,headers:l,schema:this.schema,body:r,fetch:(i=this.fetch)!==null&&i!==void 0?i:fetch})}update(r,{count:e}={}){var t;const s="PATCH",{url:n,headers:i}=this.cloneRequestState();return e&&i.append("Prefer",`count=${e}`),new ie({method:s,url:n,headers:i,schema:this.schema,body:r,fetch:(t=this.fetch)!==null&&t!==void 0?t:fetch})}delete({count:r}={}){var e;const t="DELETE",{url:s,headers:n}=this.cloneRequestState();return r&&n.append("Prefer",`count=${r}`),new ie({method:t,url:s,headers:n,schema:this.schema,fetch:(e=this.fetch)!==null&&e!==void 0?e:fetch})}},sr=class It{constructor(e,{headers:t={},schema:s,fetch:n}={}){this.url=e,this.headers=new Headers(t),this.schemaName=s,this.fetch=n}from(e){if(!e||typeof e!="string"||e.trim()==="")throw new Error("Invalid relation name: relation must be a non-empty string.");return new rr(new URL(`${this.url}/${e}`),{headers:new Headers(this.headers),schema:this.schemaName,fetch:this.fetch})}schema(e){return new It(this.url,{headers:this.headers,schema:e,fetch:this.fetch})}rpc(e,t={},{head:s=!1,get:n=!1,count:i}={}){var a;let o;const l=new URL(`${this.url}/rpc/${e}`);let c;const u=h=>h!==null&&typeof h=="object"&&(!Array.isArray(h)||h.some(u)),f=s&&Object.values(t).some(u);f?(o="POST",c=t):s||n?(o=s?"HEAD":"GET",Object.entries(t).filter(([h,p])=>p!==void 0).map(([h,p])=>[h,Array.isArray(p)?`{${p.join(",")}}`:`${p}`]).forEach(([h,p])=>{l.searchParams.append(h,p)})):(o="POST",c=t);const d=new Headers(this.headers);return f?d.set("Prefer",i?`count=${i},return=minimal`:"return=minimal"):i&&d.set("Prefer",`count=${i}`),new ie({method:o,url:l,headers:d,schema:this.schemaName,body:c,fetch:(a=this.fetch)!==null&&a!==void 0?a:fetch})}};class nr{constructor(){}static detectEnvironment(){var e;if(typeof WebSocket<"u")return{type:"native",constructor:WebSocket};if(typeof globalThis<"u"&&typeof globalThis.WebSocket<"u")return{type:"native",constructor:globalThis.WebSocket};if(typeof global<"u"&&typeof global.WebSocket<"u")return{type:"native",constructor:global.WebSocket};if(typeof globalThis<"u"&&typeof globalThis.WebSocketPair<"u"&&typeof globalThis.WebSocket>"u")return{type:"cloudflare",error:"Cloudflare Workers detected. WebSocket clients are not supported in Cloudflare Workers.",workaround:"Use Cloudflare Workers WebSocket API for server-side WebSocket handling, or deploy to a different runtime."};if(typeof globalThis<"u"&&globalThis.EdgeRuntime||typeof navigator<"u"&&(!((e=navigator.userAgent)===null||e===void 0)&&e.includes("Vercel-Edge")))return{type:"unsupported",error:"Edge runtime detected (Vercel Edge/Netlify Edge). WebSockets are not supported in edge functions.",workaround:"Use serverless functions or a different deployment target for WebSocket functionality."};const t=globalThis.process;if(t){const s=t.versions;if(s&&s.node){const n=s.node,i=parseInt(n.replace(/^v/,"").split(".")[0]);return i>=22?typeof globalThis.WebSocket<"u"?{type:"native",constructor:globalThis.WebSocket}:{type:"unsupported",error:`Node.js ${i} detected but native WebSocket not found.`,workaround:"Provide a WebSocket implementation via the transport option."}:{type:"unsupported",error:`Node.js ${i} detected without native WebSocket support.`,workaround:`For Node.js < 22, install "ws" package and provide it via the transport option:
import ws from "ws"
new RealtimeClient(url, { transport: ws })`}}}return{type:"unsupported",error:"Unknown JavaScript runtime without WebSocket support.",workaround:"Ensure you're running in a supported environment (browser, Node.js, Deno) or provide a custom WebSocket implementation."}}static getWebSocketConstructor(){const e=this.detectEnvironment();if(e.constructor)return e.constructor;let t=e.error||"WebSocket not supported in this environment.";throw e.workaround&&(t+=`

Suggested solution: ${e.workaround}`),new Error(t)}static createWebSocket(e,t){const s=this.getWebSocketConstructor();return new s(e,t)}static isWebSocketSupported(){try{const e=this.detectEnvironment();return e.type==="native"||e.type==="ws"}catch{return!1}}}const ir="2.90.1",ar=`realtime-js/${ir}`,Ct="1.0.0",or="2.0.0",ct=Ct,qe=1e4,lr=1e3,cr=100;var V;(function(r){r[r.connecting=0]="connecting",r[r.open=1]="open",r[r.closing=2]="closing",r[r.closed=3]="closed"})(V||(V={}));var $;(function(r){r.closed="closed",r.errored="errored",r.joined="joined",r.joining="joining",r.leaving="leaving"})($||($={}));var q;(function(r){r.close="phx_close",r.error="phx_error",r.join="phx_join",r.reply="phx_reply",r.leave="phx_leave",r.access_token="access_token"})(q||(q={}));var Me;(function(r){r.websocket="websocket"})(Me||(Me={}));var Y;(function(r){r.Connecting="connecting",r.Open="open",r.Closing="closing",r.Closed="closed"})(Y||(Y={}));class ur{constructor(e){this.HEADER_LENGTH=1,this.USER_BROADCAST_PUSH_META_LENGTH=6,this.KINDS={userBroadcastPush:3,userBroadcast:4},this.BINARY_ENCODING=0,this.JSON_ENCODING=1,this.BROADCAST_EVENT="broadcast",this.allowedMetadataKeys=[],this.allowedMetadataKeys=e??[]}encode(e,t){if(e.event===this.BROADCAST_EVENT&&!(e.payload instanceof ArrayBuffer)&&typeof e.payload.event=="string")return t(this._binaryEncodeUserBroadcastPush(e));let s=[e.join_ref,e.ref,e.topic,e.event,e.payload];return t(JSON.stringify(s))}_binaryEncodeUserBroadcastPush(e){var t;return this._isArrayBuffer((t=e.payload)===null||t===void 0?void 0:t.payload)?this._encodeBinaryUserBroadcastPush(e):this._encodeJsonUserBroadcastPush(e)}_encodeBinaryUserBroadcastPush(e){var t,s;const n=(s=(t=e.payload)===null||t===void 0?void 0:t.payload)!==null&&s!==void 0?s:new ArrayBuffer(0);return this._encodeUserBroadcastPush(e,this.BINARY_ENCODING,n)}_encodeJsonUserBroadcastPush(e){var t,s;const n=(s=(t=e.payload)===null||t===void 0?void 0:t.payload)!==null&&s!==void 0?s:{},a=new TextEncoder().encode(JSON.stringify(n)).buffer;return this._encodeUserBroadcastPush(e,this.JSON_ENCODING,a)}_encodeUserBroadcastPush(e,t,s){var n,i;const a=e.topic,o=(n=e.ref)!==null&&n!==void 0?n:"",l=(i=e.join_ref)!==null&&i!==void 0?i:"",c=e.payload.event,u=this.allowedMetadataKeys?this._pick(e.payload,this.allowedMetadataKeys):{},f=Object.keys(u).length===0?"":JSON.stringify(u);if(l.length>255)throw new Error(`joinRef length ${l.length} exceeds maximum of 255`);if(o.length>255)throw new Error(`ref length ${o.length} exceeds maximum of 255`);if(a.length>255)throw new Error(`topic length ${a.length} exceeds maximum of 255`);if(c.length>255)throw new Error(`userEvent length ${c.length} exceeds maximum of 255`);if(f.length>255)throw new Error(`metadata length ${f.length} exceeds maximum of 255`);const d=this.USER_BROADCAST_PUSH_META_LENGTH+l.length+o.length+a.length+c.length+f.length,h=new ArrayBuffer(this.HEADER_LENGTH+d);let p=new DataView(h),m=0;p.setUint8(m++,this.KINDS.userBroadcastPush),p.setUint8(m++,l.length),p.setUint8(m++,o.length),p.setUint8(m++,a.length),p.setUint8(m++,c.length),p.setUint8(m++,f.length),p.setUint8(m++,t),Array.from(l,w=>p.setUint8(m++,w.charCodeAt(0))),Array.from(o,w=>p.setUint8(m++,w.charCodeAt(0))),Array.from(a,w=>p.setUint8(m++,w.charCodeAt(0))),Array.from(c,w=>p.setUint8(m++,w.charCodeAt(0))),Array.from(f,w=>p.setUint8(m++,w.charCodeAt(0)));var v=new Uint8Array(h.byteLength+s.byteLength);return v.set(new Uint8Array(h),0),v.set(new Uint8Array(s),h.byteLength),v.buffer}decode(e,t){if(this._isArrayBuffer(e)){let s=this._binaryDecode(e);return t(s)}if(typeof e=="string"){const s=JSON.parse(e),[n,i,a,o,l]=s;return t({join_ref:n,ref:i,topic:a,event:o,payload:l})}return t({})}_binaryDecode(e){const t=new DataView(e),s=t.getUint8(0),n=new TextDecoder;switch(s){case this.KINDS.userBroadcast:return this._decodeUserBroadcast(e,t,n)}}_decodeUserBroadcast(e,t,s){const n=t.getUint8(1),i=t.getUint8(2),a=t.getUint8(3),o=t.getUint8(4);let l=this.HEADER_LENGTH+4;const c=s.decode(e.slice(l,l+n));l=l+n;const u=s.decode(e.slice(l,l+i));l=l+i;const f=s.decode(e.slice(l,l+a));l=l+a;const d=e.slice(l,e.byteLength),h=o===this.JSON_ENCODING?JSON.parse(s.decode(d)):d,p={type:this.BROADCAST_EVENT,event:u,payload:h};return a>0&&(p.meta=JSON.parse(f)),{join_ref:null,ref:null,topic:c,event:this.BROADCAST_EVENT,payload:p}}_isArrayBuffer(e){var t;return e instanceof ArrayBuffer||((t=e==null?void 0:e.constructor)===null||t===void 0?void 0:t.name)==="ArrayBuffer"}_pick(e,t){return!e||typeof e!="object"?{}:Object.fromEntries(Object.entries(e).filter(([s])=>t.includes(s)))}}class $t{constructor(e,t){this.callback=e,this.timerCalc=t,this.timer=void 0,this.tries=0,this.callback=e,this.timerCalc=t}reset(){this.tries=0,clearTimeout(this.timer),this.timer=void 0}scheduleTimeout(){clearTimeout(this.timer),this.timer=setTimeout(()=>{this.tries=this.tries+1,this.callback()},this.timerCalc(this.tries+1))}}var O;(function(r){r.abstime="abstime",r.bool="bool",r.date="date",r.daterange="daterange",r.float4="float4",r.float8="float8",r.int2="int2",r.int4="int4",r.int4range="int4range",r.int8="int8",r.int8range="int8range",r.json="json",r.jsonb="jsonb",r.money="money",r.numeric="numeric",r.oid="oid",r.reltime="reltime",r.text="text",r.time="time",r.timestamp="timestamp",r.timestamptz="timestamptz",r.timetz="timetz",r.tsrange="tsrange",r.tstzrange="tstzrange"})(O||(O={}));const ut=(r,e,t={})=>{var s;const n=(s=t.skipTypes)!==null&&s!==void 0?s:[];return e?Object.keys(e).reduce((i,a)=>(i[a]=dr(a,r,e,n),i),{}):{}},dr=(r,e,t,s)=>{const n=e.find(o=>o.name===r),i=n==null?void 0:n.type,a=t[r];return i&&!s.includes(i)?Pt(i,a):Fe(a)},Pt=(r,e)=>{if(r.charAt(0)==="_"){const t=r.slice(1,r.length);return mr(e,t)}switch(r){case O.bool:return hr(e);case O.float4:case O.float8:case O.int2:case O.int4:case O.int8:case O.numeric:case O.oid:return fr(e);case O.json:case O.jsonb:return pr(e);case O.timestamp:return gr(e);case O.abstime:case O.date:case O.daterange:case O.int4range:case O.int8range:case O.money:case O.reltime:case O.text:case O.time:case O.timestamptz:case O.timetz:case O.tsrange:case O.tstzrange:return Fe(e);default:return Fe(e)}},Fe=r=>r,hr=r=>{switch(r){case"t":return!0;case"f":return!1;default:return r}},fr=r=>{if(typeof r=="string"){const e=parseFloat(r);if(!Number.isNaN(e))return e}return r},pr=r=>{if(typeof r=="string")try{return JSON.parse(r)}catch{return r}return r},mr=(r,e)=>{if(typeof r!="string")return r;const t=r.length-1,s=r[t];if(r[0]==="{"&&s==="}"){let i;const a=r.slice(1,t);try{i=JSON.parse("["+a+"]")}catch{i=a?a.split(","):[]}return i.map(o=>Pt(e,o))}return r},gr=r=>typeof r=="string"?r.replace(" ","T"):r,jt=r=>{const e=new URL(r);return e.protocol=e.protocol.replace(/^ws/i,"http"),e.pathname=e.pathname.replace(/\/+$/,"").replace(/\/socket\/websocket$/i,"").replace(/\/socket$/i,"").replace(/\/websocket$/i,""),e.pathname===""||e.pathname==="/"?e.pathname="/api/broadcast":e.pathname=e.pathname+"/api/broadcast",e.href};class Ce{constructor(e,t,s={},n=qe){this.channel=e,this.event=t,this.payload=s,this.timeout=n,this.sent=!1,this.timeoutTimer=void 0,this.ref="",this.receivedResp=null,this.recHooks=[],this.refEvent=null}resend(e){this.timeout=e,this._cancelRefEvent(),this.ref="",this.refEvent=null,this.receivedResp=null,this.sent=!1,this.send()}send(){this._hasReceived("timeout")||(this.startTimeout(),this.sent=!0,this.channel.socket.push({topic:this.channel.topic,event:this.event,payload:this.payload,ref:this.ref,join_ref:this.channel._joinRef()}))}updatePayload(e){this.payload=Object.assign(Object.assign({},this.payload),e)}receive(e,t){var s;return this._hasReceived(e)&&t((s=this.receivedResp)===null||s===void 0?void 0:s.response),this.recHooks.push({status:e,callback:t}),this}startTimeout(){if(this.timeoutTimer)return;this.ref=this.channel.socket._makeRef(),this.refEvent=this.channel._replyEventName(this.ref);const e=t=>{this._cancelRefEvent(),this._cancelTimeout(),this.receivedResp=t,this._matchReceive(t)};this.channel._on(this.refEvent,{},e),this.timeoutTimer=setTimeout(()=>{this.trigger("timeout",{})},this.timeout)}trigger(e,t){this.refEvent&&this.channel._trigger(this.refEvent,{status:e,response:t})}destroy(){this._cancelRefEvent(),this._cancelTimeout()}_cancelRefEvent(){this.refEvent&&this.channel._off(this.refEvent,{})}_cancelTimeout(){clearTimeout(this.timeoutTimer),this.timeoutTimer=void 0}_matchReceive({status:e,response:t}){this.recHooks.filter(s=>s.status===e).forEach(s=>s.callback(t))}_hasReceived(e){return this.receivedResp&&this.receivedResp.status===e}}var dt;(function(r){r.SYNC="sync",r.JOIN="join",r.LEAVE="leave"})(dt||(dt={}));class de{constructor(e,t){this.channel=e,this.state={},this.pendingDiffs=[],this.joinRef=null,this.enabled=!1,this.caller={onJoin:()=>{},onLeave:()=>{},onSync:()=>{}};const s=(t==null?void 0:t.events)||{state:"presence_state",diff:"presence_diff"};this.channel._on(s.state,{},n=>{const{onJoin:i,onLeave:a,onSync:o}=this.caller;this.joinRef=this.channel._joinRef(),this.state=de.syncState(this.state,n,i,a),this.pendingDiffs.forEach(l=>{this.state=de.syncDiff(this.state,l,i,a)}),this.pendingDiffs=[],o()}),this.channel._on(s.diff,{},n=>{const{onJoin:i,onLeave:a,onSync:o}=this.caller;this.inPendingSyncState()?this.pendingDiffs.push(n):(this.state=de.syncDiff(this.state,n,i,a),o())}),this.onJoin((n,i,a)=>{this.channel._trigger("presence",{event:"join",key:n,currentPresences:i,newPresences:a})}),this.onLeave((n,i,a)=>{this.channel._trigger("presence",{event:"leave",key:n,currentPresences:i,leftPresences:a})}),this.onSync(()=>{this.channel._trigger("presence",{event:"sync"})})}static syncState(e,t,s,n){const i=this.cloneDeep(e),a=this.transformState(t),o={},l={};return this.map(i,(c,u)=>{a[c]||(l[c]=u)}),this.map(a,(c,u)=>{const f=i[c];if(f){const d=u.map(v=>v.presence_ref),h=f.map(v=>v.presence_ref),p=u.filter(v=>h.indexOf(v.presence_ref)<0),m=f.filter(v=>d.indexOf(v.presence_ref)<0);p.length>0&&(o[c]=p),m.length>0&&(l[c]=m)}else o[c]=u}),this.syncDiff(i,{joins:o,leaves:l},s,n)}static syncDiff(e,t,s,n){const{joins:i,leaves:a}={joins:this.transformState(t.joins),leaves:this.transformState(t.leaves)};return s||(s=()=>{}),n||(n=()=>{}),this.map(i,(o,l)=>{var c;const u=(c=e[o])!==null&&c!==void 0?c:[];if(e[o]=this.cloneDeep(l),u.length>0){const f=e[o].map(h=>h.presence_ref),d=u.filter(h=>f.indexOf(h.presence_ref)<0);e[o].unshift(...d)}s(o,u,l)}),this.map(a,(o,l)=>{let c=e[o];if(!c)return;const u=l.map(f=>f.presence_ref);c=c.filter(f=>u.indexOf(f.presence_ref)<0),e[o]=c,n(o,c,l),c.length===0&&delete e[o]}),e}static map(e,t){return Object.getOwnPropertyNames(e).map(s=>t(s,e[s]))}static transformState(e){return e=this.cloneDeep(e),Object.getOwnPropertyNames(e).reduce((t,s)=>{const n=e[s];return"metas"in n?t[s]=n.metas.map(i=>(i.presence_ref=i.phx_ref,delete i.phx_ref,delete i.phx_ref_prev,i)):t[s]=n,t},{})}static cloneDeep(e){return JSON.parse(JSON.stringify(e))}onJoin(e){this.caller.onJoin=e}onLeave(e){this.caller.onLeave=e}onSync(e){this.caller.onSync=e}inPendingSyncState(){return!this.joinRef||this.joinRef!==this.channel._joinRef()}}var ht;(function(r){r.ALL="*",r.INSERT="INSERT",r.UPDATE="UPDATE",r.DELETE="DELETE"})(ht||(ht={}));var he;(function(r){r.BROADCAST="broadcast",r.PRESENCE="presence",r.POSTGRES_CHANGES="postgres_changes",r.SYSTEM="system"})(he||(he={}));var F;(function(r){r.SUBSCRIBED="SUBSCRIBED",r.TIMED_OUT="TIMED_OUT",r.CLOSED="CLOSED",r.CHANNEL_ERROR="CHANNEL_ERROR"})(F||(F={}));class le{constructor(e,t={config:{}},s){var n,i;if(this.topic=e,this.params=t,this.socket=s,this.bindings={},this.state=$.closed,this.joinedOnce=!1,this.pushBuffer=[],this.subTopic=e.replace(/^realtime:/i,""),this.params.config=Object.assign({broadcast:{ack:!1,self:!1},presence:{key:"",enabled:!1},private:!1},t.config),this.timeout=this.socket.timeout,this.joinPush=new Ce(this,q.join,this.params,this.timeout),this.rejoinTimer=new $t(()=>this._rejoinUntilConnected(),this.socket.reconnectAfterMs),this.joinPush.receive("ok",()=>{this.state=$.joined,this.rejoinTimer.reset(),this.pushBuffer.forEach(a=>a.send()),this.pushBuffer=[]}),this._onClose(()=>{this.rejoinTimer.reset(),this.socket.log("channel",`close ${this.topic} ${this._joinRef()}`),this.state=$.closed,this.socket._remove(this)}),this._onError(a=>{this._isLeaving()||this._isClosed()||(this.socket.log("channel",`error ${this.topic}`,a),this.state=$.errored,this.rejoinTimer.scheduleTimeout())}),this.joinPush.receive("timeout",()=>{this._isJoining()&&(this.socket.log("channel",`timeout ${this.topic}`,this.joinPush.timeout),this.state=$.errored,this.rejoinTimer.scheduleTimeout())}),this.joinPush.receive("error",a=>{this._isLeaving()||this._isClosed()||(this.socket.log("channel",`error ${this.topic}`,a),this.state=$.errored,this.rejoinTimer.scheduleTimeout())}),this._on(q.reply,{},(a,o)=>{this._trigger(this._replyEventName(o),a)}),this.presence=new de(this),this.broadcastEndpointURL=jt(this.socket.endPoint),this.private=this.params.config.private||!1,!this.private&&(!((i=(n=this.params.config)===null||n===void 0?void 0:n.broadcast)===null||i===void 0)&&i.replay))throw`tried to use replay on public channel '${this.topic}'. It must be a private channel.`}subscribe(e,t=this.timeout){var s,n,i;if(this.socket.isConnected()||this.socket.connect(),this.state==$.closed){const{config:{broadcast:a,presence:o,private:l}}=this.params,c=(n=(s=this.bindings.postgres_changes)===null||s===void 0?void 0:s.map(h=>h.filter))!==null&&n!==void 0?n:[],u=!!this.bindings[he.PRESENCE]&&this.bindings[he.PRESENCE].length>0||((i=this.params.config.presence)===null||i===void 0?void 0:i.enabled)===!0,f={},d={broadcast:a,presence:Object.assign(Object.assign({},o),{enabled:u}),postgres_changes:c,private:l};this.socket.accessTokenValue&&(f.access_token=this.socket.accessTokenValue),this._onError(h=>e==null?void 0:e(F.CHANNEL_ERROR,h)),this._onClose(()=>e==null?void 0:e(F.CLOSED)),this.updateJoinPayload(Object.assign({config:d},f)),this.joinedOnce=!0,this._rejoin(t),this.joinPush.receive("ok",async({postgres_changes:h})=>{var p;if(this.socket._isManualToken()||this.socket.setAuth(),h===void 0){e==null||e(F.SUBSCRIBED);return}else{const m=this.bindings.postgres_changes,v=(p=m==null?void 0:m.length)!==null&&p!==void 0?p:0,w=[];for(let b=0;b<v;b++){const g=m[b],{filter:{event:S,schema:x,table:T,filter:A}}=g,K=h&&h[b];if(K&&K.event===S&&le.isFilterValueEqual(K.schema,x)&&le.isFilterValueEqual(K.table,T)&&le.isFilterValueEqual(K.filter,A))w.push(Object.assign(Object.assign({},g),{id:K.id}));else{this.unsubscribe(),this.state=$.errored,e==null||e(F.CHANNEL_ERROR,new Error("mismatch between server and client bindings for postgres changes"));return}}this.bindings.postgres_changes=w,e&&e(F.SUBSCRIBED);return}}).receive("error",h=>{this.state=$.errored,e==null||e(F.CHANNEL_ERROR,new Error(JSON.stringify(Object.values(h).join(", ")||"error")))}).receive("timeout",()=>{e==null||e(F.TIMED_OUT)})}return this}presenceState(){return this.presence.state}async track(e,t={}){return await this.send({type:"presence",event:"track",payload:e},t.timeout||this.timeout)}async untrack(e={}){return await this.send({type:"presence",event:"untrack"},e)}on(e,t,s){return this.state===$.joined&&e===he.PRESENCE&&(this.socket.log("channel",`resubscribe to ${this.topic} due to change in presence callbacks on joined channel`),this.unsubscribe().then(async()=>await this.subscribe())),this._on(e,t,s)}async httpSend(e,t,s={}){var n;if(t==null)return Promise.reject("Payload is required for httpSend()");const i={apikey:this.socket.apiKey?this.socket.apiKey:"","Content-Type":"application/json"};this.socket.accessTokenValue&&(i.Authorization=`Bearer ${this.socket.accessTokenValue}`);const a={method:"POST",headers:i,body:JSON.stringify({messages:[{topic:this.subTopic,event:e,payload:t,private:this.private}]})},o=await this._fetchWithTimeout(this.broadcastEndpointURL,a,(n=s.timeout)!==null&&n!==void 0?n:this.timeout);if(o.status===202)return{success:!0};let l=o.statusText;try{const c=await o.json();l=c.error||c.message||l}catch{}return Promise.reject(new Error(l))}async send(e,t={}){var s,n;if(!this._canPush()&&e.type==="broadcast"){console.warn("Realtime send() is automatically falling back to REST API. This behavior will be deprecated in the future. Please use httpSend() explicitly for REST delivery.");const{event:i,payload:a}=e,o={apikey:this.socket.apiKey?this.socket.apiKey:"","Content-Type":"application/json"};this.socket.accessTokenValue&&(o.Authorization=`Bearer ${this.socket.accessTokenValue}`);const l={method:"POST",headers:o,body:JSON.stringify({messages:[{topic:this.subTopic,event:i,payload:a,private:this.private}]})};try{const c=await this._fetchWithTimeout(this.broadcastEndpointURL,l,(s=t.timeout)!==null&&s!==void 0?s:this.timeout);return await((n=c.body)===null||n===void 0?void 0:n.cancel()),c.ok?"ok":"error"}catch(c){return c.name==="AbortError"?"timed out":"error"}}else return new Promise(i=>{var a,o,l;const c=this._push(e.type,e,t.timeout||this.timeout);e.type==="broadcast"&&!(!((l=(o=(a=this.params)===null||a===void 0?void 0:a.config)===null||o===void 0?void 0:o.broadcast)===null||l===void 0)&&l.ack)&&i("ok"),c.receive("ok",()=>i("ok")),c.receive("error",()=>i("error")),c.receive("timeout",()=>i("timed out"))})}updateJoinPayload(e){this.joinPush.updatePayload(e)}unsubscribe(e=this.timeout){this.state=$.leaving;const t=()=>{this.socket.log("channel",`leave ${this.topic}`),this._trigger(q.close,"leave",this._joinRef())};this.joinPush.destroy();let s=null;return new Promise(n=>{s=new Ce(this,q.leave,{},e),s.receive("ok",()=>{t(),n("ok")}).receive("timeout",()=>{t(),n("timed out")}).receive("error",()=>{n("error")}),s.send(),this._canPush()||s.trigger("ok",{})}).finally(()=>{s==null||s.destroy()})}teardown(){this.pushBuffer.forEach(e=>e.destroy()),this.pushBuffer=[],this.rejoinTimer.reset(),this.joinPush.destroy(),this.state=$.closed,this.bindings={}}async _fetchWithTimeout(e,t,s){const n=new AbortController,i=setTimeout(()=>n.abort(),s),a=await this.socket.fetch(e,Object.assign(Object.assign({},t),{signal:n.signal}));return clearTimeout(i),a}_push(e,t,s=this.timeout){if(!this.joinedOnce)throw`tried to push '${e}' to '${this.topic}' before joining. Use channel.subscribe() before pushing events`;let n=new Ce(this,e,t,s);return this._canPush()?n.send():this._addToPushBuffer(n),n}_addToPushBuffer(e){if(e.startTimeout(),this.pushBuffer.push(e),this.pushBuffer.length>cr){const t=this.pushBuffer.shift();t&&(t.destroy(),this.socket.log("channel",`discarded push due to buffer overflow: ${t.event}`,t.payload))}}_onMessage(e,t,s){return t}_isMember(e){return this.topic===e}_joinRef(){return this.joinPush.ref}_trigger(e,t,s){var n,i;const a=e.toLocaleLowerCase(),{close:o,error:l,leave:c,join:u}=q;if(s&&[o,l,c,u].indexOf(a)>=0&&s!==this._joinRef())return;let d=this._onMessage(a,t,s);if(t&&!d)throw"channel onMessage callbacks must return the payload, modified or unmodified";["insert","update","delete"].includes(a)?(n=this.bindings.postgres_changes)===null||n===void 0||n.filter(h=>{var p,m,v;return((p=h.filter)===null||p===void 0?void 0:p.event)==="*"||((v=(m=h.filter)===null||m===void 0?void 0:m.event)===null||v===void 0?void 0:v.toLocaleLowerCase())===a}).map(h=>h.callback(d,s)):(i=this.bindings[a])===null||i===void 0||i.filter(h=>{var p,m,v,w,b,g,S,x;if(["broadcast","presence","postgres_changes"].includes(a))if("id"in h){const T=h.id,A=(p=h.filter)===null||p===void 0?void 0:p.event;return T&&((m=t.ids)===null||m===void 0?void 0:m.includes(T))&&(A==="*"||(A==null?void 0:A.toLocaleLowerCase())===((v=t.data)===null||v===void 0?void 0:v.type.toLocaleLowerCase()))&&(!(!((w=h.filter)===null||w===void 0)&&w.table)||h.filter.table===((b=t.data)===null||b===void 0?void 0:b.table))}else{const T=(S=(g=h==null?void 0:h.filter)===null||g===void 0?void 0:g.event)===null||S===void 0?void 0:S.toLocaleLowerCase();return T==="*"||T===((x=t==null?void 0:t.event)===null||x===void 0?void 0:x.toLocaleLowerCase())}else return h.type.toLocaleLowerCase()===a}).map(h=>{if(typeof d=="object"&&"ids"in d){const p=d.data,{schema:m,table:v,commit_timestamp:w,type:b,errors:g}=p;d=Object.assign(Object.assign({},{schema:m,table:v,commit_timestamp:w,eventType:b,new:{},old:{},errors:g}),this._getPayloadRecords(p))}h.callback(d,s)})}_isClosed(){return this.state===$.closed}_isJoined(){return this.state===$.joined}_isJoining(){return this.state===$.joining}_isLeaving(){return this.state===$.leaving}_replyEventName(e){return`chan_reply_${e}`}_on(e,t,s){const n=e.toLocaleLowerCase(),i={type:n,filter:t,callback:s};return this.bindings[n]?this.bindings[n].push(i):this.bindings[n]=[i],this}_off(e,t){const s=e.toLocaleLowerCase();return this.bindings[s]&&(this.bindings[s]=this.bindings[s].filter(n=>{var i;return!(((i=n.type)===null||i===void 0?void 0:i.toLocaleLowerCase())===s&&le.isEqual(n.filter,t))})),this}static isEqual(e,t){if(Object.keys(e).length!==Object.keys(t).length)return!1;for(const s in e)if(e[s]!==t[s])return!1;return!0}static isFilterValueEqual(e,t){return(e??void 0)===(t??void 0)}_rejoinUntilConnected(){this.rejoinTimer.scheduleTimeout(),this.socket.isConnected()&&this._rejoin()}_onClose(e){this._on(q.close,{},e)}_onError(e){this._on(q.error,{},t=>e(t))}_canPush(){return this.socket.isConnected()&&this._isJoined()}_rejoin(e=this.timeout){this._isLeaving()||(this.socket._leaveOpenTopic(this.topic),this.state=$.joining,this.joinPush.resend(e))}_getPayloadRecords(e){const t={new:{},old:{}};return(e.type==="INSERT"||e.type==="UPDATE")&&(t.new=ut(e.columns,e.record)),(e.type==="UPDATE"||e.type==="DELETE")&&(t.old=ut(e.columns,e.old_record)),t}}const $e=()=>{},be={HEARTBEAT_INTERVAL:25e3,RECONNECT_DELAY:10,HEARTBEAT_TIMEOUT_FALLBACK:100},vr=[1e3,2e3,5e3,1e4],yr=1e4,wr=`
  addEventListener("message", (e) => {
    if (e.data.event === "start") {
      setInterval(() => postMessage({ event: "keepAlive" }), e.data.interval);
    }
  });`;class br{constructor(e,t){var s;if(this.accessTokenValue=null,this.apiKey=null,this._manuallySetToken=!1,this.channels=new Array,this.endPoint="",this.httpEndpoint="",this.headers={},this.params={},this.timeout=qe,this.transport=null,this.heartbeatIntervalMs=be.HEARTBEAT_INTERVAL,this.heartbeatTimer=void 0,this.pendingHeartbeatRef=null,this.heartbeatCallback=$e,this.ref=0,this.reconnectTimer=null,this.vsn=ct,this.logger=$e,this.conn=null,this.sendBuffer=[],this.serializer=new ur,this.stateChangeCallbacks={open:[],close:[],error:[],message:[]},this.accessToken=null,this._connectionState="disconnected",this._wasManualDisconnect=!1,this._authPromise=null,this._heartbeatSentAt=null,this._resolveFetch=n=>n?(...i)=>n(...i):(...i)=>fetch(...i),!(!((s=t==null?void 0:t.params)===null||s===void 0)&&s.apikey))throw new Error("API key is required to connect to Realtime");this.apiKey=t.params.apikey,this.endPoint=`${e}/${Me.websocket}`,this.httpEndpoint=jt(e),this._initializeOptions(t),this._setupReconnectionTimer(),this.fetch=this._resolveFetch(t==null?void 0:t.fetch)}connect(){if(!(this.isConnecting()||this.isDisconnecting()||this.conn!==null&&this.isConnected())){if(this._setConnectionState("connecting"),this.accessToken&&!this._authPromise&&this._setAuthSafely("connect"),this.transport)this.conn=new this.transport(this.endpointURL());else try{this.conn=nr.createWebSocket(this.endpointURL())}catch(e){this._setConnectionState("disconnected");const t=e.message;throw t.includes("Node.js")?new Error(`${t}

To use Realtime in Node.js, you need to provide a WebSocket implementation:

Option 1: Use Node.js 22+ which has native WebSocket support
Option 2: Install and provide the "ws" package:

  npm install ws

  import ws from "ws"
  const client = new RealtimeClient(url, {
    ...options,
    transport: ws
  })`):new Error(`WebSocket not available: ${t}`)}this._setupConnectionHandlers()}}endpointURL(){return this._appendParams(this.endPoint,Object.assign({},this.params,{vsn:this.vsn}))}disconnect(e,t){if(!this.isDisconnecting())if(this._setConnectionState("disconnecting",!0),this.conn){const s=setTimeout(()=>{this._setConnectionState("disconnected")},100);this.conn.onclose=()=>{clearTimeout(s),this._setConnectionState("disconnected")},typeof this.conn.close=="function"&&(e?this.conn.close(e,t??""):this.conn.close()),this._teardownConnection()}else this._setConnectionState("disconnected")}getChannels(){return this.channels}async removeChannel(e){const t=await e.unsubscribe();return this.channels.length===0&&this.disconnect(),t}async removeAllChannels(){const e=await Promise.all(this.channels.map(t=>t.unsubscribe()));return this.channels=[],this.disconnect(),e}log(e,t,s){this.logger(e,t,s)}connectionState(){switch(this.conn&&this.conn.readyState){case V.connecting:return Y.Connecting;case V.open:return Y.Open;case V.closing:return Y.Closing;default:return Y.Closed}}isConnected(){return this.connectionState()===Y.Open}isConnecting(){return this._connectionState==="connecting"}isDisconnecting(){return this._connectionState==="disconnecting"}channel(e,t={config:{}}){const s=`realtime:${e}`,n=this.getChannels().find(i=>i.topic===s);if(n)return n;{const i=new le(`realtime:${e}`,t,this);return this.channels.push(i),i}}push(e){const{topic:t,event:s,payload:n,ref:i}=e,a=()=>{this.encode(e,o=>{var l;(l=this.conn)===null||l===void 0||l.send(o)})};this.log("push",`${t} ${s} (${i})`,n),this.isConnected()?a():this.sendBuffer.push(a)}async setAuth(e=null){this._authPromise=this._performAuth(e);try{await this._authPromise}finally{this._authPromise=null}}_isManualToken(){return this._manuallySetToken}async sendHeartbeat(){var e;if(!this.isConnected()){try{this.heartbeatCallback("disconnected")}catch(t){this.log("error","error in heartbeat callback",t)}return}if(this.pendingHeartbeatRef){this.pendingHeartbeatRef=null,this._heartbeatSentAt=null,this.log("transport","heartbeat timeout. Attempting to re-establish connection");try{this.heartbeatCallback("timeout")}catch(t){this.log("error","error in heartbeat callback",t)}this._wasManualDisconnect=!1,(e=this.conn)===null||e===void 0||e.close(lr,"heartbeat timeout"),setTimeout(()=>{var t;this.isConnected()||(t=this.reconnectTimer)===null||t===void 0||t.scheduleTimeout()},be.HEARTBEAT_TIMEOUT_FALLBACK);return}this._heartbeatSentAt=Date.now(),this.pendingHeartbeatRef=this._makeRef(),this.push({topic:"phoenix",event:"heartbeat",payload:{},ref:this.pendingHeartbeatRef});try{this.heartbeatCallback("sent")}catch(t){this.log("error","error in heartbeat callback",t)}this._setAuthSafely("heartbeat")}onHeartbeat(e){this.heartbeatCallback=e}flushSendBuffer(){this.isConnected()&&this.sendBuffer.length>0&&(this.sendBuffer.forEach(e=>e()),this.sendBuffer=[])}_makeRef(){let e=this.ref+1;return e===this.ref?this.ref=0:this.ref=e,this.ref.toString()}_leaveOpenTopic(e){let t=this.channels.find(s=>s.topic===e&&(s._isJoined()||s._isJoining()));t&&(this.log("transport",`leaving duplicate topic "${e}"`),t.unsubscribe())}_remove(e){this.channels=this.channels.filter(t=>t.topic!==e.topic)}_onConnMessage(e){this.decode(e.data,t=>{if(t.topic==="phoenix"&&t.event==="phx_reply"&&t.ref&&t.ref===this.pendingHeartbeatRef){const c=this._heartbeatSentAt?Date.now()-this._heartbeatSentAt:void 0;try{this.heartbeatCallback(t.payload.status==="ok"?"ok":"error",c)}catch(u){this.log("error","error in heartbeat callback",u)}this._heartbeatSentAt=null,this.pendingHeartbeatRef=null}const{topic:s,event:n,payload:i,ref:a}=t,o=a?`(${a})`:"",l=i.status||"";this.log("receive",`${l} ${s} ${n} ${o}`.trim(),i),this.channels.filter(c=>c._isMember(s)).forEach(c=>c._trigger(n,i,a)),this._triggerStateCallbacks("message",t)})}_clearTimer(e){var t;e==="heartbeat"&&this.heartbeatTimer?(clearInterval(this.heartbeatTimer),this.heartbeatTimer=void 0):e==="reconnect"&&((t=this.reconnectTimer)===null||t===void 0||t.reset())}_clearAllTimers(){this._clearTimer("heartbeat"),this._clearTimer("reconnect")}_setupConnectionHandlers(){this.conn&&("binaryType"in this.conn&&(this.conn.binaryType="arraybuffer"),this.conn.onopen=()=>this._onConnOpen(),this.conn.onerror=e=>this._onConnError(e),this.conn.onmessage=e=>this._onConnMessage(e),this.conn.onclose=e=>this._onConnClose(e),this.conn.readyState===V.open&&this._onConnOpen())}_teardownConnection(){if(this.conn){if(this.conn.readyState===V.open||this.conn.readyState===V.connecting)try{this.conn.close()}catch(e){this.log("error","Error closing connection",e)}this.conn.onopen=null,this.conn.onerror=null,this.conn.onmessage=null,this.conn.onclose=null,this.conn=null}this._clearAllTimers(),this._terminateWorker(),this.channels.forEach(e=>e.teardown())}_onConnOpen(){this._setConnectionState("connected"),this.log("transport",`connected to ${this.endpointURL()}`),(this._authPromise||(this.accessToken&&!this.accessTokenValue?this.setAuth():Promise.resolve())).then(()=>{this.flushSendBuffer()}).catch(t=>{this.log("error","error waiting for auth on connect",t),this.flushSendBuffer()}),this._clearTimer("reconnect"),this.worker?this.workerRef||this._startWorkerHeartbeat():this._startHeartbeat(),this._triggerStateCallbacks("open")}_startHeartbeat(){this.heartbeatTimer&&clearInterval(this.heartbeatTimer),this.heartbeatTimer=setInterval(()=>this.sendHeartbeat(),this.heartbeatIntervalMs)}_startWorkerHeartbeat(){this.workerUrl?this.log("worker",`starting worker for from ${this.workerUrl}`):this.log("worker","starting default worker");const e=this._workerObjectUrl(this.workerUrl);this.workerRef=new Worker(e),this.workerRef.onerror=t=>{this.log("worker","worker error",t.message),this._terminateWorker()},this.workerRef.onmessage=t=>{t.data.event==="keepAlive"&&this.sendHeartbeat()},this.workerRef.postMessage({event:"start",interval:this.heartbeatIntervalMs})}_terminateWorker(){this.workerRef&&(this.log("worker","terminating worker"),this.workerRef.terminate(),this.workerRef=void 0)}_onConnClose(e){var t;this._setConnectionState("disconnected"),this.log("transport","close",e),this._triggerChanError(),this._clearTimer("heartbeat"),this._wasManualDisconnect||(t=this.reconnectTimer)===null||t===void 0||t.scheduleTimeout(),this._triggerStateCallbacks("close",e)}_onConnError(e){this._setConnectionState("disconnected"),this.log("transport",`${e}`),this._triggerChanError(),this._triggerStateCallbacks("error",e)}_triggerChanError(){this.channels.forEach(e=>e._trigger(q.error))}_appendParams(e,t){if(Object.keys(t).length===0)return e;const s=e.match(/\?/)?"&":"?",n=new URLSearchParams(t);return`${e}${s}${n}`}_workerObjectUrl(e){let t;if(e)t=e;else{const s=new Blob([wr],{type:"application/javascript"});t=URL.createObjectURL(s)}return t}_setConnectionState(e,t=!1){this._connectionState=e,e==="connecting"?this._wasManualDisconnect=!1:e==="disconnecting"&&(this._wasManualDisconnect=t)}async _performAuth(e=null){let t,s=!1;if(e)t=e,s=!0;else if(this.accessToken)try{t=await this.accessToken()}catch(n){this.log("error","Error fetching access token from callback",n),t=this.accessTokenValue}else t=this.accessTokenValue;s?this._manuallySetToken=!0:this.accessToken&&(this._manuallySetToken=!1),this.accessTokenValue!=t&&(this.accessTokenValue=t,this.channels.forEach(n=>{const i={access_token:t,version:ar};t&&n.updateJoinPayload(i),n.joinedOnce&&n._isJoined()&&n._push(q.access_token,{access_token:t})}))}async _waitForAuthIfNeeded(){this._authPromise&&await this._authPromise}_setAuthSafely(e="general"){this._isManualToken()||this.setAuth().catch(t=>{this.log("error",`Error setting auth in ${e}`,t)})}_triggerStateCallbacks(e,t){try{this.stateChangeCallbacks[e].forEach(s=>{try{s(t)}catch(n){this.log("error",`error in ${e} callback`,n)}})}catch(s){this.log("error",`error triggering ${e} callbacks`,s)}}_setupReconnectionTimer(){this.reconnectTimer=new $t(async()=>{setTimeout(async()=>{await this._waitForAuthIfNeeded(),this.isConnected()||this.connect()},be.RECONNECT_DELAY)},this.reconnectAfterMs)}_initializeOptions(e){var t,s,n,i,a,o,l,c,u,f,d,h;switch(this.transport=(t=e==null?void 0:e.transport)!==null&&t!==void 0?t:null,this.timeout=(s=e==null?void 0:e.timeout)!==null&&s!==void 0?s:qe,this.heartbeatIntervalMs=(n=e==null?void 0:e.heartbeatIntervalMs)!==null&&n!==void 0?n:be.HEARTBEAT_INTERVAL,this.worker=(i=e==null?void 0:e.worker)!==null&&i!==void 0?i:!1,this.accessToken=(a=e==null?void 0:e.accessToken)!==null&&a!==void 0?a:null,this.heartbeatCallback=(o=e==null?void 0:e.heartbeatCallback)!==null&&o!==void 0?o:$e,this.vsn=(l=e==null?void 0:e.vsn)!==null&&l!==void 0?l:ct,e!=null&&e.params&&(this.params=e.params),e!=null&&e.logger&&(this.logger=e.logger),(e!=null&&e.logLevel||e!=null&&e.log_level)&&(this.logLevel=e.logLevel||e.log_level,this.params=Object.assign(Object.assign({},this.params),{log_level:this.logLevel})),this.reconnectAfterMs=(c=e==null?void 0:e.reconnectAfterMs)!==null&&c!==void 0?c:p=>vr[p-1]||yr,this.vsn){case Ct:this.encode=(u=e==null?void 0:e.encode)!==null&&u!==void 0?u:(p,m)=>m(JSON.stringify(p)),this.decode=(f=e==null?void 0:e.decode)!==null&&f!==void 0?f:(p,m)=>m(JSON.parse(p));break;case or:this.encode=(d=e==null?void 0:e.encode)!==null&&d!==void 0?d:this.serializer.encode.bind(this.serializer),this.decode=(h=e==null?void 0:e.decode)!==null&&h!==void 0?h:this.serializer.decode.bind(this.serializer);break;default:throw new Error(`Unsupported serializer version: ${this.vsn}`)}if(this.worker){if(typeof window<"u"&&!window.Worker)throw new Error("Web Worker is not supported");this.workerUrl=e==null?void 0:e.workerUrl}}}var fe=class extends Error{constructor(r,e){var t;super(r),this.name="IcebergError",this.status=e.status,this.icebergType=e.icebergType,this.icebergCode=e.icebergCode,this.details=e.details,this.isCommitStateUnknown=e.icebergType==="CommitStateUnknownException"||[500,502,504].includes(e.status)&&((t=e.icebergType)==null?void 0:t.includes("CommitState"))===!0}isNotFound(){return this.status===404}isConflict(){return this.status===409}isAuthenticationTimeout(){return this.status===419}};function _r(r,e,t){const s=new URL(e,r);if(t)for(const[n,i]of Object.entries(t))i!==void 0&&s.searchParams.set(n,i);return s.toString()}async function Er(r){return!r||r.type==="none"?{}:r.type==="bearer"?{Authorization:`Bearer ${r.token}`}:r.type==="header"?{[r.name]:r.value}:r.type==="custom"?await r.getHeaders():{}}function Sr(r){const e=r.fetchImpl??globalThis.fetch;return{async request({method:t,path:s,query:n,body:i,headers:a}){const o=_r(r.baseUrl,s,n),l=await Er(r.auth),c=await e(o,{method:t,headers:{...i?{"Content-Type":"application/json"}:{},...l,...a},body:i?JSON.stringify(i):void 0}),u=await c.text(),f=(c.headers.get("content-type")||"").includes("application/json"),d=f&&u?JSON.parse(u):u;if(!c.ok){const h=f?d:void 0,p=h==null?void 0:h.error;throw new fe((p==null?void 0:p.message)??`Request failed with status ${c.status}`,{status:c.status,icebergType:p==null?void 0:p.type,icebergCode:p==null?void 0:p.code,details:h})}return{status:c.status,headers:c.headers,data:d}}}}function _e(r){return r.join("")}var kr=class{constructor(r,e=""){this.client=r,this.prefix=e}async listNamespaces(r){const e=r?{parent:_e(r.namespace)}:void 0;return(await this.client.request({method:"GET",path:`${this.prefix}/namespaces`,query:e})).data.namespaces.map(s=>({namespace:s}))}async createNamespace(r,e){const t={namespace:r.namespace,properties:e==null?void 0:e.properties};return(await this.client.request({method:"POST",path:`${this.prefix}/namespaces`,body:t})).data}async dropNamespace(r){await this.client.request({method:"DELETE",path:`${this.prefix}/namespaces/${_e(r.namespace)}`})}async loadNamespaceMetadata(r){return{properties:(await this.client.request({method:"GET",path:`${this.prefix}/namespaces/${_e(r.namespace)}`})).data.properties}}async namespaceExists(r){try{return await this.client.request({method:"HEAD",path:`${this.prefix}/namespaces/${_e(r.namespace)}`}),!0}catch(e){if(e instanceof fe&&e.status===404)return!1;throw e}}async createNamespaceIfNotExists(r,e){try{return await this.createNamespace(r,e)}catch(t){if(t instanceof fe&&t.status===409)return;throw t}}};function Z(r){return r.join("")}var Tr=class{constructor(r,e="",t){this.client=r,this.prefix=e,this.accessDelegation=t}async listTables(r){return(await this.client.request({method:"GET",path:`${this.prefix}/namespaces/${Z(r.namespace)}/tables`})).data.identifiers}async createTable(r,e){const t={};return this.accessDelegation&&(t["X-Iceberg-Access-Delegation"]=this.accessDelegation),(await this.client.request({method:"POST",path:`${this.prefix}/namespaces/${Z(r.namespace)}/tables`,body:e,headers:t})).data.metadata}async updateTable(r,e){const t=await this.client.request({method:"POST",path:`${this.prefix}/namespaces/${Z(r.namespace)}/tables/${r.name}`,body:e});return{"metadata-location":t.data["metadata-location"],metadata:t.data.metadata}}async dropTable(r,e){await this.client.request({method:"DELETE",path:`${this.prefix}/namespaces/${Z(r.namespace)}/tables/${r.name}`,query:{purgeRequested:String((e==null?void 0:e.purge)??!1)}})}async loadTable(r){const e={};return this.accessDelegation&&(e["X-Iceberg-Access-Delegation"]=this.accessDelegation),(await this.client.request({method:"GET",path:`${this.prefix}/namespaces/${Z(r.namespace)}/tables/${r.name}`,headers:e})).data.metadata}async tableExists(r){const e={};this.accessDelegation&&(e["X-Iceberg-Access-Delegation"]=this.accessDelegation);try{return await this.client.request({method:"HEAD",path:`${this.prefix}/namespaces/${Z(r.namespace)}/tables/${r.name}`,headers:e}),!0}catch(t){if(t instanceof fe&&t.status===404)return!1;throw t}}async createTableIfNotExists(r,e){try{return await this.createTable(r,e)}catch(t){if(t instanceof fe&&t.status===409)return await this.loadTable({namespace:r.namespace,name:e.name});throw t}}},Or=class{constructor(r){var s;let e="v1";r.catalogName&&(e+=`/${r.catalogName}`);const t=r.baseUrl.endsWith("/")?r.baseUrl:`${r.baseUrl}/`;this.client=Sr({baseUrl:t,auth:r.auth,fetchImpl:r.fetch}),this.accessDelegation=(s=r.accessDelegation)==null?void 0:s.join(","),this.namespaceOps=new kr(this.client,e),this.tableOps=new Tr(this.client,e,this.accessDelegation)}async listNamespaces(r){return this.namespaceOps.listNamespaces(r)}async createNamespace(r,e){return this.namespaceOps.createNamespace(r,e)}async dropNamespace(r){await this.namespaceOps.dropNamespace(r)}async loadNamespaceMetadata(r){return this.namespaceOps.loadNamespaceMetadata(r)}async listTables(r){return this.tableOps.listTables(r)}async createTable(r,e){return this.tableOps.createTable(r,e)}async updateTable(r,e){return this.tableOps.updateTable(r,e)}async dropTable(r,e){await this.tableOps.dropTable(r,e)}async loadTable(r){return this.tableOps.loadTable(r)}async namespaceExists(r){return this.namespaceOps.namespaceExists(r)}async tableExists(r){return this.tableOps.tableExists(r)}async createNamespaceIfNotExists(r,e){return this.namespaceOps.createNamespaceIfNotExists(r,e)}async createTableIfNotExists(r,e){return this.tableOps.createTableIfNotExists(r,e)}},Re=class extends Error{constructor(r){super(r),this.__isStorageError=!0,this.name="StorageError"}};function R(r){return typeof r=="object"&&r!==null&&"__isStorageError"in r}var Ar=class extends Re{constructor(r,e,t){super(r),this.name="StorageApiError",this.status=e,this.statusCode=t}toJSON(){return{name:this.name,message:this.message,status:this.status,statusCode:this.statusCode}}},We=class extends Re{constructor(r,e){super(r),this.name="StorageUnknownError",this.originalError=e}};const Xe=r=>r?(...e)=>r(...e):(...e)=>fetch(...e),Rr=()=>Response,Ke=r=>{if(Array.isArray(r))return r.map(t=>Ke(t));if(typeof r=="function"||r!==Object(r))return r;const e={};return Object.entries(r).forEach(([t,s])=>{const n=t.replace(/([-_][a-z])/gi,i=>i.toUpperCase().replace(/[-_]/g,""));e[n]=Ke(s)}),e},Ir=r=>{if(typeof r!="object"||r===null)return!1;const e=Object.getPrototypeOf(r);return(e===null||e===Object.prototype||Object.getPrototypeOf(e)===null)&&!(Symbol.toStringTag in r)&&!(Symbol.iterator in r)},Cr=r=>!r||typeof r!="string"||r.length===0||r.length>100||r.trim()!==r||r.includes("/")||r.includes("\\")?!1:/^[\w!.\*'() &$@=;:+,?-]+$/.test(r);function pe(r){"@babel/helpers - typeof";return pe=typeof Symbol=="function"&&typeof Symbol.iterator=="symbol"?function(e){return typeof e}:function(e){return e&&typeof Symbol=="function"&&e.constructor===Symbol&&e!==Symbol.prototype?"symbol":typeof e},pe(r)}function $r(r,e){if(pe(r)!="object"||!r)return r;var t=r[Symbol.toPrimitive];if(t!==void 0){var s=t.call(r,e);if(pe(s)!="object")return s;throw new TypeError("@@toPrimitive must return a primitive value.")}return(e==="string"?String:Number)(r)}function Pr(r){var e=$r(r,"string");return pe(e)=="symbol"?e:e+""}function jr(r,e,t){return(e=Pr(e))in r?Object.defineProperty(r,e,{value:t,enumerable:!0,configurable:!0,writable:!0}):r[e]=t,r}function ft(r,e){var t=Object.keys(r);if(Object.getOwnPropertySymbols){var s=Object.getOwnPropertySymbols(r);e&&(s=s.filter(function(n){return Object.getOwnPropertyDescriptor(r,n).enumerable})),t.push.apply(t,s)}return t}function E(r){for(var e=1;e<arguments.length;e++){var t=arguments[e]!=null?arguments[e]:{};e%2?ft(Object(t),!0).forEach(function(s){jr(r,s,t[s])}):Object.getOwnPropertyDescriptors?Object.defineProperties(r,Object.getOwnPropertyDescriptors(t)):ft(Object(t)).forEach(function(s){Object.defineProperty(r,s,Object.getOwnPropertyDescriptor(t,s))})}return r}const Pe=r=>{var e;return r.msg||r.message||r.error_description||(typeof r.error=="string"?r.error:(e=r.error)===null||e===void 0?void 0:e.message)||JSON.stringify(r)},xr=async(r,e,t)=>{r instanceof await Rr()&&!(t!=null&&t.noResolveJson)?r.json().then(s=>{const n=r.status||500,i=(s==null?void 0:s.statusCode)||n+"";e(new Ar(Pe(s),n,i))}).catch(s=>{e(new We(Pe(s),s))}):e(new We(Pe(r),r))},Ur=(r,e,t,s)=>{const n={method:r,headers:(e==null?void 0:e.headers)||{}};return r==="GET"||!s?n:(Ir(s)?(n.headers=E({"Content-Type":"application/json"},e==null?void 0:e.headers),n.body=JSON.stringify(s)):n.body=s,e!=null&&e.duplex&&(n.duplex=e.duplex),E(E({},n),t))};async function we(r,e,t,s,n,i){return new Promise((a,o)=>{r(t,Ur(e,s,n,i)).then(l=>{if(!l.ok)throw l;return s!=null&&s.noResolveJson?l:l.json()}).then(l=>a(l)).catch(l=>xr(l,o,s))})}async function me(r,e,t,s){return we(r,"GET",e,t,s)}async function L(r,e,t,s,n){return we(r,"POST",e,s,n,t)}async function Ve(r,e,t,s,n){return we(r,"PUT",e,s,n,t)}async function Nr(r,e,t,s){return we(r,"HEAD",e,E(E({},t),{},{noResolveJson:!0}),s)}async function Qe(r,e,t,s,n){return we(r,"DELETE",e,s,n,t)}var Br=class{constructor(r,e){this.downloadFn=r,this.shouldThrowOnError=e}then(r,e){return this.execute().then(r,e)}async execute(){var r=this;try{return{data:(await r.downloadFn()).body,error:null}}catch(e){if(r.shouldThrowOnError)throw e;if(R(e))return{data:null,error:e};throw e}}};let xt;xt=Symbol.toStringTag;var Dr=class{constructor(r,e){this.downloadFn=r,this.shouldThrowOnError=e,this[xt]="BlobDownloadBuilder",this.promise=null}asStream(){return new Br(this.downloadFn,this.shouldThrowOnError)}then(r,e){return this.getPromise().then(r,e)}catch(r){return this.getPromise().catch(r)}finally(r){return this.getPromise().finally(r)}getPromise(){return this.promise||(this.promise=this.execute()),this.promise}async execute(){var r=this;try{return{data:await(await r.downloadFn()).blob(),error:null}}catch(e){if(r.shouldThrowOnError)throw e;if(R(e))return{data:null,error:e};throw e}}};const Lr={limit:100,offset:0,sortBy:{column:"name",order:"asc"}},pt={cacheControl:"3600",contentType:"text/plain;charset=UTF-8",upsert:!1};var qr=class{constructor(r,e={},t,s){this.shouldThrowOnError=!1,this.url=r,this.headers=e,this.bucketId=t,this.fetch=Xe(s)}throwOnError(){return this.shouldThrowOnError=!0,this}async uploadOrUpdate(r,e,t,s){var n=this;try{let i;const a=E(E({},pt),s);let o=E(E({},n.headers),r==="POST"&&{"x-upsert":String(a.upsert)});const l=a.metadata;typeof Blob<"u"&&t instanceof Blob?(i=new FormData,i.append("cacheControl",a.cacheControl),l&&i.append("metadata",n.encodeMetadata(l)),i.append("",t)):typeof FormData<"u"&&t instanceof FormData?(i=t,i.has("cacheControl")||i.append("cacheControl",a.cacheControl),l&&!i.has("metadata")&&i.append("metadata",n.encodeMetadata(l))):(i=t,o["cache-control"]=`max-age=${a.cacheControl}`,o["content-type"]=a.contentType,l&&(o["x-metadata"]=n.toBase64(n.encodeMetadata(l))),(typeof ReadableStream<"u"&&i instanceof ReadableStream||i&&typeof i=="object"&&"pipe"in i&&typeof i.pipe=="function")&&!a.duplex&&(a.duplex="half")),s!=null&&s.headers&&(o=E(E({},o),s.headers));const c=n._removeEmptyFolders(e),u=n._getFinalPath(c),f=await(r=="PUT"?Ve:L)(n.fetch,`${n.url}/object/${u}`,i,E({headers:o},a!=null&&a.duplex?{duplex:a.duplex}:{}));return{data:{path:c,id:f.Id,fullPath:f.Key},error:null}}catch(i){if(n.shouldThrowOnError)throw i;if(R(i))return{data:null,error:i};throw i}}async upload(r,e,t){return this.uploadOrUpdate("POST",r,e,t)}async uploadToSignedUrl(r,e,t,s){var n=this;const i=n._removeEmptyFolders(r),a=n._getFinalPath(i),o=new URL(n.url+`/object/upload/sign/${a}`);o.searchParams.set("token",e);try{let l;const c=E({upsert:pt.upsert},s),u=E(E({},n.headers),{"x-upsert":String(c.upsert)});return typeof Blob<"u"&&t instanceof Blob?(l=new FormData,l.append("cacheControl",c.cacheControl),l.append("",t)):typeof FormData<"u"&&t instanceof FormData?(l=t,l.append("cacheControl",c.cacheControl)):(l=t,u["cache-control"]=`max-age=${c.cacheControl}`,u["content-type"]=c.contentType),{data:{path:i,fullPath:(await Ve(n.fetch,o.toString(),l,{headers:u})).Key},error:null}}catch(l){if(n.shouldThrowOnError)throw l;if(R(l))return{data:null,error:l};throw l}}async createSignedUploadUrl(r,e){var t=this;try{let s=t._getFinalPath(r);const n=E({},t.headers);e!=null&&e.upsert&&(n["x-upsert"]="true");const i=await L(t.fetch,`${t.url}/object/upload/sign/${s}`,{},{headers:n}),a=new URL(t.url+i.url),o=a.searchParams.get("token");if(!o)throw new Re("No token returned by API");return{data:{signedUrl:a.toString(),path:r,token:o},error:null}}catch(s){if(t.shouldThrowOnError)throw s;if(R(s))return{data:null,error:s};throw s}}async update(r,e,t){return this.uploadOrUpdate("PUT",r,e,t)}async move(r,e,t){var s=this;try{return{data:await L(s.fetch,`${s.url}/object/move`,{bucketId:s.bucketId,sourceKey:r,destinationKey:e,destinationBucket:t==null?void 0:t.destinationBucket},{headers:s.headers}),error:null}}catch(n){if(s.shouldThrowOnError)throw n;if(R(n))return{data:null,error:n};throw n}}async copy(r,e,t){var s=this;try{return{data:{path:(await L(s.fetch,`${s.url}/object/copy`,{bucketId:s.bucketId,sourceKey:r,destinationKey:e,destinationBucket:t==null?void 0:t.destinationBucket},{headers:s.headers})).Key},error:null}}catch(n){if(s.shouldThrowOnError)throw n;if(R(n))return{data:null,error:n};throw n}}async createSignedUrl(r,e,t){var s=this;try{let n=s._getFinalPath(r),i=await L(s.fetch,`${s.url}/object/sign/${n}`,E({expiresIn:e},t!=null&&t.transform?{transform:t.transform}:{}),{headers:s.headers});const a=t!=null&&t.download?`&download=${t.download===!0?"":t.download}`:"";return i={signedUrl:encodeURI(`${s.url}${i.signedURL}${a}`)},{data:i,error:null}}catch(n){if(s.shouldThrowOnError)throw n;if(R(n))return{data:null,error:n};throw n}}async createSignedUrls(r,e,t){var s=this;try{const n=await L(s.fetch,`${s.url}/object/sign/${s.bucketId}`,{expiresIn:e,paths:r},{headers:s.headers}),i=t!=null&&t.download?`&download=${t.download===!0?"":t.download}`:"";return{data:n.map(a=>E(E({},a),{},{signedUrl:a.signedURL?encodeURI(`${s.url}${a.signedURL}${i}`):null})),error:null}}catch(n){if(s.shouldThrowOnError)throw n;if(R(n))return{data:null,error:n};throw n}}download(r,e){const t=typeof(e==null?void 0:e.transform)<"u"?"render/image/authenticated":"object",s=this.transformOptsToQueryString((e==null?void 0:e.transform)||{}),n=s?`?${s}`:"",i=this._getFinalPath(r),a=()=>me(this.fetch,`${this.url}/${t}/${i}${n}`,{headers:this.headers,noResolveJson:!0});return new Dr(a,this.shouldThrowOnError)}async info(r){var e=this;const t=e._getFinalPath(r);try{return{data:Ke(await me(e.fetch,`${e.url}/object/info/${t}`,{headers:e.headers})),error:null}}catch(s){if(e.shouldThrowOnError)throw s;if(R(s))return{data:null,error:s};throw s}}async exists(r){var e=this;const t=e._getFinalPath(r);try{return await Nr(e.fetch,`${e.url}/object/${t}`,{headers:e.headers}),{data:!0,error:null}}catch(s){if(e.shouldThrowOnError)throw s;if(R(s)&&s instanceof We){const n=s.originalError;if([400,404].includes(n==null?void 0:n.status))return{data:!1,error:s}}throw s}}getPublicUrl(r,e){const t=this._getFinalPath(r),s=[],n=e!=null&&e.download?`download=${e.download===!0?"":e.download}`:"";n!==""&&s.push(n);const i=typeof(e==null?void 0:e.transform)<"u"?"render/image":"object",a=this.transformOptsToQueryString((e==null?void 0:e.transform)||{});a!==""&&s.push(a);let o=s.join("&");return o!==""&&(o=`?${o}`),{data:{publicUrl:encodeURI(`${this.url}/${i}/public/${t}${o}`)}}}async remove(r){var e=this;try{return{data:await Qe(e.fetch,`${e.url}/object/${e.bucketId}`,{prefixes:r},{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(R(t))return{data:null,error:t};throw t}}async list(r,e,t){var s=this;try{const n=E(E(E({},Lr),e),{},{prefix:r||""});return{data:await L(s.fetch,`${s.url}/object/list/${s.bucketId}`,n,{headers:s.headers},t),error:null}}catch(n){if(s.shouldThrowOnError)throw n;if(R(n))return{data:null,error:n};throw n}}async listV2(r,e){var t=this;try{const s=E({},r);return{data:await L(t.fetch,`${t.url}/object/list-v2/${t.bucketId}`,s,{headers:t.headers},e),error:null}}catch(s){if(t.shouldThrowOnError)throw s;if(R(s))return{data:null,error:s};throw s}}encodeMetadata(r){return JSON.stringify(r)}toBase64(r){return typeof Buffer<"u"?Buffer.from(r).toString("base64"):btoa(r)}_getFinalPath(r){return`${this.bucketId}/${r.replace(/^\/+/,"")}`}_removeEmptyFolders(r){return r.replace(/^\/|\/$/g,"").replace(/\/+/g,"/")}transformOptsToQueryString(r){const e=[];return r.width&&e.push(`width=${r.width}`),r.height&&e.push(`height=${r.height}`),r.resize&&e.push(`resize=${r.resize}`),r.format&&e.push(`format=${r.format}`),r.quality&&e.push(`quality=${r.quality}`),e.join("&")}};const Ut="2.90.1",Nt={"X-Client-Info":`storage-js/${Ut}`};var Mr=class{constructor(r,e={},t,s){this.shouldThrowOnError=!1;const n=new URL(r);s!=null&&s.useNewHostname&&/supabase\.(co|in|red)$/.test(n.hostname)&&!n.hostname.includes("storage.supabase.")&&(n.hostname=n.hostname.replace("supabase.","storage.supabase.")),this.url=n.href.replace(/\/$/,""),this.headers=E(E({},Nt),e),this.fetch=Xe(t)}throwOnError(){return this.shouldThrowOnError=!0,this}async listBuckets(r){var e=this;try{const t=e.listBucketOptionsToQueryString(r);return{data:await me(e.fetch,`${e.url}/bucket${t}`,{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(R(t))return{data:null,error:t};throw t}}async getBucket(r){var e=this;try{return{data:await me(e.fetch,`${e.url}/bucket/${r}`,{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(R(t))return{data:null,error:t};throw t}}async createBucket(r,e={public:!1}){var t=this;try{return{data:await L(t.fetch,`${t.url}/bucket`,{id:r,name:r,type:e.type,public:e.public,file_size_limit:e.fileSizeLimit,allowed_mime_types:e.allowedMimeTypes},{headers:t.headers}),error:null}}catch(s){if(t.shouldThrowOnError)throw s;if(R(s))return{data:null,error:s};throw s}}async updateBucket(r,e){var t=this;try{return{data:await Ve(t.fetch,`${t.url}/bucket/${r}`,{id:r,name:r,public:e.public,file_size_limit:e.fileSizeLimit,allowed_mime_types:e.allowedMimeTypes},{headers:t.headers}),error:null}}catch(s){if(t.shouldThrowOnError)throw s;if(R(s))return{data:null,error:s};throw s}}async emptyBucket(r){var e=this;try{return{data:await L(e.fetch,`${e.url}/bucket/${r}/empty`,{},{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(R(t))return{data:null,error:t};throw t}}async deleteBucket(r){var e=this;try{return{data:await Qe(e.fetch,`${e.url}/bucket/${r}`,{},{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(R(t))return{data:null,error:t};throw t}}listBucketOptionsToQueryString(r){const e={};return r&&("limit"in r&&(e.limit=String(r.limit)),"offset"in r&&(e.offset=String(r.offset)),r.search&&(e.search=r.search),r.sortColumn&&(e.sortColumn=r.sortColumn),r.sortOrder&&(e.sortOrder=r.sortOrder)),Object.keys(e).length>0?"?"+new URLSearchParams(e).toString():""}},Fr=class{constructor(r,e={},t){this.shouldThrowOnError=!1,this.url=r.replace(/\/$/,""),this.headers=E(E({},Nt),e),this.fetch=Xe(t)}throwOnError(){return this.shouldThrowOnError=!0,this}async createBucket(r){var e=this;try{return{data:await L(e.fetch,`${e.url}/bucket`,{name:r},{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(R(t))return{data:null,error:t};throw t}}async listBuckets(r){var e=this;try{const t=new URLSearchParams;(r==null?void 0:r.limit)!==void 0&&t.set("limit",r.limit.toString()),(r==null?void 0:r.offset)!==void 0&&t.set("offset",r.offset.toString()),r!=null&&r.sortColumn&&t.set("sortColumn",r.sortColumn),r!=null&&r.sortOrder&&t.set("sortOrder",r.sortOrder),r!=null&&r.search&&t.set("search",r.search);const s=t.toString(),n=s?`${e.url}/bucket?${s}`:`${e.url}/bucket`;return{data:await me(e.fetch,n,{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(R(t))return{data:null,error:t};throw t}}async deleteBucket(r){var e=this;try{return{data:await Qe(e.fetch,`${e.url}/bucket/${r}`,{},{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(R(t))return{data:null,error:t};throw t}}from(r){var e=this;if(!Cr(r))throw new Re("Invalid bucket name: File, folder, and bucket names must follow AWS object key naming guidelines and should avoid the use of any other characters.");const t=new Or({baseUrl:this.url,catalogName:r,auth:{type:"custom",getHeaders:async()=>e.headers},fetch:this.fetch}),s=this.shouldThrowOnError;return new Proxy(t,{get(n,i){const a=n[i];return typeof a!="function"?a:async(...o)=>{try{return{data:await a.apply(n,o),error:null}}catch(l){if(s)throw l;return{data:null,error:l}}}}})}};const Ze={"X-Client-Info":`storage-js/${Ut}`,"Content-Type":"application/json"};var Bt=class extends Error{constructor(r){super(r),this.__isStorageVectorsError=!0,this.name="StorageVectorsError"}};function N(r){return typeof r=="object"&&r!==null&&"__isStorageVectorsError"in r}var je=class extends Bt{constructor(r,e,t){super(r),this.name="StorageVectorsApiError",this.status=e,this.statusCode=t}toJSON(){return{name:this.name,message:this.message,status:this.status,statusCode:this.statusCode}}},Wr=class extends Bt{constructor(r,e){super(r),this.name="StorageVectorsUnknownError",this.originalError=e}};const et=r=>r?(...e)=>r(...e):(...e)=>fetch(...e),Kr=r=>{if(typeof r!="object"||r===null)return!1;const e=Object.getPrototypeOf(r);return(e===null||e===Object.prototype||Object.getPrototypeOf(e)===null)&&!(Symbol.toStringTag in r)&&!(Symbol.iterator in r)},mt=r=>r.msg||r.message||r.error_description||r.error||JSON.stringify(r),Vr=async(r,e,t)=>{if(r&&typeof r=="object"&&"status"in r&&"ok"in r&&typeof r.status=="number"&&!(t!=null&&t.noResolveJson)){const s=r.status||500,n=r;if(typeof n.json=="function")n.json().then(i=>{const a=(i==null?void 0:i.statusCode)||(i==null?void 0:i.code)||s+"";e(new je(mt(i),s,a))}).catch(()=>{const i=s+"";e(new je(n.statusText||`HTTP ${s} error`,s,i))});else{const i=s+"";e(new je(n.statusText||`HTTP ${s} error`,s,i))}}else e(new Wr(mt(r),r))},Hr=(r,e,t,s)=>{const n={method:r,headers:(e==null?void 0:e.headers)||{}};return s?(Kr(s)?(n.headers=E({"Content-Type":"application/json"},e==null?void 0:e.headers),n.body=JSON.stringify(s)):n.body=s,E(E({},n),t)):n};async function Jr(r,e,t,s,n,i){return new Promise((a,o)=>{r(t,Hr(e,s,n,i)).then(l=>{if(!l.ok)throw l;if(s!=null&&s.noResolveJson)return l;const c=l.headers.get("content-type");return!c||!c.includes("application/json")?{}:l.json()}).then(l=>a(l)).catch(l=>Vr(l,o,s))})}async function B(r,e,t,s,n){return Jr(r,"POST",e,s,n,t)}var Gr=class{constructor(r,e={},t){this.shouldThrowOnError=!1,this.url=r.replace(/\/$/,""),this.headers=E(E({},Ze),e),this.fetch=et(t)}throwOnError(){return this.shouldThrowOnError=!0,this}async createIndex(r){var e=this;try{return{data:await B(e.fetch,`${e.url}/CreateIndex`,r,{headers:e.headers})||{},error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(N(t))return{data:null,error:t};throw t}}async getIndex(r,e){var t=this;try{return{data:await B(t.fetch,`${t.url}/GetIndex`,{vectorBucketName:r,indexName:e},{headers:t.headers}),error:null}}catch(s){if(t.shouldThrowOnError)throw s;if(N(s))return{data:null,error:s};throw s}}async listIndexes(r){var e=this;try{return{data:await B(e.fetch,`${e.url}/ListIndexes`,r,{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(N(t))return{data:null,error:t};throw t}}async deleteIndex(r,e){var t=this;try{return{data:await B(t.fetch,`${t.url}/DeleteIndex`,{vectorBucketName:r,indexName:e},{headers:t.headers})||{},error:null}}catch(s){if(t.shouldThrowOnError)throw s;if(N(s))return{data:null,error:s};throw s}}},zr=class{constructor(r,e={},t){this.shouldThrowOnError=!1,this.url=r.replace(/\/$/,""),this.headers=E(E({},Ze),e),this.fetch=et(t)}throwOnError(){return this.shouldThrowOnError=!0,this}async putVectors(r){var e=this;try{if(r.vectors.length<1||r.vectors.length>500)throw new Error("Vector batch size must be between 1 and 500 items");return{data:await B(e.fetch,`${e.url}/PutVectors`,r,{headers:e.headers})||{},error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(N(t))return{data:null,error:t};throw t}}async getVectors(r){var e=this;try{return{data:await B(e.fetch,`${e.url}/GetVectors`,r,{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(N(t))return{data:null,error:t};throw t}}async listVectors(r){var e=this;try{if(r.segmentCount!==void 0){if(r.segmentCount<1||r.segmentCount>16)throw new Error("segmentCount must be between 1 and 16");if(r.segmentIndex!==void 0&&(r.segmentIndex<0||r.segmentIndex>=r.segmentCount))throw new Error(`segmentIndex must be between 0 and ${r.segmentCount-1}`)}return{data:await B(e.fetch,`${e.url}/ListVectors`,r,{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(N(t))return{data:null,error:t};throw t}}async queryVectors(r){var e=this;try{return{data:await B(e.fetch,`${e.url}/QueryVectors`,r,{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(N(t))return{data:null,error:t};throw t}}async deleteVectors(r){var e=this;try{if(r.keys.length<1||r.keys.length>500)throw new Error("Keys batch size must be between 1 and 500 items");return{data:await B(e.fetch,`${e.url}/DeleteVectors`,r,{headers:e.headers})||{},error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(N(t))return{data:null,error:t};throw t}}},Yr=class{constructor(r,e={},t){this.shouldThrowOnError=!1,this.url=r.replace(/\/$/,""),this.headers=E(E({},Ze),e),this.fetch=et(t)}throwOnError(){return this.shouldThrowOnError=!0,this}async createBucket(r){var e=this;try{return{data:await B(e.fetch,`${e.url}/CreateVectorBucket`,{vectorBucketName:r},{headers:e.headers})||{},error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(N(t))return{data:null,error:t};throw t}}async getBucket(r){var e=this;try{return{data:await B(e.fetch,`${e.url}/GetVectorBucket`,{vectorBucketName:r},{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(N(t))return{data:null,error:t};throw t}}async listBuckets(r={}){var e=this;try{return{data:await B(e.fetch,`${e.url}/ListVectorBuckets`,r,{headers:e.headers}),error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(N(t))return{data:null,error:t};throw t}}async deleteBucket(r){var e=this;try{return{data:await B(e.fetch,`${e.url}/DeleteVectorBucket`,{vectorBucketName:r},{headers:e.headers})||{},error:null}}catch(t){if(e.shouldThrowOnError)throw t;if(N(t))return{data:null,error:t};throw t}}},Xr=class extends Yr{constructor(r,e={}){super(r,e.headers||{},e.fetch)}from(r){return new Qr(this.url,this.headers,r,this.fetch)}async createBucket(r){var e=()=>super.createBucket,t=this;return e().call(t,r)}async getBucket(r){var e=()=>super.getBucket,t=this;return e().call(t,r)}async listBuckets(r={}){var e=()=>super.listBuckets,t=this;return e().call(t,r)}async deleteBucket(r){var e=()=>super.deleteBucket,t=this;return e().call(t,r)}},Qr=class extends Gr{constructor(r,e,t,s){super(r,e,s),this.vectorBucketName=t}async createIndex(r){var e=()=>super.createIndex,t=this;return e().call(t,E(E({},r),{},{vectorBucketName:t.vectorBucketName}))}async listIndexes(r={}){var e=()=>super.listIndexes,t=this;return e().call(t,E(E({},r),{},{vectorBucketName:t.vectorBucketName}))}async getIndex(r){var e=()=>super.getIndex,t=this;return e().call(t,t.vectorBucketName,r)}async deleteIndex(r){var e=()=>super.deleteIndex,t=this;return e().call(t,t.vectorBucketName,r)}index(r){return new Zr(this.url,this.headers,this.vectorBucketName,r,this.fetch)}},Zr=class extends zr{constructor(r,e,t,s,n){super(r,e,n),this.vectorBucketName=t,this.indexName=s}async putVectors(r){var e=()=>super.putVectors,t=this;return e().call(t,E(E({},r),{},{vectorBucketName:t.vectorBucketName,indexName:t.indexName}))}async getVectors(r){var e=()=>super.getVectors,t=this;return e().call(t,E(E({},r),{},{vectorBucketName:t.vectorBucketName,indexName:t.indexName}))}async listVectors(r={}){var e=()=>super.listVectors,t=this;return e().call(t,E(E({},r),{},{vectorBucketName:t.vectorBucketName,indexName:t.indexName}))}async queryVectors(r){var e=()=>super.queryVectors,t=this;return e().call(t,E(E({},r),{},{vectorBucketName:t.vectorBucketName,indexName:t.indexName}))}async deleteVectors(r){var e=()=>super.deleteVectors,t=this;return e().call(t,E(E({},r),{},{vectorBucketName:t.vectorBucketName,indexName:t.indexName}))}},es=class extends Mr{constructor(r,e={},t,s){super(r,e,t,s)}from(r){return new qr(this.url,this.headers,r,this.fetch)}get vectors(){return new Xr(this.url+"/vector",{headers:this.headers,fetch:this.fetch})}get analytics(){return new Fr(this.url+"/iceberg",this.headers,this.fetch)}};const Dt="2.90.1",ae=30*1e3,He=3,xe=He*ae,ts="http://localhost:9999",rs="supabase.auth.token",ss={"X-Client-Info":`gotrue-js/${Dt}`},Je="X-Supabase-Api-Version",Lt={"2024-01-01":{timestamp:Date.parse("2024-01-01T00:00:00.0Z"),name:"2024-01-01"}},ns=/^([a-z0-9_-]{4})*($|[a-z0-9_-]{3}$|[a-z0-9_-]{2}$)$/i,is=10*60*1e3;class ge extends Error{constructor(e,t,s){super(e),this.__isAuthError=!0,this.name="AuthError",this.status=t,this.code=s}}function y(r){return typeof r=="object"&&r!==null&&"__isAuthError"in r}class as extends ge{constructor(e,t,s){super(e,t,s),this.name="AuthApiError",this.status=t,this.code=s}}function os(r){return y(r)&&r.name==="AuthApiError"}class X extends ge{constructor(e,t){super(e),this.name="AuthUnknownError",this.originalError=t}}class W extends ge{constructor(e,t,s,n){super(e,s,n),this.name=t,this.status=s}}class U extends W{constructor(){super("Auth session missing!","AuthSessionMissingError",400,void 0)}}function ls(r){return y(r)&&r.name==="AuthSessionMissingError"}class ee extends W{constructor(){super("Auth session or user missing","AuthInvalidTokenResponseError",500,void 0)}}class Ee extends W{constructor(e){super(e,"AuthInvalidCredentialsError",400,void 0)}}class Se extends W{constructor(e,t=null){super(e,"AuthImplicitGrantRedirectError",500,void 0),this.details=null,this.details=t}toJSON(){return{name:this.name,message:this.message,status:this.status,details:this.details}}}function cs(r){return y(r)&&r.name==="AuthImplicitGrantRedirectError"}class gt extends W{constructor(e,t=null){super(e,"AuthPKCEGrantCodeExchangeError",500,void 0),this.details=null,this.details=t}toJSON(){return{name:this.name,message:this.message,status:this.status,details:this.details}}}class us extends W{constructor(){super("PKCE code verifier not found in storage. This can happen if the auth flow was initiated in a different browser or device, or if the storage was cleared. For SSR frameworks (Next.js, SvelteKit, etc.), use @supabase/ssr on both the server and client to store the code verifier in cookies.","AuthPKCECodeVerifierMissingError",400,"pkce_code_verifier_not_found")}}class Ge extends W{constructor(e,t){super(e,"AuthRetryableFetchError",t,void 0)}}function Ue(r){return y(r)&&r.name==="AuthRetryableFetchError"}class vt extends W{constructor(e,t,s){super(e,"AuthWeakPasswordError",t,"weak_password"),this.reasons=s}}class ze extends W{constructor(e){super(e,"AuthInvalidJwtError",400,"invalid_jwt")}}const ke="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789-_".split(""),yt=` 	
\r=`.split(""),ds=(()=>{const r=new Array(128);for(let e=0;e<r.length;e+=1)r[e]=-1;for(let e=0;e<yt.length;e+=1)r[yt[e].charCodeAt(0)]=-2;for(let e=0;e<ke.length;e+=1)r[ke[e].charCodeAt(0)]=e;return r})();function wt(r,e,t){if(r!==null)for(e.queue=e.queue<<8|r,e.queuedBits+=8;e.queuedBits>=6;){const s=e.queue>>e.queuedBits-6&63;t(ke[s]),e.queuedBits-=6}else if(e.queuedBits>0)for(e.queue=e.queue<<6-e.queuedBits,e.queuedBits=6;e.queuedBits>=6;){const s=e.queue>>e.queuedBits-6&63;t(ke[s]),e.queuedBits-=6}}function qt(r,e,t){const s=ds[r];if(s>-1)for(e.queue=e.queue<<6|s,e.queuedBits+=6;e.queuedBits>=8;)t(e.queue>>e.queuedBits-8&255),e.queuedBits-=8;else{if(s===-2)return;throw new Error(`Invalid Base64-URL character "${String.fromCharCode(r)}"`)}}function bt(r){const e=[],t=a=>{e.push(String.fromCodePoint(a))},s={utf8seq:0,codepoint:0},n={queue:0,queuedBits:0},i=a=>{ps(a,s,t)};for(let a=0;a<r.length;a+=1)qt(r.charCodeAt(a),n,i);return e.join("")}function hs(r,e){if(r<=127){e(r);return}else if(r<=2047){e(192|r>>6),e(128|r&63);return}else if(r<=65535){e(224|r>>12),e(128|r>>6&63),e(128|r&63);return}else if(r<=1114111){e(240|r>>18),e(128|r>>12&63),e(128|r>>6&63),e(128|r&63);return}throw new Error(`Unrecognized Unicode codepoint: ${r.toString(16)}`)}function fs(r,e){for(let t=0;t<r.length;t+=1){let s=r.charCodeAt(t);if(s>55295&&s<=56319){const n=(s-55296)*1024&65535;s=(r.charCodeAt(t+1)-56320&65535|n)+65536,t+=1}hs(s,e)}}function ps(r,e,t){if(e.utf8seq===0){if(r<=127){t(r);return}for(let s=1;s<6;s+=1)if(!(r>>7-s&1)){e.utf8seq=s;break}if(e.utf8seq===2)e.codepoint=r&31;else if(e.utf8seq===3)e.codepoint=r&15;else if(e.utf8seq===4)e.codepoint=r&7;else throw new Error("Invalid UTF-8 sequence");e.utf8seq-=1}else if(e.utf8seq>0){if(r<=127)throw new Error("Invalid UTF-8 sequence");e.codepoint=e.codepoint<<6|r&63,e.utf8seq-=1,e.utf8seq===0&&t(e.codepoint)}}function ce(r){const e=[],t={queue:0,queuedBits:0},s=n=>{e.push(n)};for(let n=0;n<r.length;n+=1)qt(r.charCodeAt(n),t,s);return new Uint8Array(e)}function ms(r){const e=[];return fs(r,t=>e.push(t)),new Uint8Array(e)}function Q(r){const e=[],t={queue:0,queuedBits:0},s=n=>{e.push(n)};return r.forEach(n=>wt(n,t,s)),wt(null,t,s),e.join("")}function gs(r){return Math.round(Date.now()/1e3)+r}function vs(){return Symbol("auth-callback")}const j=()=>typeof window<"u"&&typeof document<"u",J={tested:!1,writable:!1},Mt=()=>{if(!j())return!1;try{if(typeof globalThis.localStorage!="object")return!1}catch{return!1}if(J.tested)return J.writable;const r=`lswt-${Math.random()}${Math.random()}`;try{globalThis.localStorage.setItem(r,r),globalThis.localStorage.removeItem(r),J.tested=!0,J.writable=!0}catch{J.tested=!0,J.writable=!1}return J.writable};function ys(r){const e={},t=new URL(r);if(t.hash&&t.hash[0]==="#")try{new URLSearchParams(t.hash.substring(1)).forEach((n,i)=>{e[i]=n})}catch{}return t.searchParams.forEach((s,n)=>{e[n]=s}),e}const Ft=r=>r?(...e)=>r(...e):(...e)=>fetch(...e),ws=r=>typeof r=="object"&&r!==null&&"status"in r&&"ok"in r&&"json"in r&&typeof r.json=="function",oe=async(r,e,t)=>{await r.setItem(e,JSON.stringify(t))},G=async(r,e)=>{const t=await r.getItem(e);if(!t)return null;try{return JSON.parse(t)}catch{return t}},P=async(r,e)=>{await r.removeItem(e)};class Ie{constructor(){this.promise=new Ie.promiseConstructor((e,t)=>{this.resolve=e,this.reject=t})}}Ie.promiseConstructor=Promise;function Ne(r){const e=r.split(".");if(e.length!==3)throw new ze("Invalid JWT structure");for(let s=0;s<e.length;s++)if(!ns.test(e[s]))throw new ze("JWT not in base64url format");return{header:JSON.parse(bt(e[0])),payload:JSON.parse(bt(e[1])),signature:ce(e[2]),raw:{header:e[0],payload:e[1]}}}async function bs(r){return await new Promise(e=>{setTimeout(()=>e(null),r)})}function _s(r,e){return new Promise((s,n)=>{(async()=>{for(let i=0;i<1/0;i++)try{const a=await r(i);if(!e(i,null,a)){s(a);return}}catch(a){if(!e(i,a)){n(a);return}}})()})}function Es(r){return("0"+r.toString(16)).substr(-2)}function Ss(){const e=new Uint32Array(56);if(typeof crypto>"u"){const t="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789-._~",s=t.length;let n="";for(let i=0;i<56;i++)n+=t.charAt(Math.floor(Math.random()*s));return n}return crypto.getRandomValues(e),Array.from(e,Es).join("")}async function ks(r){const t=new TextEncoder().encode(r),s=await crypto.subtle.digest("SHA-256",t),n=new Uint8Array(s);return Array.from(n).map(i=>String.fromCharCode(i)).join("")}async function Ts(r){if(!(typeof crypto<"u"&&typeof crypto.subtle<"u"&&typeof TextEncoder<"u"))return console.warn("WebCrypto API is not supported. Code challenge method will default to use plain instead of sha256."),r;const t=await ks(r);return btoa(t).replace(/\+/g,"-").replace(/\//g,"_").replace(/=+$/,"")}async function te(r,e,t=!1){const s=Ss();let n=s;t&&(n+="/PASSWORD_RECOVERY"),await oe(r,`${e}-code-verifier`,n);const i=await Ts(s);return[i,s===i?"plain":"s256"]}const Os=/^2[0-9]{3}-(0[1-9]|1[0-2])-(0[1-9]|1[0-9]|2[0-9]|3[0-1])$/i;function As(r){const e=r.headers.get(Je);if(!e||!e.match(Os))return null;try{return new Date(`${e}T00:00:00.0Z`)}catch{return null}}function Rs(r){if(!r)throw new Error("Missing exp claim");const e=Math.floor(Date.now()/1e3);if(r<=e)throw new Error("JWT has expired")}function Is(r){switch(r){case"RS256":return{name:"RSASSA-PKCS1-v1_5",hash:{name:"SHA-256"}};case"ES256":return{name:"ECDSA",namedCurve:"P-256",hash:{name:"SHA-256"}};default:throw new Error("Invalid alg claim")}}const Cs=/^[0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12}$/;function re(r){if(!Cs.test(r))throw new Error("@supabase/auth-js: Expected parameter to be UUID but is not")}function Be(){const r={};return new Proxy(r,{get:(e,t)=>{if(t==="__isUserNotAvailableProxy")return!0;if(typeof t=="symbol"){const s=t.toString();if(s==="Symbol(Symbol.toPrimitive)"||s==="Symbol(Symbol.toStringTag)"||s==="Symbol(util.inspect.custom)")return}throw new Error(`@supabase/auth-js: client was created with userStorage option and there was no user stored in the user storage. Accessing the "${t}" property of the session object is not supported. Please use getUser() instead.`)},set:(e,t)=>{throw new Error(`@supabase/auth-js: client was created with userStorage option and there was no user stored in the user storage. Setting the "${t}" property of the session object is not supported. Please use getUser() to fetch a user object you can manipulate.`)},deleteProperty:(e,t)=>{throw new Error(`@supabase/auth-js: client was created with userStorage option and there was no user stored in the user storage. Deleting the "${t}" property of the session object is not supported. Please use getUser() to fetch a user object you can manipulate.`)}})}function $s(r,e){return new Proxy(r,{get:(t,s,n)=>{if(s==="__isInsecureUserWarningProxy")return!0;if(typeof s=="symbol"){const i=s.toString();if(i==="Symbol(Symbol.toPrimitive)"||i==="Symbol(Symbol.toStringTag)"||i==="Symbol(util.inspect.custom)"||i==="Symbol(nodejs.util.inspect.custom)")return Reflect.get(t,s,n)}return!e.value&&typeof s=="string"&&(console.warn("Using the user object as returned from supabase.auth.getSession() or from some supabase.auth.onAuthStateChange() events could be insecure! This value comes directly from the storage medium (usually cookies on the server) and may not be authentic. Use supabase.auth.getUser() instead which authenticates the data by contacting the Supabase Auth server."),e.value=!0),Reflect.get(t,s,n)}})}function _t(r){return JSON.parse(JSON.stringify(r))}const z=r=>r.msg||r.message||r.error_description||r.error||JSON.stringify(r),Ps=[502,503,504];async function Et(r){var e;if(!ws(r))throw new Ge(z(r),0);if(Ps.includes(r.status))throw new Ge(z(r),r.status);let t;try{t=await r.json()}catch(i){throw new X(z(i),i)}let s;const n=As(r);if(n&&n.getTime()>=Lt["2024-01-01"].timestamp&&typeof t=="object"&&t&&typeof t.code=="string"?s=t.code:typeof t=="object"&&t&&typeof t.error_code=="string"&&(s=t.error_code),s){if(s==="weak_password")throw new vt(z(t),r.status,((e=t.weak_password)===null||e===void 0?void 0:e.reasons)||[]);if(s==="session_not_found")throw new U}else if(typeof t=="object"&&t&&typeof t.weak_password=="object"&&t.weak_password&&Array.isArray(t.weak_password.reasons)&&t.weak_password.reasons.length&&t.weak_password.reasons.reduce((i,a)=>i&&typeof a=="string",!0))throw new vt(z(t),r.status,t.weak_password.reasons);throw new as(z(t),r.status||500,s)}const js=(r,e,t,s)=>{const n={method:r,headers:(e==null?void 0:e.headers)||{}};return r==="GET"?n:(n.headers=Object.assign({"Content-Type":"application/json;charset=UTF-8"},e==null?void 0:e.headers),n.body=JSON.stringify(s),Object.assign(Object.assign({},n),t))};async function _(r,e,t,s){var n;const i=Object.assign({},s==null?void 0:s.headers);i[Je]||(i[Je]=Lt["2024-01-01"].name),s!=null&&s.jwt&&(i.Authorization=`Bearer ${s.jwt}`);const a=(n=s==null?void 0:s.query)!==null&&n!==void 0?n:{};s!=null&&s.redirectTo&&(a.redirect_to=s.redirectTo);const o=Object.keys(a).length?"?"+new URLSearchParams(a).toString():"",l=await xs(r,e,t+o,{headers:i,noResolveJson:s==null?void 0:s.noResolveJson},{},s==null?void 0:s.body);return s!=null&&s.xform?s==null?void 0:s.xform(l):{data:Object.assign({},l),error:null}}async function xs(r,e,t,s,n,i){const a=js(e,s,n,i);let o;try{o=await r(t,Object.assign({},a))}catch(l){throw console.error(l),new Ge(z(l),0)}if(o.ok||await Et(o),s!=null&&s.noResolveJson)return o;try{return await o.json()}catch(l){await Et(l)}}function D(r){var e;let t=null;Bs(r)&&(t=Object.assign({},r),r.expires_at||(t.expires_at=gs(r.expires_in)));const s=(e=r.user)!==null&&e!==void 0?e:r;return{data:{session:t,user:s},error:null}}function St(r){const e=D(r);return!e.error&&r.weak_password&&typeof r.weak_password=="object"&&Array.isArray(r.weak_password.reasons)&&r.weak_password.reasons.length&&r.weak_password.message&&typeof r.weak_password.message=="string"&&r.weak_password.reasons.reduce((t,s)=>t&&typeof s=="string",!0)&&(e.data.weak_password=r.weak_password),e}function H(r){var e;return{data:{user:(e=r.user)!==null&&e!==void 0?e:r},error:null}}function Us(r){return{data:r,error:null}}function Ns(r){const{action_link:e,email_otp:t,hashed_token:s,redirect_to:n,verification_type:i}=r,a=Ae(r,["action_link","email_otp","hashed_token","redirect_to","verification_type"]),o={action_link:e,email_otp:t,hashed_token:s,redirect_to:n,verification_type:i},l=Object.assign({},a);return{data:{properties:o,user:l},error:null}}function kt(r){return r}function Bs(r){return r.access_token&&r.refresh_token&&r.expires_in}const De=["global","local","others"];class Ds{constructor({url:e="",headers:t={},fetch:s}){this.url=e,this.headers=t,this.fetch=Ft(s),this.mfa={listFactors:this._listFactors.bind(this),deleteFactor:this._deleteFactor.bind(this)},this.oauth={listClients:this._listOAuthClients.bind(this),createClient:this._createOAuthClient.bind(this),getClient:this._getOAuthClient.bind(this),updateClient:this._updateOAuthClient.bind(this),deleteClient:this._deleteOAuthClient.bind(this),regenerateClientSecret:this._regenerateOAuthClientSecret.bind(this)}}async signOut(e,t=De[0]){if(De.indexOf(t)<0)throw new Error(`@supabase/auth-js: Parameter scope must be one of ${De.join(", ")}`);try{return await _(this.fetch,"POST",`${this.url}/logout?scope=${t}`,{headers:this.headers,jwt:e,noResolveJson:!0}),{data:null,error:null}}catch(s){if(y(s))return{data:null,error:s};throw s}}async inviteUserByEmail(e,t={}){try{return await _(this.fetch,"POST",`${this.url}/invite`,{body:{email:e,data:t.data},headers:this.headers,redirectTo:t.redirectTo,xform:H})}catch(s){if(y(s))return{data:{user:null},error:s};throw s}}async generateLink(e){try{const{options:t}=e,s=Ae(e,["options"]),n=Object.assign(Object.assign({},s),t);return"newEmail"in s&&(n.new_email=s==null?void 0:s.newEmail,delete n.newEmail),await _(this.fetch,"POST",`${this.url}/admin/generate_link`,{body:n,headers:this.headers,xform:Ns,redirectTo:t==null?void 0:t.redirectTo})}catch(t){if(y(t))return{data:{properties:null,user:null},error:t};throw t}}async createUser(e){try{return await _(this.fetch,"POST",`${this.url}/admin/users`,{body:e,headers:this.headers,xform:H})}catch(t){if(y(t))return{data:{user:null},error:t};throw t}}async listUsers(e){var t,s,n,i,a,o,l;try{const c={nextPage:null,lastPage:0,total:0},u=await _(this.fetch,"GET",`${this.url}/admin/users`,{headers:this.headers,noResolveJson:!0,query:{page:(s=(t=e==null?void 0:e.page)===null||t===void 0?void 0:t.toString())!==null&&s!==void 0?s:"",per_page:(i=(n=e==null?void 0:e.perPage)===null||n===void 0?void 0:n.toString())!==null&&i!==void 0?i:""},xform:kt});if(u.error)throw u.error;const f=await u.json(),d=(a=u.headers.get("x-total-count"))!==null&&a!==void 0?a:0,h=(l=(o=u.headers.get("link"))===null||o===void 0?void 0:o.split(","))!==null&&l!==void 0?l:[];return h.length>0&&(h.forEach(p=>{const m=parseInt(p.split(";")[0].split("=")[1].substring(0,1)),v=JSON.parse(p.split(";")[1].split("=")[1]);c[`${v}Page`]=m}),c.total=parseInt(d)),{data:Object.assign(Object.assign({},f),c),error:null}}catch(c){if(y(c))return{data:{users:[]},error:c};throw c}}async getUserById(e){re(e);try{return await _(this.fetch,"GET",`${this.url}/admin/users/${e}`,{headers:this.headers,xform:H})}catch(t){if(y(t))return{data:{user:null},error:t};throw t}}async updateUserById(e,t){re(e);try{return await _(this.fetch,"PUT",`${this.url}/admin/users/${e}`,{body:t,headers:this.headers,xform:H})}catch(s){if(y(s))return{data:{user:null},error:s};throw s}}async deleteUser(e,t=!1){re(e);try{return await _(this.fetch,"DELETE",`${this.url}/admin/users/${e}`,{headers:this.headers,body:{should_soft_delete:t},xform:H})}catch(s){if(y(s))return{data:{user:null},error:s};throw s}}async _listFactors(e){re(e.userId);try{const{data:t,error:s}=await _(this.fetch,"GET",`${this.url}/admin/users/${e.userId}/factors`,{headers:this.headers,xform:n=>({data:{factors:n},error:null})});return{data:t,error:s}}catch(t){if(y(t))return{data:null,error:t};throw t}}async _deleteFactor(e){re(e.userId),re(e.id);try{return{data:await _(this.fetch,"DELETE",`${this.url}/admin/users/${e.userId}/factors/${e.id}`,{headers:this.headers}),error:null}}catch(t){if(y(t))return{data:null,error:t};throw t}}async _listOAuthClients(e){var t,s,n,i,a,o,l;try{const c={nextPage:null,lastPage:0,total:0},u=await _(this.fetch,"GET",`${this.url}/admin/oauth/clients`,{headers:this.headers,noResolveJson:!0,query:{page:(s=(t=e==null?void 0:e.page)===null||t===void 0?void 0:t.toString())!==null&&s!==void 0?s:"",per_page:(i=(n=e==null?void 0:e.perPage)===null||n===void 0?void 0:n.toString())!==null&&i!==void 0?i:""},xform:kt});if(u.error)throw u.error;const f=await u.json(),d=(a=u.headers.get("x-total-count"))!==null&&a!==void 0?a:0,h=(l=(o=u.headers.get("link"))===null||o===void 0?void 0:o.split(","))!==null&&l!==void 0?l:[];return h.length>0&&(h.forEach(p=>{const m=parseInt(p.split(";")[0].split("=")[1].substring(0,1)),v=JSON.parse(p.split(";")[1].split("=")[1]);c[`${v}Page`]=m}),c.total=parseInt(d)),{data:Object.assign(Object.assign({},f),c),error:null}}catch(c){if(y(c))return{data:{clients:[]},error:c};throw c}}async _createOAuthClient(e){try{return await _(this.fetch,"POST",`${this.url}/admin/oauth/clients`,{body:e,headers:this.headers,xform:t=>({data:t,error:null})})}catch(t){if(y(t))return{data:null,error:t};throw t}}async _getOAuthClient(e){try{return await _(this.fetch,"GET",`${this.url}/admin/oauth/clients/${e}`,{headers:this.headers,xform:t=>({data:t,error:null})})}catch(t){if(y(t))return{data:null,error:t};throw t}}async _updateOAuthClient(e,t){try{return await _(this.fetch,"PUT",`${this.url}/admin/oauth/clients/${e}`,{body:t,headers:this.headers,xform:s=>({data:s,error:null})})}catch(s){if(y(s))return{data:null,error:s};throw s}}async _deleteOAuthClient(e){try{return await _(this.fetch,"DELETE",`${this.url}/admin/oauth/clients/${e}`,{headers:this.headers,noResolveJson:!0}),{data:null,error:null}}catch(t){if(y(t))return{data:null,error:t};throw t}}async _regenerateOAuthClientSecret(e){try{return await _(this.fetch,"POST",`${this.url}/admin/oauth/clients/${e}/regenerate_secret`,{headers:this.headers,xform:t=>({data:t,error:null})})}catch(t){if(y(t))return{data:null,error:t};throw t}}}function Tt(r={}){return{getItem:e=>r[e]||null,setItem:(e,t)=>{r[e]=t},removeItem:e=>{delete r[e]}}}const se={debug:!!(globalThis&&Mt()&&globalThis.localStorage&&globalThis.localStorage.getItem("supabase.gotrue-js.locks.debug")==="true")};class Wt extends Error{constructor(e){super(e),this.isAcquireTimeout=!0}}class Ls extends Wt{}async function qs(r,e,t){se.debug&&console.log("@supabase/gotrue-js: navigatorLock: acquire lock",r,e);const s=new globalThis.AbortController;return e>0&&setTimeout(()=>{s.abort(),se.debug&&console.log("@supabase/gotrue-js: navigatorLock acquire timed out",r)},e),await Promise.resolve().then(()=>globalThis.navigator.locks.request(r,e===0?{mode:"exclusive",ifAvailable:!0}:{mode:"exclusive",signal:s.signal},async n=>{if(n){se.debug&&console.log("@supabase/gotrue-js: navigatorLock: acquired",r,n.name);try{return await t()}finally{se.debug&&console.log("@supabase/gotrue-js: navigatorLock: released",r,n.name)}}else{if(e===0)throw se.debug&&console.log("@supabase/gotrue-js: navigatorLock: not immediately available",r),new Ls(`Acquiring an exclusive Navigator LockManager lock "${r}" immediately failed`);if(se.debug)try{const i=await globalThis.navigator.locks.query();console.log("@supabase/gotrue-js: Navigator LockManager state",JSON.stringify(i,null,"  "))}catch(i){console.warn("@supabase/gotrue-js: Error when querying Navigator LockManager state",i)}return console.warn("@supabase/gotrue-js: Navigator LockManager returned a null lock when using #request without ifAvailable set to true, it appears this browser is not following the LockManager spec https://developer.mozilla.org/en-US/docs/Web/API/LockManager/request"),await t()}}))}function Ms(){if(typeof globalThis!="object")try{Object.defineProperty(Object.prototype,"__magic__",{get:function(){return this},configurable:!0}),__magic__.globalThis=__magic__,delete Object.prototype.__magic__}catch{typeof self<"u"&&(self.globalThis=self)}}function Kt(r){if(!/^0x[a-fA-F0-9]{40}$/.test(r))throw new Error(`@supabase/auth-js: Address "${r}" is invalid.`);return r.toLowerCase()}function Fs(r){return parseInt(r,16)}function Ws(r){const e=new TextEncoder().encode(r);return"0x"+Array.from(e,s=>s.toString(16).padStart(2,"0")).join("")}function Ks(r){var e;const{chainId:t,domain:s,expirationTime:n,issuedAt:i=new Date,nonce:a,notBefore:o,requestId:l,resources:c,scheme:u,uri:f,version:d}=r;{if(!Number.isInteger(t))throw new Error(`@supabase/auth-js: Invalid SIWE message field "chainId". Chain ID must be a EIP-155 chain ID. Provided value: ${t}`);if(!s)throw new Error('@supabase/auth-js: Invalid SIWE message field "domain". Domain must be provided.');if(a&&a.length<8)throw new Error(`@supabase/auth-js: Invalid SIWE message field "nonce". Nonce must be at least 8 characters. Provided value: ${a}`);if(!f)throw new Error('@supabase/auth-js: Invalid SIWE message field "uri". URI must be provided.');if(d!=="1")throw new Error(`@supabase/auth-js: Invalid SIWE message field "version". Version must be '1'. Provided value: ${d}`);if(!((e=r.statement)===null||e===void 0)&&e.includes(`
`))throw new Error(`@supabase/auth-js: Invalid SIWE message field "statement". Statement must not include '\\n'. Provided value: ${r.statement}`)}const h=Kt(r.address),p=u?`${u}://${s}`:s,m=r.statement?`${r.statement}
`:"",v=`${p} wants you to sign in with your Ethereum account:
${h}

${m}`;let w=`URI: ${f}
Version: ${d}
Chain ID: ${t}${a?`
Nonce: ${a}`:""}
Issued At: ${i.toISOString()}`;if(n&&(w+=`
Expiration Time: ${n.toISOString()}`),o&&(w+=`
Not Before: ${o.toISOString()}`),l&&(w+=`
Request ID: ${l}`),c){let b=`
Resources:`;for(const g of c){if(!g||typeof g!="string")throw new Error(`@supabase/auth-js: Invalid SIWE message field "resources". Every resource must be a valid string. Provided value: ${g}`);b+=`
- ${g}`}w+=b}return`${v}
${w}`}class C extends Error{constructor({message:e,code:t,cause:s,name:n}){var i;super(e,{cause:s}),this.__isWebAuthnError=!0,this.name=(i=n??(s instanceof Error?s.name:void 0))!==null&&i!==void 0?i:"Unknown Error",this.code=t}}class Te extends C{constructor(e,t){super({code:"ERROR_PASSTHROUGH_SEE_CAUSE_PROPERTY",cause:t,message:e}),this.name="WebAuthnUnknownError",this.originalError=t}}function Vs({error:r,options:e}){var t,s,n;const{publicKey:i}=e;if(!i)throw Error("options was missing required publicKey property");if(r.name==="AbortError"){if(e.signal instanceof AbortSignal)return new C({message:"Registration ceremony was sent an abort signal",code:"ERROR_CEREMONY_ABORTED",cause:r})}else if(r.name==="ConstraintError"){if(((t=i.authenticatorSelection)===null||t===void 0?void 0:t.requireResidentKey)===!0)return new C({message:"Discoverable credentials were required but no available authenticator supported it",code:"ERROR_AUTHENTICATOR_MISSING_DISCOVERABLE_CREDENTIAL_SUPPORT",cause:r});if(e.mediation==="conditional"&&((s=i.authenticatorSelection)===null||s===void 0?void 0:s.userVerification)==="required")return new C({message:"User verification was required during automatic registration but it could not be performed",code:"ERROR_AUTO_REGISTER_USER_VERIFICATION_FAILURE",cause:r});if(((n=i.authenticatorSelection)===null||n===void 0?void 0:n.userVerification)==="required")return new C({message:"User verification was required but no available authenticator supported it",code:"ERROR_AUTHENTICATOR_MISSING_USER_VERIFICATION_SUPPORT",cause:r})}else{if(r.name==="InvalidStateError")return new C({message:"The authenticator was previously registered",code:"ERROR_AUTHENTICATOR_PREVIOUSLY_REGISTERED",cause:r});if(r.name==="NotAllowedError")return new C({message:r.message,code:"ERROR_PASSTHROUGH_SEE_CAUSE_PROPERTY",cause:r});if(r.name==="NotSupportedError")return i.pubKeyCredParams.filter(o=>o.type==="public-key").length===0?new C({message:'No entry in pubKeyCredParams was of type "public-key"',code:"ERROR_MALFORMED_PUBKEYCREDPARAMS",cause:r}):new C({message:"No available authenticator supported any of the specified pubKeyCredParams algorithms",code:"ERROR_AUTHENTICATOR_NO_SUPPORTED_PUBKEYCREDPARAMS_ALG",cause:r});if(r.name==="SecurityError"){const a=window.location.hostname;if(Vt(a)){if(i.rp.id!==a)return new C({message:`The RP ID "${i.rp.id}" is invalid for this domain`,code:"ERROR_INVALID_RP_ID",cause:r})}else return new C({message:`${window.location.hostname} is an invalid domain`,code:"ERROR_INVALID_DOMAIN",cause:r})}else if(r.name==="TypeError"){if(i.user.id.byteLength<1||i.user.id.byteLength>64)return new C({message:"User ID was not between 1 and 64 characters",code:"ERROR_INVALID_USER_ID_LENGTH",cause:r})}else if(r.name==="UnknownError")return new C({message:"The authenticator was unable to process the specified options, or could not create a new credential",code:"ERROR_AUTHENTICATOR_GENERAL_ERROR",cause:r})}return new C({message:"a Non-Webauthn related error has occurred",code:"ERROR_PASSTHROUGH_SEE_CAUSE_PROPERTY",cause:r})}function Hs({error:r,options:e}){const{publicKey:t}=e;if(!t)throw Error("options was missing required publicKey property");if(r.name==="AbortError"){if(e.signal instanceof AbortSignal)return new C({message:"Authentication ceremony was sent an abort signal",code:"ERROR_CEREMONY_ABORTED",cause:r})}else{if(r.name==="NotAllowedError")return new C({message:r.message,code:"ERROR_PASSTHROUGH_SEE_CAUSE_PROPERTY",cause:r});if(r.name==="SecurityError"){const s=window.location.hostname;if(Vt(s)){if(t.rpId!==s)return new C({message:`The RP ID "${t.rpId}" is invalid for this domain`,code:"ERROR_INVALID_RP_ID",cause:r})}else return new C({message:`${window.location.hostname} is an invalid domain`,code:"ERROR_INVALID_DOMAIN",cause:r})}else if(r.name==="UnknownError")return new C({message:"The authenticator was unable to process the specified options, or could not create a new assertion signature",code:"ERROR_AUTHENTICATOR_GENERAL_ERROR",cause:r})}return new C({message:"a Non-Webauthn related error has occurred",code:"ERROR_PASSTHROUGH_SEE_CAUSE_PROPERTY",cause:r})}class Js{createNewAbortSignal(){if(this.controller){const t=new Error("Cancelling existing WebAuthn API call for new one");t.name="AbortError",this.controller.abort(t)}const e=new AbortController;return this.controller=e,e.signal}cancelCeremony(){if(this.controller){const e=new Error("Manually cancelling existing WebAuthn API call");e.name="AbortError",this.controller.abort(e),this.controller=void 0}}}const Gs=new Js;function zs(r){if(!r)throw new Error("Credential creation options are required");if(typeof PublicKeyCredential<"u"&&"parseCreationOptionsFromJSON"in PublicKeyCredential&&typeof PublicKeyCredential.parseCreationOptionsFromJSON=="function")return PublicKeyCredential.parseCreationOptionsFromJSON(r);const{challenge:e,user:t,excludeCredentials:s}=r,n=Ae(r,["challenge","user","excludeCredentials"]),i=ce(e).buffer,a=Object.assign(Object.assign({},t),{id:ce(t.id).buffer}),o=Object.assign(Object.assign({},n),{challenge:i,user:a});if(s&&s.length>0){o.excludeCredentials=new Array(s.length);for(let l=0;l<s.length;l++){const c=s[l];o.excludeCredentials[l]=Object.assign(Object.assign({},c),{id:ce(c.id).buffer,type:c.type||"public-key",transports:c.transports})}}return o}function Ys(r){if(!r)throw new Error("Credential request options are required");if(typeof PublicKeyCredential<"u"&&"parseRequestOptionsFromJSON"in PublicKeyCredential&&typeof PublicKeyCredential.parseRequestOptionsFromJSON=="function")return PublicKeyCredential.parseRequestOptionsFromJSON(r);const{challenge:e,allowCredentials:t}=r,s=Ae(r,["challenge","allowCredentials"]),n=ce(e).buffer,i=Object.assign(Object.assign({},s),{challenge:n});if(t&&t.length>0){i.allowCredentials=new Array(t.length);for(let a=0;a<t.length;a++){const o=t[a];i.allowCredentials[a]=Object.assign(Object.assign({},o),{id:ce(o.id).buffer,type:o.type||"public-key",transports:o.transports})}}return i}function Xs(r){var e;if("toJSON"in r&&typeof r.toJSON=="function")return r.toJSON();const t=r;return{id:r.id,rawId:r.id,response:{attestationObject:Q(new Uint8Array(r.response.attestationObject)),clientDataJSON:Q(new Uint8Array(r.response.clientDataJSON))},type:"public-key",clientExtensionResults:r.getClientExtensionResults(),authenticatorAttachment:(e=t.authenticatorAttachment)!==null&&e!==void 0?e:void 0}}function Qs(r){var e;if("toJSON"in r&&typeof r.toJSON=="function")return r.toJSON();const t=r,s=r.getClientExtensionResults(),n=r.response;return{id:r.id,rawId:r.id,response:{authenticatorData:Q(new Uint8Array(n.authenticatorData)),clientDataJSON:Q(new Uint8Array(n.clientDataJSON)),signature:Q(new Uint8Array(n.signature)),userHandle:n.userHandle?Q(new Uint8Array(n.userHandle)):void 0},type:"public-key",clientExtensionResults:s,authenticatorAttachment:(e=t.authenticatorAttachment)!==null&&e!==void 0?e:void 0}}function Vt(r){return r==="localhost"||/^([a-z0-9]+(-[a-z0-9]+)*\.)+[a-z]{2,}$/i.test(r)}function Ot(){var r,e;return!!(j()&&"PublicKeyCredential"in window&&window.PublicKeyCredential&&"credentials"in navigator&&typeof((r=navigator==null?void 0:navigator.credentials)===null||r===void 0?void 0:r.create)=="function"&&typeof((e=navigator==null?void 0:navigator.credentials)===null||e===void 0?void 0:e.get)=="function")}async function Zs(r){try{const e=await navigator.credentials.create(r);return e?e instanceof PublicKeyCredential?{data:e,error:null}:{data:null,error:new Te("Browser returned unexpected credential type",e)}:{data:null,error:new Te("Empty credential response",e)}}catch(e){return{data:null,error:Vs({error:e,options:r})}}}async function en(r){try{const e=await navigator.credentials.get(r);return e?e instanceof PublicKeyCredential?{data:e,error:null}:{data:null,error:new Te("Browser returned unexpected credential type",e)}:{data:null,error:new Te("Empty credential response",e)}}catch(e){return{data:null,error:Hs({error:e,options:r})}}}const tn={hints:["security-key"],authenticatorSelection:{authenticatorAttachment:"cross-platform",requireResidentKey:!1,userVerification:"preferred",residentKey:"discouraged"},attestation:"direct"},rn={userVerification:"preferred",hints:["security-key"],attestation:"direct"};function Oe(...r){const e=n=>n!==null&&typeof n=="object"&&!Array.isArray(n),t=n=>n instanceof ArrayBuffer||ArrayBuffer.isView(n),s={};for(const n of r)if(n)for(const i in n){const a=n[i];if(a!==void 0)if(Array.isArray(a))s[i]=a;else if(t(a))s[i]=a;else if(e(a)){const o=s[i];e(o)?s[i]=Oe(o,a):s[i]=Oe(a)}else s[i]=a}return s}function sn(r,e){return Oe(tn,r,e||{})}function nn(r,e){return Oe(rn,r,e||{})}class an{constructor(e){this.client=e,this.enroll=this._enroll.bind(this),this.challenge=this._challenge.bind(this),this.verify=this._verify.bind(this),this.authenticate=this._authenticate.bind(this),this.register=this._register.bind(this)}async _enroll(e){return this.client.mfa.enroll(Object.assign(Object.assign({},e),{factorType:"webauthn"}))}async _challenge({factorId:e,webauthn:t,friendlyName:s,signal:n},i){try{const{data:a,error:o}=await this.client.mfa.challenge({factorId:e,webauthn:t});if(!a)return{data:null,error:o};const l=n??Gs.createNewAbortSignal();if(a.webauthn.type==="create"){const{user:c}=a.webauthn.credential_options.publicKey;c.name||(c.name=`${c.id}:${s}`),c.displayName||(c.displayName=c.name)}switch(a.webauthn.type){case"create":{const c=sn(a.webauthn.credential_options.publicKey,i==null?void 0:i.create),{data:u,error:f}=await Zs({publicKey:c,signal:l});return u?{data:{factorId:e,challengeId:a.id,webauthn:{type:a.webauthn.type,credential_response:u}},error:null}:{data:null,error:f}}case"request":{const c=nn(a.webauthn.credential_options.publicKey,i==null?void 0:i.request),{data:u,error:f}=await en(Object.assign(Object.assign({},a.webauthn.credential_options),{publicKey:c,signal:l}));return u?{data:{factorId:e,challengeId:a.id,webauthn:{type:a.webauthn.type,credential_response:u}},error:null}:{data:null,error:f}}}}catch(a){return y(a)?{data:null,error:a}:{data:null,error:new X("Unexpected error in challenge",a)}}}async _verify({challengeId:e,factorId:t,webauthn:s}){return this.client.mfa.verify({factorId:t,challengeId:e,webauthn:s})}async _authenticate({factorId:e,webauthn:{rpId:t=typeof window<"u"?window.location.hostname:void 0,rpOrigins:s=typeof window<"u"?[window.location.origin]:void 0,signal:n}={}},i){if(!t)return{data:null,error:new ge("rpId is required for WebAuthn authentication")};try{if(!Ot())return{data:null,error:new X("Browser does not support WebAuthn",null)};const{data:a,error:o}=await this.challenge({factorId:e,webauthn:{rpId:t,rpOrigins:s},signal:n},{request:i});if(!a)return{data:null,error:o};const{webauthn:l}=a;return this._verify({factorId:e,challengeId:a.challengeId,webauthn:{type:l.type,rpId:t,rpOrigins:s,credential_response:l.credential_response}})}catch(a){return y(a)?{data:null,error:a}:{data:null,error:new X("Unexpected error in authenticate",a)}}}async _register({friendlyName:e,webauthn:{rpId:t=typeof window<"u"?window.location.hostname:void 0,rpOrigins:s=typeof window<"u"?[window.location.origin]:void 0,signal:n}={}},i){if(!t)return{data:null,error:new ge("rpId is required for WebAuthn registration")};try{if(!Ot())return{data:null,error:new X("Browser does not support WebAuthn",null)};const{data:a,error:o}=await this._enroll({friendlyName:e});if(!a)return await this.client.mfa.listFactors().then(u=>{var f;return(f=u.data)===null||f===void 0?void 0:f.all.find(d=>d.factor_type==="webauthn"&&d.friendly_name===e&&d.status!=="unverified")}).then(u=>u?this.client.mfa.unenroll({factorId:u==null?void 0:u.id}):void 0),{data:null,error:o};const{data:l,error:c}=await this._challenge({factorId:a.id,friendlyName:a.friendly_name,webauthn:{rpId:t,rpOrigins:s},signal:n},{create:i});return l?this._verify({factorId:a.id,challengeId:l.challengeId,webauthn:{rpId:t,rpOrigins:s,type:l.webauthn.type,credential_response:l.webauthn.credential_response}}):{data:null,error:c}}catch(a){return y(a)?{data:null,error:a}:{data:null,error:new X("Unexpected error in register",a)}}}}Ms();const on={url:ts,storageKey:rs,autoRefreshToken:!0,persistSession:!0,detectSessionInUrl:!0,headers:ss,flowType:"implicit",debug:!1,hasCustomAuthorizationHeader:!1,throwOnError:!1,lockAcquireTimeout:1e4};async function At(r,e,t){return await t()}const ne={};class ve{get jwks(){var e,t;return(t=(e=ne[this.storageKey])===null||e===void 0?void 0:e.jwks)!==null&&t!==void 0?t:{keys:[]}}set jwks(e){ne[this.storageKey]=Object.assign(Object.assign({},ne[this.storageKey]),{jwks:e})}get jwks_cached_at(){var e,t;return(t=(e=ne[this.storageKey])===null||e===void 0?void 0:e.cachedAt)!==null&&t!==void 0?t:Number.MIN_SAFE_INTEGER}set jwks_cached_at(e){ne[this.storageKey]=Object.assign(Object.assign({},ne[this.storageKey]),{cachedAt:e})}constructor(e){var t,s,n;this.userStorage=null,this.memoryStorage=null,this.stateChangeEmitters=new Map,this.autoRefreshTicker=null,this.autoRefreshTickTimeout=null,this.visibilityChangedCallback=null,this.refreshingDeferred=null,this.initializePromise=null,this.detectSessionInUrl=!0,this.hasCustomAuthorizationHeader=!1,this.suppressGetSessionWarning=!1,this.lockAcquired=!1,this.pendingInLock=[],this.broadcastChannel=null,this.logger=console.log;const i=Object.assign(Object.assign({},on),e);if(this.storageKey=i.storageKey,this.instanceID=(t=ve.nextInstanceID[this.storageKey])!==null&&t!==void 0?t:0,ve.nextInstanceID[this.storageKey]=this.instanceID+1,this.logDebugMessages=!!i.debug,typeof i.debug=="function"&&(this.logger=i.debug),this.instanceID>0&&j()){const a=`${this._logPrefix()} Multiple GoTrueClient instances detected in the same browser context. It is not an error, but this should be avoided as it may produce undefined behavior when used concurrently under the same storage key.`;console.warn(a),this.logDebugMessages&&console.trace(a)}if(this.persistSession=i.persistSession,this.autoRefreshToken=i.autoRefreshToken,this.admin=new Ds({url:i.url,headers:i.headers,fetch:i.fetch}),this.url=i.url,this.headers=i.headers,this.fetch=Ft(i.fetch),this.lock=i.lock||At,this.detectSessionInUrl=i.detectSessionInUrl,this.flowType=i.flowType,this.hasCustomAuthorizationHeader=i.hasCustomAuthorizationHeader,this.throwOnError=i.throwOnError,this.lockAcquireTimeout=i.lockAcquireTimeout,i.lock?this.lock=i.lock:this.persistSession&&j()&&(!((s=globalThis==null?void 0:globalThis.navigator)===null||s===void 0)&&s.locks)?this.lock=qs:this.lock=At,this.jwks||(this.jwks={keys:[]},this.jwks_cached_at=Number.MIN_SAFE_INTEGER),this.mfa={verify:this._verify.bind(this),enroll:this._enroll.bind(this),unenroll:this._unenroll.bind(this),challenge:this._challenge.bind(this),listFactors:this._listFactors.bind(this),challengeAndVerify:this._challengeAndVerify.bind(this),getAuthenticatorAssuranceLevel:this._getAuthenticatorAssuranceLevel.bind(this),webauthn:new an(this)},this.oauth={getAuthorizationDetails:this._getAuthorizationDetails.bind(this),approveAuthorization:this._approveAuthorization.bind(this),denyAuthorization:this._denyAuthorization.bind(this),listGrants:this._listOAuthGrants.bind(this),revokeGrant:this._revokeOAuthGrant.bind(this)},this.persistSession?(i.storage?this.storage=i.storage:Mt()?this.storage=globalThis.localStorage:(this.memoryStorage={},this.storage=Tt(this.memoryStorage)),i.userStorage&&(this.userStorage=i.userStorage)):(this.memoryStorage={},this.storage=Tt(this.memoryStorage)),j()&&globalThis.BroadcastChannel&&this.persistSession&&this.storageKey){try{this.broadcastChannel=new globalThis.BroadcastChannel(this.storageKey)}catch(a){console.error("Failed to create a new BroadcastChannel, multi-tab state changes will not be available",a)}(n=this.broadcastChannel)===null||n===void 0||n.addEventListener("message",async a=>{this._debug("received broadcast notification from other tab or client",a),await this._notifyAllSubscribers(a.data.event,a.data.session,!1)})}this.initialize()}isThrowOnErrorEnabled(){return this.throwOnError}_returnResult(e){if(this.throwOnError&&e&&e.error)throw e.error;return e}_logPrefix(){return`GoTrueClient@${this.storageKey}:${this.instanceID} (${Dt}) ${new Date().toISOString()}`}_debug(...e){return this.logDebugMessages&&this.logger(this._logPrefix(),...e),this}async initialize(){return this.initializePromise?await this.initializePromise:(this.initializePromise=(async()=>await this._acquireLock(this.lockAcquireTimeout,async()=>await this._initialize()))(),await this.initializePromise)}async _initialize(){var e;try{let t={},s="none";if(j()&&(t=ys(window.location.href),this._isImplicitGrantCallback(t)?s="implicit":await this._isPKCECallback(t)&&(s="pkce")),j()&&this.detectSessionInUrl&&s!=="none"){const{data:n,error:i}=await this._getSessionFromURL(t,s);if(i){if(this._debug("#_initialize()","error detecting session from URL",i),cs(i)){const l=(e=i.details)===null||e===void 0?void 0:e.code;if(l==="identity_already_exists"||l==="identity_not_found"||l==="single_identity_not_deletable")return{error:i}}return{error:i}}const{session:a,redirectType:o}=n;return this._debug("#_initialize()","detected session in URL",a,"redirect type",o),await this._saveSession(a),setTimeout(async()=>{o==="recovery"?await this._notifyAllSubscribers("PASSWORD_RECOVERY",a):await this._notifyAllSubscribers("SIGNED_IN",a)},0),{error:null}}return await this._recoverAndRefresh(),{error:null}}catch(t){return y(t)?this._returnResult({error:t}):this._returnResult({error:new X("Unexpected error during initialization",t)})}finally{await this._handleVisibilityChange(),this._debug("#_initialize()","end")}}async signInAnonymously(e){var t,s,n;try{const i=await _(this.fetch,"POST",`${this.url}/signup`,{headers:this.headers,body:{data:(s=(t=e==null?void 0:e.options)===null||t===void 0?void 0:t.data)!==null&&s!==void 0?s:{},gotrue_meta_security:{captcha_token:(n=e==null?void 0:e.options)===null||n===void 0?void 0:n.captchaToken}},xform:D}),{data:a,error:o}=i;if(o||!a)return this._returnResult({data:{user:null,session:null},error:o});const l=a.session,c=a.user;return a.session&&(await this._saveSession(a.session),await this._notifyAllSubscribers("SIGNED_IN",l)),this._returnResult({data:{user:c,session:l},error:null})}catch(i){if(y(i))return this._returnResult({data:{user:null,session:null},error:i});throw i}}async signUp(e){var t,s,n;try{let i;if("email"in e){const{email:u,password:f,options:d}=e;let h=null,p=null;this.flowType==="pkce"&&([h,p]=await te(this.storage,this.storageKey)),i=await _(this.fetch,"POST",`${this.url}/signup`,{headers:this.headers,redirectTo:d==null?void 0:d.emailRedirectTo,body:{email:u,password:f,data:(t=d==null?void 0:d.data)!==null&&t!==void 0?t:{},gotrue_meta_security:{captcha_token:d==null?void 0:d.captchaToken},code_challenge:h,code_challenge_method:p},xform:D})}else if("phone"in e){const{phone:u,password:f,options:d}=e;i=await _(this.fetch,"POST",`${this.url}/signup`,{headers:this.headers,body:{phone:u,password:f,data:(s=d==null?void 0:d.data)!==null&&s!==void 0?s:{},channel:(n=d==null?void 0:d.channel)!==null&&n!==void 0?n:"sms",gotrue_meta_security:{captcha_token:d==null?void 0:d.captchaToken}},xform:D})}else throw new Ee("You must provide either an email or phone number and a password");const{data:a,error:o}=i;if(o||!a)return await P(this.storage,`${this.storageKey}-code-verifier`),this._returnResult({data:{user:null,session:null},error:o});const l=a.session,c=a.user;return a.session&&(await this._saveSession(a.session),await this._notifyAllSubscribers("SIGNED_IN",l)),this._returnResult({data:{user:c,session:l},error:null})}catch(i){if(await P(this.storage,`${this.storageKey}-code-verifier`),y(i))return this._returnResult({data:{user:null,session:null},error:i});throw i}}async signInWithPassword(e){try{let t;if("email"in e){const{email:i,password:a,options:o}=e;t=await _(this.fetch,"POST",`${this.url}/token?grant_type=password`,{headers:this.headers,body:{email:i,password:a,gotrue_meta_security:{captcha_token:o==null?void 0:o.captchaToken}},xform:St})}else if("phone"in e){const{phone:i,password:a,options:o}=e;t=await _(this.fetch,"POST",`${this.url}/token?grant_type=password`,{headers:this.headers,body:{phone:i,password:a,gotrue_meta_security:{captcha_token:o==null?void 0:o.captchaToken}},xform:St})}else throw new Ee("You must provide either an email or phone number and a password");const{data:s,error:n}=t;if(n)return this._returnResult({data:{user:null,session:null},error:n});if(!s||!s.session||!s.user){const i=new ee;return this._returnResult({data:{user:null,session:null},error:i})}return s.session&&(await this._saveSession(s.session),await this._notifyAllSubscribers("SIGNED_IN",s.session)),this._returnResult({data:Object.assign({user:s.user,session:s.session},s.weak_password?{weakPassword:s.weak_password}:null),error:n})}catch(t){if(y(t))return this._returnResult({data:{user:null,session:null},error:t});throw t}}async signInWithOAuth(e){var t,s,n,i;return await this._handleProviderSignIn(e.provider,{redirectTo:(t=e.options)===null||t===void 0?void 0:t.redirectTo,scopes:(s=e.options)===null||s===void 0?void 0:s.scopes,queryParams:(n=e.options)===null||n===void 0?void 0:n.queryParams,skipBrowserRedirect:(i=e.options)===null||i===void 0?void 0:i.skipBrowserRedirect})}async exchangeCodeForSession(e){return await this.initializePromise,this._acquireLock(this.lockAcquireTimeout,async()=>this._exchangeCodeForSession(e))}async signInWithWeb3(e){const{chain:t}=e;switch(t){case"ethereum":return await this.signInWithEthereum(e);case"solana":return await this.signInWithSolana(e);default:throw new Error(`@supabase/auth-js: Unsupported chain "${t}"`)}}async signInWithEthereum(e){var t,s,n,i,a,o,l,c,u,f,d;let h,p;if("message"in e)h=e.message,p=e.signature;else{const{chain:m,wallet:v,statement:w,options:b}=e;let g;if(j())if(typeof v=="object")g=v;else{const M=window;if("ethereum"in M&&typeof M.ethereum=="object"&&"request"in M.ethereum&&typeof M.ethereum.request=="function")g=M.ethereum;else throw new Error("@supabase/auth-js: No compatible Ethereum wallet interface on the window object (window.ethereum) detected. Make sure the user already has a wallet installed and connected for this app. Prefer passing the wallet interface object directly to signInWithWeb3({ chain: 'ethereum', wallet: resolvedUserWallet }) instead.")}else{if(typeof v!="object"||!(b!=null&&b.url))throw new Error("@supabase/auth-js: Both wallet and url must be specified in non-browser environments.");g=v}const S=new URL((t=b==null?void 0:b.url)!==null&&t!==void 0?t:window.location.href),x=await g.request({method:"eth_requestAccounts"}).then(M=>M).catch(()=>{throw new Error("@supabase/auth-js: Wallet method eth_requestAccounts is missing or invalid")});if(!x||x.length===0)throw new Error("@supabase/auth-js: No accounts available. Please ensure the wallet is connected.");const T=Kt(x[0]);let A=(s=b==null?void 0:b.signInWithEthereum)===null||s===void 0?void 0:s.chainId;if(!A){const M=await g.request({method:"eth_chainId"});A=Fs(M)}const K={domain:S.host,address:T,statement:w,uri:S.href,version:"1",chainId:A,nonce:(n=b==null?void 0:b.signInWithEthereum)===null||n===void 0?void 0:n.nonce,issuedAt:(a=(i=b==null?void 0:b.signInWithEthereum)===null||i===void 0?void 0:i.issuedAt)!==null&&a!==void 0?a:new Date,expirationTime:(o=b==null?void 0:b.signInWithEthereum)===null||o===void 0?void 0:o.expirationTime,notBefore:(l=b==null?void 0:b.signInWithEthereum)===null||l===void 0?void 0:l.notBefore,requestId:(c=b==null?void 0:b.signInWithEthereum)===null||c===void 0?void 0:c.requestId,resources:(u=b==null?void 0:b.signInWithEthereum)===null||u===void 0?void 0:u.resources};h=Ks(K),p=await g.request({method:"personal_sign",params:[Ws(h),T]})}try{const{data:m,error:v}=await _(this.fetch,"POST",`${this.url}/token?grant_type=web3`,{headers:this.headers,body:Object.assign({chain:"ethereum",message:h,signature:p},!((f=e.options)===null||f===void 0)&&f.captchaToken?{gotrue_meta_security:{captcha_token:(d=e.options)===null||d===void 0?void 0:d.captchaToken}}:null),xform:D});if(v)throw v;if(!m||!m.session||!m.user){const w=new ee;return this._returnResult({data:{user:null,session:null},error:w})}return m.session&&(await this._saveSession(m.session),await this._notifyAllSubscribers("SIGNED_IN",m.session)),this._returnResult({data:Object.assign({},m),error:v})}catch(m){if(y(m))return this._returnResult({data:{user:null,session:null},error:m});throw m}}async signInWithSolana(e){var t,s,n,i,a,o,l,c,u,f,d,h;let p,m;if("message"in e)p=e.message,m=e.signature;else{const{chain:v,wallet:w,statement:b,options:g}=e;let S;if(j())if(typeof w=="object")S=w;else{const T=window;if("solana"in T&&typeof T.solana=="object"&&("signIn"in T.solana&&typeof T.solana.signIn=="function"||"signMessage"in T.solana&&typeof T.solana.signMessage=="function"))S=T.solana;else throw new Error("@supabase/auth-js: No compatible Solana wallet interface on the window object (window.solana) detected. Make sure the user already has a wallet installed and connected for this app. Prefer passing the wallet interface object directly to signInWithWeb3({ chain: 'solana', wallet: resolvedUserWallet }) instead.")}else{if(typeof w!="object"||!(g!=null&&g.url))throw new Error("@supabase/auth-js: Both wallet and url must be specified in non-browser environments.");S=w}const x=new URL((t=g==null?void 0:g.url)!==null&&t!==void 0?t:window.location.href);if("signIn"in S&&S.signIn){const T=await S.signIn(Object.assign(Object.assign(Object.assign({issuedAt:new Date().toISOString()},g==null?void 0:g.signInWithSolana),{version:"1",domain:x.host,uri:x.href}),b?{statement:b}:null));let A;if(Array.isArray(T)&&T[0]&&typeof T[0]=="object")A=T[0];else if(T&&typeof T=="object"&&"signedMessage"in T&&"signature"in T)A=T;else throw new Error("@supabase/auth-js: Wallet method signIn() returned unrecognized value");if("signedMessage"in A&&"signature"in A&&(typeof A.signedMessage=="string"||A.signedMessage instanceof Uint8Array)&&A.signature instanceof Uint8Array)p=typeof A.signedMessage=="string"?A.signedMessage:new TextDecoder().decode(A.signedMessage),m=A.signature;else throw new Error("@supabase/auth-js: Wallet method signIn() API returned object without signedMessage and signature fields")}else{if(!("signMessage"in S)||typeof S.signMessage!="function"||!("publicKey"in S)||typeof S!="object"||!S.publicKey||!("toBase58"in S.publicKey)||typeof S.publicKey.toBase58!="function")throw new Error("@supabase/auth-js: Wallet does not have a compatible signMessage() and publicKey.toBase58() API");p=[`${x.host} wants you to sign in with your Solana account:`,S.publicKey.toBase58(),...b?["",b,""]:[""],"Version: 1",`URI: ${x.href}`,`Issued At: ${(n=(s=g==null?void 0:g.signInWithSolana)===null||s===void 0?void 0:s.issuedAt)!==null&&n!==void 0?n:new Date().toISOString()}`,...!((i=g==null?void 0:g.signInWithSolana)===null||i===void 0)&&i.notBefore?[`Not Before: ${g.signInWithSolana.notBefore}`]:[],...!((a=g==null?void 0:g.signInWithSolana)===null||a===void 0)&&a.expirationTime?[`Expiration Time: ${g.signInWithSolana.expirationTime}`]:[],...!((o=g==null?void 0:g.signInWithSolana)===null||o===void 0)&&o.chainId?[`Chain ID: ${g.signInWithSolana.chainId}`]:[],...!((l=g==null?void 0:g.signInWithSolana)===null||l===void 0)&&l.nonce?[`Nonce: ${g.signInWithSolana.nonce}`]:[],...!((c=g==null?void 0:g.signInWithSolana)===null||c===void 0)&&c.requestId?[`Request ID: ${g.signInWithSolana.requestId}`]:[],...!((f=(u=g==null?void 0:g.signInWithSolana)===null||u===void 0?void 0:u.resources)===null||f===void 0)&&f.length?["Resources",...g.signInWithSolana.resources.map(A=>`- ${A}`)]:[]].join(`
`);const T=await S.signMessage(new TextEncoder().encode(p),"utf8");if(!T||!(T instanceof Uint8Array))throw new Error("@supabase/auth-js: Wallet signMessage() API returned an recognized value");m=T}}try{const{data:v,error:w}=await _(this.fetch,"POST",`${this.url}/token?grant_type=web3`,{headers:this.headers,body:Object.assign({chain:"solana",message:p,signature:Q(m)},!((d=e.options)===null||d===void 0)&&d.captchaToken?{gotrue_meta_security:{captcha_token:(h=e.options)===null||h===void 0?void 0:h.captchaToken}}:null),xform:D});if(w)throw w;if(!v||!v.session||!v.user){const b=new ee;return this._returnResult({data:{user:null,session:null},error:b})}return v.session&&(await this._saveSession(v.session),await this._notifyAllSubscribers("SIGNED_IN",v.session)),this._returnResult({data:Object.assign({},v),error:w})}catch(v){if(y(v))return this._returnResult({data:{user:null,session:null},error:v});throw v}}async _exchangeCodeForSession(e){const t=await G(this.storage,`${this.storageKey}-code-verifier`),[s,n]=(t??"").split("/");try{if(!s&&this.flowType==="pkce")throw new us;const{data:i,error:a}=await _(this.fetch,"POST",`${this.url}/token?grant_type=pkce`,{headers:this.headers,body:{auth_code:e,code_verifier:s},xform:D});if(await P(this.storage,`${this.storageKey}-code-verifier`),a)throw a;if(!i||!i.session||!i.user){const o=new ee;return this._returnResult({data:{user:null,session:null,redirectType:null},error:o})}return i.session&&(await this._saveSession(i.session),await this._notifyAllSubscribers("SIGNED_IN",i.session)),this._returnResult({data:Object.assign(Object.assign({},i),{redirectType:n??null}),error:a})}catch(i){if(await P(this.storage,`${this.storageKey}-code-verifier`),y(i))return this._returnResult({data:{user:null,session:null,redirectType:null},error:i});throw i}}async signInWithIdToken(e){try{const{options:t,provider:s,token:n,access_token:i,nonce:a}=e,o=await _(this.fetch,"POST",`${this.url}/token?grant_type=id_token`,{headers:this.headers,body:{provider:s,id_token:n,access_token:i,nonce:a,gotrue_meta_security:{captcha_token:t==null?void 0:t.captchaToken}},xform:D}),{data:l,error:c}=o;if(c)return this._returnResult({data:{user:null,session:null},error:c});if(!l||!l.session||!l.user){const u=new ee;return this._returnResult({data:{user:null,session:null},error:u})}return l.session&&(await this._saveSession(l.session),await this._notifyAllSubscribers("SIGNED_IN",l.session)),this._returnResult({data:l,error:c})}catch(t){if(y(t))return this._returnResult({data:{user:null,session:null},error:t});throw t}}async signInWithOtp(e){var t,s,n,i,a;try{if("email"in e){const{email:o,options:l}=e;let c=null,u=null;this.flowType==="pkce"&&([c,u]=await te(this.storage,this.storageKey));const{error:f}=await _(this.fetch,"POST",`${this.url}/otp`,{headers:this.headers,body:{email:o,data:(t=l==null?void 0:l.data)!==null&&t!==void 0?t:{},create_user:(s=l==null?void 0:l.shouldCreateUser)!==null&&s!==void 0?s:!0,gotrue_meta_security:{captcha_token:l==null?void 0:l.captchaToken},code_challenge:c,code_challenge_method:u},redirectTo:l==null?void 0:l.emailRedirectTo});return this._returnResult({data:{user:null,session:null},error:f})}if("phone"in e){const{phone:o,options:l}=e,{data:c,error:u}=await _(this.fetch,"POST",`${this.url}/otp`,{headers:this.headers,body:{phone:o,data:(n=l==null?void 0:l.data)!==null&&n!==void 0?n:{},create_user:(i=l==null?void 0:l.shouldCreateUser)!==null&&i!==void 0?i:!0,gotrue_meta_security:{captcha_token:l==null?void 0:l.captchaToken},channel:(a=l==null?void 0:l.channel)!==null&&a!==void 0?a:"sms"}});return this._returnResult({data:{user:null,session:null,messageId:c==null?void 0:c.message_id},error:u})}throw new Ee("You must provide either an email or phone number.")}catch(o){if(await P(this.storage,`${this.storageKey}-code-verifier`),y(o))return this._returnResult({data:{user:null,session:null},error:o});throw o}}async verifyOtp(e){var t,s;try{let n,i;"options"in e&&(n=(t=e.options)===null||t===void 0?void 0:t.redirectTo,i=(s=e.options)===null||s===void 0?void 0:s.captchaToken);const{data:a,error:o}=await _(this.fetch,"POST",`${this.url}/verify`,{headers:this.headers,body:Object.assign(Object.assign({},e),{gotrue_meta_security:{captcha_token:i}}),redirectTo:n,xform:D});if(o)throw o;if(!a)throw new Error("An error occurred on token verification.");const l=a.session,c=a.user;return l!=null&&l.access_token&&(await this._saveSession(l),await this._notifyAllSubscribers(e.type=="recovery"?"PASSWORD_RECOVERY":"SIGNED_IN",l)),this._returnResult({data:{user:c,session:l},error:null})}catch(n){if(y(n))return this._returnResult({data:{user:null,session:null},error:n});throw n}}async signInWithSSO(e){var t,s,n,i,a;try{let o=null,l=null;this.flowType==="pkce"&&([o,l]=await te(this.storage,this.storageKey));const c=await _(this.fetch,"POST",`${this.url}/sso`,{body:Object.assign(Object.assign(Object.assign(Object.assign(Object.assign({},"providerId"in e?{provider_id:e.providerId}:null),"domain"in e?{domain:e.domain}:null),{redirect_to:(s=(t=e.options)===null||t===void 0?void 0:t.redirectTo)!==null&&s!==void 0?s:void 0}),!((n=e==null?void 0:e.options)===null||n===void 0)&&n.captchaToken?{gotrue_meta_security:{captcha_token:e.options.captchaToken}}:null),{skip_http_redirect:!0,code_challenge:o,code_challenge_method:l}),headers:this.headers,xform:Us});return!((i=c.data)===null||i===void 0)&&i.url&&j()&&!(!((a=e.options)===null||a===void 0)&&a.skipBrowserRedirect)&&window.location.assign(c.data.url),this._returnResult(c)}catch(o){if(await P(this.storage,`${this.storageKey}-code-verifier`),y(o))return this._returnResult({data:null,error:o});throw o}}async reauthenticate(){return await this.initializePromise,await this._acquireLock(this.lockAcquireTimeout,async()=>await this._reauthenticate())}async _reauthenticate(){try{return await this._useSession(async e=>{const{data:{session:t},error:s}=e;if(s)throw s;if(!t)throw new U;const{error:n}=await _(this.fetch,"GET",`${this.url}/reauthenticate`,{headers:this.headers,jwt:t.access_token});return this._returnResult({data:{user:null,session:null},error:n})})}catch(e){if(y(e))return this._returnResult({data:{user:null,session:null},error:e});throw e}}async resend(e){try{const t=`${this.url}/resend`;if("email"in e){const{email:s,type:n,options:i}=e,{error:a}=await _(this.fetch,"POST",t,{headers:this.headers,body:{email:s,type:n,gotrue_meta_security:{captcha_token:i==null?void 0:i.captchaToken}},redirectTo:i==null?void 0:i.emailRedirectTo});return this._returnResult({data:{user:null,session:null},error:a})}else if("phone"in e){const{phone:s,type:n,options:i}=e,{data:a,error:o}=await _(this.fetch,"POST",t,{headers:this.headers,body:{phone:s,type:n,gotrue_meta_security:{captcha_token:i==null?void 0:i.captchaToken}}});return this._returnResult({data:{user:null,session:null,messageId:a==null?void 0:a.message_id},error:o})}throw new Ee("You must provide either an email or phone number and a type")}catch(t){if(y(t))return this._returnResult({data:{user:null,session:null},error:t});throw t}}async getSession(){return await this.initializePromise,await this._acquireLock(this.lockAcquireTimeout,async()=>this._useSession(async t=>t))}async _acquireLock(e,t){this._debug("#_acquireLock","begin",e);try{if(this.lockAcquired){const s=this.pendingInLock.length?this.pendingInLock[this.pendingInLock.length-1]:Promise.resolve(),n=(async()=>(await s,await t()))();return this.pendingInLock.push((async()=>{try{await n}catch{}})()),n}return await this.lock(`lock:${this.storageKey}`,e,async()=>{this._debug("#_acquireLock","lock acquired for storage key",this.storageKey);try{this.lockAcquired=!0;const s=t();for(this.pendingInLock.push((async()=>{try{await s}catch{}})()),await s;this.pendingInLock.length;){const n=[...this.pendingInLock];await Promise.all(n),this.pendingInLock.splice(0,n.length)}return await s}finally{this._debug("#_acquireLock","lock released for storage key",this.storageKey),this.lockAcquired=!1}})}finally{this._debug("#_acquireLock","end")}}async _useSession(e){this._debug("#_useSession","begin");try{const t=await this.__loadSession();return await e(t)}finally{this._debug("#_useSession","end")}}async __loadSession(){this._debug("#__loadSession()","begin"),this.lockAcquired||this._debug("#__loadSession()","used outside of an acquired lock!",new Error().stack);try{let e=null;const t=await G(this.storage,this.storageKey);if(this._debug("#getSession()","session from storage",t),t!==null&&(this._isValidSession(t)?e=t:(this._debug("#getSession()","session from storage is not valid"),await this._removeSession())),!e)return{data:{session:null},error:null};const s=e.expires_at?e.expires_at*1e3-Date.now()<xe:!1;if(this._debug("#__loadSession()",`session has${s?"":" not"} expired`,"expires_at",e.expires_at),!s){if(this.userStorage){const a=await G(this.userStorage,this.storageKey+"-user");a!=null&&a.user?e.user=a.user:e.user=Be()}if(this.storage.isServer&&e.user&&!e.user.__isUserNotAvailableProxy){const a={value:this.suppressGetSessionWarning};e.user=$s(e.user,a),a.value&&(this.suppressGetSessionWarning=!0)}return{data:{session:e},error:null}}const{data:n,error:i}=await this._callRefreshToken(e.refresh_token);return i?this._returnResult({data:{session:null},error:i}):this._returnResult({data:{session:n},error:null})}finally{this._debug("#__loadSession()","end")}}async getUser(e){if(e)return await this._getUser(e);await this.initializePromise;const t=await this._acquireLock(this.lockAcquireTimeout,async()=>await this._getUser());return t.data.user&&(this.suppressGetSessionWarning=!0),t}async _getUser(e){try{return e?await _(this.fetch,"GET",`${this.url}/user`,{headers:this.headers,jwt:e,xform:H}):await this._useSession(async t=>{var s,n,i;const{data:a,error:o}=t;if(o)throw o;return!(!((s=a.session)===null||s===void 0)&&s.access_token)&&!this.hasCustomAuthorizationHeader?{data:{user:null},error:new U}:await _(this.fetch,"GET",`${this.url}/user`,{headers:this.headers,jwt:(i=(n=a.session)===null||n===void 0?void 0:n.access_token)!==null&&i!==void 0?i:void 0,xform:H})})}catch(t){if(y(t))return ls(t)&&(await this._removeSession(),await P(this.storage,`${this.storageKey}-code-verifier`)),this._returnResult({data:{user:null},error:t});throw t}}async updateUser(e,t={}){return await this.initializePromise,await this._acquireLock(this.lockAcquireTimeout,async()=>await this._updateUser(e,t))}async _updateUser(e,t={}){try{return await this._useSession(async s=>{const{data:n,error:i}=s;if(i)throw i;if(!n.session)throw new U;const a=n.session;let o=null,l=null;this.flowType==="pkce"&&e.email!=null&&([o,l]=await te(this.storage,this.storageKey));const{data:c,error:u}=await _(this.fetch,"PUT",`${this.url}/user`,{headers:this.headers,redirectTo:t==null?void 0:t.emailRedirectTo,body:Object.assign(Object.assign({},e),{code_challenge:o,code_challenge_method:l}),jwt:a.access_token,xform:H});if(u)throw u;return a.user=c.user,await this._saveSession(a),await this._notifyAllSubscribers("USER_UPDATED",a),this._returnResult({data:{user:a.user},error:null})})}catch(s){if(await P(this.storage,`${this.storageKey}-code-verifier`),y(s))return this._returnResult({data:{user:null},error:s});throw s}}async setSession(e){return await this.initializePromise,await this._acquireLock(this.lockAcquireTimeout,async()=>await this._setSession(e))}async _setSession(e){try{if(!e.access_token||!e.refresh_token)throw new U;const t=Date.now()/1e3;let s=t,n=!0,i=null;const{payload:a}=Ne(e.access_token);if(a.exp&&(s=a.exp,n=s<=t),n){const{data:o,error:l}=await this._callRefreshToken(e.refresh_token);if(l)return this._returnResult({data:{user:null,session:null},error:l});if(!o)return{data:{user:null,session:null},error:null};i=o}else{const{data:o,error:l}=await this._getUser(e.access_token);if(l)throw l;i={access_token:e.access_token,refresh_token:e.refresh_token,user:o.user,token_type:"bearer",expires_in:s-t,expires_at:s},await this._saveSession(i),await this._notifyAllSubscribers("SIGNED_IN",i)}return this._returnResult({data:{user:i.user,session:i},error:null})}catch(t){if(y(t))return this._returnResult({data:{session:null,user:null},error:t});throw t}}async refreshSession(e){return await this.initializePromise,await this._acquireLock(this.lockAcquireTimeout,async()=>await this._refreshSession(e))}async _refreshSession(e){try{return await this._useSession(async t=>{var s;if(!e){const{data:a,error:o}=t;if(o)throw o;e=(s=a.session)!==null&&s!==void 0?s:void 0}if(!(e!=null&&e.refresh_token))throw new U;const{data:n,error:i}=await this._callRefreshToken(e.refresh_token);return i?this._returnResult({data:{user:null,session:null},error:i}):n?this._returnResult({data:{user:n.user,session:n},error:null}):this._returnResult({data:{user:null,session:null},error:null})})}catch(t){if(y(t))return this._returnResult({data:{user:null,session:null},error:t});throw t}}async _getSessionFromURL(e,t){try{if(!j())throw new Se("No browser detected.");if(e.error||e.error_description||e.error_code)throw new Se(e.error_description||"Error in URL with unspecified error_description",{error:e.error||"unspecified_error",code:e.error_code||"unspecified_code"});switch(t){case"implicit":if(this.flowType==="pkce")throw new gt("Not a valid PKCE flow url.");break;case"pkce":if(this.flowType==="implicit")throw new Se("Not a valid implicit grant flow url.");break;default:}if(t==="pkce"){if(this._debug("#_initialize()","begin","is PKCE flow",!0),!e.code)throw new gt("No code detected.");const{data:b,error:g}=await this._exchangeCodeForSession(e.code);if(g)throw g;const S=new URL(window.location.href);return S.searchParams.delete("code"),window.history.replaceState(window.history.state,"",S.toString()),{data:{session:b.session,redirectType:null},error:null}}const{provider_token:s,provider_refresh_token:n,access_token:i,refresh_token:a,expires_in:o,expires_at:l,token_type:c}=e;if(!i||!o||!a||!c)throw new Se("No session defined in URL");const u=Math.round(Date.now()/1e3),f=parseInt(o);let d=u+f;l&&(d=parseInt(l));const h=d-u;h*1e3<=ae&&console.warn(`@supabase/gotrue-js: Session as retrieved from URL expires in ${h}s, should have been closer to ${f}s`);const p=d-f;u-p>=120?console.warn("@supabase/gotrue-js: Session as retrieved from URL was issued over 120s ago, URL could be stale",p,d,u):u-p<0&&console.warn("@supabase/gotrue-js: Session as retrieved from URL was issued in the future? Check the device clock for skew",p,d,u);const{data:m,error:v}=await this._getUser(i);if(v)throw v;const w={provider_token:s,provider_refresh_token:n,access_token:i,expires_in:f,expires_at:d,refresh_token:a,token_type:c,user:m.user};return window.location.hash="",this._debug("#_getSessionFromURL()","clearing window.location.hash"),this._returnResult({data:{session:w,redirectType:e.type},error:null})}catch(s){if(y(s))return this._returnResult({data:{session:null,redirectType:null},error:s});throw s}}_isImplicitGrantCallback(e){return typeof this.detectSessionInUrl=="function"?this.detectSessionInUrl(new URL(window.location.href),e):!!(e.access_token||e.error_description)}async _isPKCECallback(e){const t=await G(this.storage,`${this.storageKey}-code-verifier`);return!!(e.code&&t)}async signOut(e={scope:"global"}){return await this.initializePromise,await this._acquireLock(this.lockAcquireTimeout,async()=>await this._signOut(e))}async _signOut({scope:e}={scope:"global"}){return await this._useSession(async t=>{var s;const{data:n,error:i}=t;if(i)return this._returnResult({error:i});const a=(s=n.session)===null||s===void 0?void 0:s.access_token;if(a){const{error:o}=await this.admin.signOut(a,e);if(o&&!(os(o)&&(o.status===404||o.status===401||o.status===403)))return this._returnResult({error:o})}return e!=="others"&&(await this._removeSession(),await P(this.storage,`${this.storageKey}-code-verifier`)),this._returnResult({error:null})})}onAuthStateChange(e){const t=vs(),s={id:t,callback:e,unsubscribe:()=>{this._debug("#unsubscribe()","state change callback with id removed",t),this.stateChangeEmitters.delete(t)}};return this._debug("#onAuthStateChange()","registered callback with id",t),this.stateChangeEmitters.set(t,s),(async()=>(await this.initializePromise,await this._acquireLock(this.lockAcquireTimeout,async()=>{this._emitInitialSession(t)})))(),{data:{subscription:s}}}async _emitInitialSession(e){return await this._useSession(async t=>{var s,n;try{const{data:{session:i},error:a}=t;if(a)throw a;await((s=this.stateChangeEmitters.get(e))===null||s===void 0?void 0:s.callback("INITIAL_SESSION",i)),this._debug("INITIAL_SESSION","callback id",e,"session",i)}catch(i){await((n=this.stateChangeEmitters.get(e))===null||n===void 0?void 0:n.callback("INITIAL_SESSION",null)),this._debug("INITIAL_SESSION","callback id",e,"error",i),console.error(i)}})}async resetPasswordForEmail(e,t={}){let s=null,n=null;this.flowType==="pkce"&&([s,n]=await te(this.storage,this.storageKey,!0));try{return await _(this.fetch,"POST",`${this.url}/recover`,{body:{email:e,code_challenge:s,code_challenge_method:n,gotrue_meta_security:{captcha_token:t.captchaToken}},headers:this.headers,redirectTo:t.redirectTo})}catch(i){if(await P(this.storage,`${this.storageKey}-code-verifier`),y(i))return this._returnResult({data:null,error:i});throw i}}async getUserIdentities(){var e;try{const{data:t,error:s}=await this.getUser();if(s)throw s;return this._returnResult({data:{identities:(e=t.user.identities)!==null&&e!==void 0?e:[]},error:null})}catch(t){if(y(t))return this._returnResult({data:null,error:t});throw t}}async linkIdentity(e){return"token"in e?this.linkIdentityIdToken(e):this.linkIdentityOAuth(e)}async linkIdentityOAuth(e){var t;try{const{data:s,error:n}=await this._useSession(async i=>{var a,o,l,c,u;const{data:f,error:d}=i;if(d)throw d;const h=await this._getUrlForProvider(`${this.url}/user/identities/authorize`,e.provider,{redirectTo:(a=e.options)===null||a===void 0?void 0:a.redirectTo,scopes:(o=e.options)===null||o===void 0?void 0:o.scopes,queryParams:(l=e.options)===null||l===void 0?void 0:l.queryParams,skipBrowserRedirect:!0});return await _(this.fetch,"GET",h,{headers:this.headers,jwt:(u=(c=f.session)===null||c===void 0?void 0:c.access_token)!==null&&u!==void 0?u:void 0})});if(n)throw n;return j()&&!(!((t=e.options)===null||t===void 0)&&t.skipBrowserRedirect)&&window.location.assign(s==null?void 0:s.url),this._returnResult({data:{provider:e.provider,url:s==null?void 0:s.url},error:null})}catch(s){if(y(s))return this._returnResult({data:{provider:e.provider,url:null},error:s});throw s}}async linkIdentityIdToken(e){return await this._useSession(async t=>{var s;try{const{error:n,data:{session:i}}=t;if(n)throw n;const{options:a,provider:o,token:l,access_token:c,nonce:u}=e,f=await _(this.fetch,"POST",`${this.url}/token?grant_type=id_token`,{headers:this.headers,jwt:(s=i==null?void 0:i.access_token)!==null&&s!==void 0?s:void 0,body:{provider:o,id_token:l,access_token:c,nonce:u,link_identity:!0,gotrue_meta_security:{captcha_token:a==null?void 0:a.captchaToken}},xform:D}),{data:d,error:h}=f;return h?this._returnResult({data:{user:null,session:null},error:h}):!d||!d.session||!d.user?this._returnResult({data:{user:null,session:null},error:new ee}):(d.session&&(await this._saveSession(d.session),await this._notifyAllSubscribers("USER_UPDATED",d.session)),this._returnResult({data:d,error:h}))}catch(n){if(await P(this.storage,`${this.storageKey}-code-verifier`),y(n))return this._returnResult({data:{user:null,session:null},error:n});throw n}})}async unlinkIdentity(e){try{return await this._useSession(async t=>{var s,n;const{data:i,error:a}=t;if(a)throw a;return await _(this.fetch,"DELETE",`${this.url}/user/identities/${e.identity_id}`,{headers:this.headers,jwt:(n=(s=i.session)===null||s===void 0?void 0:s.access_token)!==null&&n!==void 0?n:void 0})})}catch(t){if(y(t))return this._returnResult({data:null,error:t});throw t}}async _refreshAccessToken(e){const t=`#_refreshAccessToken(${e.substring(0,5)}...)`;this._debug(t,"begin");try{const s=Date.now();return await _s(async n=>(n>0&&await bs(200*Math.pow(2,n-1)),this._debug(t,"refreshing attempt",n),await _(this.fetch,"POST",`${this.url}/token?grant_type=refresh_token`,{body:{refresh_token:e},headers:this.headers,xform:D})),(n,i)=>{const a=200*Math.pow(2,n);return i&&Ue(i)&&Date.now()+a-s<ae})}catch(s){if(this._debug(t,"error",s),y(s))return this._returnResult({data:{session:null,user:null},error:s});throw s}finally{this._debug(t,"end")}}_isValidSession(e){return typeof e=="object"&&e!==null&&"access_token"in e&&"refresh_token"in e&&"expires_at"in e}async _handleProviderSignIn(e,t){const s=await this._getUrlForProvider(`${this.url}/authorize`,e,{redirectTo:t.redirectTo,scopes:t.scopes,queryParams:t.queryParams});return this._debug("#_handleProviderSignIn()","provider",e,"options",t,"url",s),j()&&!t.skipBrowserRedirect&&window.location.assign(s),{data:{provider:e,url:s},error:null}}async _recoverAndRefresh(){var e,t;const s="#_recoverAndRefresh()";this._debug(s,"begin");try{const n=await G(this.storage,this.storageKey);if(n&&this.userStorage){let a=await G(this.userStorage,this.storageKey+"-user");!this.storage.isServer&&Object.is(this.storage,this.userStorage)&&!a&&(a={user:n.user},await oe(this.userStorage,this.storageKey+"-user",a)),n.user=(e=a==null?void 0:a.user)!==null&&e!==void 0?e:Be()}else if(n&&!n.user&&!n.user){const a=await G(this.storage,this.storageKey+"-user");a&&(a!=null&&a.user)?(n.user=a.user,await P(this.storage,this.storageKey+"-user"),await oe(this.storage,this.storageKey,n)):n.user=Be()}if(this._debug(s,"session from storage",n),!this._isValidSession(n)){this._debug(s,"session is not valid"),n!==null&&await this._removeSession();return}const i=((t=n.expires_at)!==null&&t!==void 0?t:1/0)*1e3-Date.now()<xe;if(this._debug(s,`session has${i?"":" not"} expired with margin of ${xe}s`),i){if(this.autoRefreshToken&&n.refresh_token){const{error:a}=await this._callRefreshToken(n.refresh_token);a&&(console.error(a),Ue(a)||(this._debug(s,"refresh failed with a non-retryable error, removing the session",a),await this._removeSession()))}}else if(n.user&&n.user.__isUserNotAvailableProxy===!0)try{const{data:a,error:o}=await this._getUser(n.access_token);!o&&(a!=null&&a.user)?(n.user=a.user,await this._saveSession(n),await this._notifyAllSubscribers("SIGNED_IN",n)):this._debug(s,"could not get user data, skipping SIGNED_IN notification")}catch(a){console.error("Error getting user data:",a),this._debug(s,"error getting user data, skipping SIGNED_IN notification",a)}else await this._notifyAllSubscribers("SIGNED_IN",n)}catch(n){this._debug(s,"error",n),console.error(n);return}finally{this._debug(s,"end")}}async _callRefreshToken(e){var t,s;if(!e)throw new U;if(this.refreshingDeferred)return this.refreshingDeferred.promise;const n=`#_callRefreshToken(${e.substring(0,5)}...)`;this._debug(n,"begin");try{this.refreshingDeferred=new Ie;const{data:i,error:a}=await this._refreshAccessToken(e);if(a)throw a;if(!i.session)throw new U;await this._saveSession(i.session),await this._notifyAllSubscribers("TOKEN_REFRESHED",i.session);const o={data:i.session,error:null};return this.refreshingDeferred.resolve(o),o}catch(i){if(this._debug(n,"error",i),y(i)){const a={data:null,error:i};return Ue(i)||await this._removeSession(),(t=this.refreshingDeferred)===null||t===void 0||t.resolve(a),a}throw(s=this.refreshingDeferred)===null||s===void 0||s.reject(i),i}finally{this.refreshingDeferred=null,this._debug(n,"end")}}async _notifyAllSubscribers(e,t,s=!0){const n=`#_notifyAllSubscribers(${e})`;this._debug(n,"begin",t,`broadcast = ${s}`);try{this.broadcastChannel&&s&&this.broadcastChannel.postMessage({event:e,session:t});const i=[],a=Array.from(this.stateChangeEmitters.values()).map(async o=>{try{await o.callback(e,t)}catch(l){i.push(l)}});if(await Promise.all(a),i.length>0){for(let o=0;o<i.length;o+=1)console.error(i[o]);throw i[0]}}finally{this._debug(n,"end")}}async _saveSession(e){this._debug("#_saveSession()",e),this.suppressGetSessionWarning=!0,await P(this.storage,`${this.storageKey}-code-verifier`);const t=Object.assign({},e),s=t.user&&t.user.__isUserNotAvailableProxy===!0;if(this.userStorage){!s&&t.user&&await oe(this.userStorage,this.storageKey+"-user",{user:t.user});const n=Object.assign({},t);delete n.user;const i=_t(n);await oe(this.storage,this.storageKey,i)}else{const n=_t(t);await oe(this.storage,this.storageKey,n)}}async _removeSession(){this._debug("#_removeSession()"),this.suppressGetSessionWarning=!1,await P(this.storage,this.storageKey),await P(this.storage,this.storageKey+"-code-verifier"),await P(this.storage,this.storageKey+"-user"),this.userStorage&&await P(this.userStorage,this.storageKey+"-user"),await this._notifyAllSubscribers("SIGNED_OUT",null)}_removeVisibilityChangedCallback(){this._debug("#_removeVisibilityChangedCallback()");const e=this.visibilityChangedCallback;this.visibilityChangedCallback=null;try{e&&j()&&(window!=null&&window.removeEventListener)&&window.removeEventListener("visibilitychange",e)}catch(t){console.error("removing visibilitychange callback failed",t)}}async _startAutoRefresh(){await this._stopAutoRefresh(),this._debug("#_startAutoRefresh()");const e=setInterval(()=>this._autoRefreshTokenTick(),ae);this.autoRefreshTicker=e,e&&typeof e=="object"&&typeof e.unref=="function"?e.unref():typeof Deno<"u"&&typeof Deno.unrefTimer=="function"&&Deno.unrefTimer(e);const t=setTimeout(async()=>{await this.initializePromise,await this._autoRefreshTokenTick()},0);this.autoRefreshTickTimeout=t,t&&typeof t=="object"&&typeof t.unref=="function"?t.unref():typeof Deno<"u"&&typeof Deno.unrefTimer=="function"&&Deno.unrefTimer(t)}async _stopAutoRefresh(){this._debug("#_stopAutoRefresh()");const e=this.autoRefreshTicker;this.autoRefreshTicker=null,e&&clearInterval(e);const t=this.autoRefreshTickTimeout;this.autoRefreshTickTimeout=null,t&&clearTimeout(t)}async startAutoRefresh(){this._removeVisibilityChangedCallback(),await this._startAutoRefresh()}async stopAutoRefresh(){this._removeVisibilityChangedCallback(),await this._stopAutoRefresh()}async _autoRefreshTokenTick(){this._debug("#_autoRefreshTokenTick()","begin");try{await this._acquireLock(0,async()=>{try{const e=Date.now();try{return await this._useSession(async t=>{const{data:{session:s}}=t;if(!s||!s.refresh_token||!s.expires_at){this._debug("#_autoRefreshTokenTick()","no session");return}const n=Math.floor((s.expires_at*1e3-e)/ae);this._debug("#_autoRefreshTokenTick()",`access token expires in ${n} ticks, a tick lasts ${ae}ms, refresh threshold is ${He} ticks`),n<=He&&await this._callRefreshToken(s.refresh_token)})}catch(t){console.error("Auto refresh tick failed with error. This is likely a transient error.",t)}}finally{this._debug("#_autoRefreshTokenTick()","end")}})}catch(e){if(e.isAcquireTimeout||e instanceof Wt)this._debug("auto refresh token tick lock not available");else throw e}}async _handleVisibilityChange(){if(this._debug("#_handleVisibilityChange()"),!j()||!(window!=null&&window.addEventListener))return this.autoRefreshToken&&this.startAutoRefresh(),!1;try{this.visibilityChangedCallback=async()=>await this._onVisibilityChanged(!1),window==null||window.addEventListener("visibilitychange",this.visibilityChangedCallback),await this._onVisibilityChanged(!0)}catch(e){console.error("_handleVisibilityChange",e)}}async _onVisibilityChanged(e){const t=`#_onVisibilityChanged(${e})`;this._debug(t,"visibilityState",document.visibilityState),document.visibilityState==="visible"?(this.autoRefreshToken&&this._startAutoRefresh(),e||(await this.initializePromise,await this._acquireLock(this.lockAcquireTimeout,async()=>{if(document.visibilityState!=="visible"){this._debug(t,"acquired the lock to recover the session, but the browser visibilityState is no longer visible, aborting");return}await this._recoverAndRefresh()}))):document.visibilityState==="hidden"&&this.autoRefreshToken&&this._stopAutoRefresh()}async _getUrlForProvider(e,t,s){const n=[`provider=${encodeURIComponent(t)}`];if(s!=null&&s.redirectTo&&n.push(`redirect_to=${encodeURIComponent(s.redirectTo)}`),s!=null&&s.scopes&&n.push(`scopes=${encodeURIComponent(s.scopes)}`),this.flowType==="pkce"){const[i,a]=await te(this.storage,this.storageKey),o=new URLSearchParams({code_challenge:`${encodeURIComponent(i)}`,code_challenge_method:`${encodeURIComponent(a)}`});n.push(o.toString())}if(s!=null&&s.queryParams){const i=new URLSearchParams(s.queryParams);n.push(i.toString())}return s!=null&&s.skipBrowserRedirect&&n.push(`skip_http_redirect=${s.skipBrowserRedirect}`),`${e}?${n.join("&")}`}async _unenroll(e){try{return await this._useSession(async t=>{var s;const{data:n,error:i}=t;return i?this._returnResult({data:null,error:i}):await _(this.fetch,"DELETE",`${this.url}/factors/${e.factorId}`,{headers:this.headers,jwt:(s=n==null?void 0:n.session)===null||s===void 0?void 0:s.access_token})})}catch(t){if(y(t))return this._returnResult({data:null,error:t});throw t}}async _enroll(e){try{return await this._useSession(async t=>{var s,n;const{data:i,error:a}=t;if(a)return this._returnResult({data:null,error:a});const o=Object.assign({friendly_name:e.friendlyName,factor_type:e.factorType},e.factorType==="phone"?{phone:e.phone}:e.factorType==="totp"?{issuer:e.issuer}:{}),{data:l,error:c}=await _(this.fetch,"POST",`${this.url}/factors`,{body:o,headers:this.headers,jwt:(s=i==null?void 0:i.session)===null||s===void 0?void 0:s.access_token});return c?this._returnResult({data:null,error:c}):(e.factorType==="totp"&&l.type==="totp"&&(!((n=l==null?void 0:l.totp)===null||n===void 0)&&n.qr_code)&&(l.totp.qr_code=`data:image/svg+xml;utf-8,${l.totp.qr_code}`),this._returnResult({data:l,error:null}))})}catch(t){if(y(t))return this._returnResult({data:null,error:t});throw t}}async _verify(e){return this._acquireLock(this.lockAcquireTimeout,async()=>{try{return await this._useSession(async t=>{var s;const{data:n,error:i}=t;if(i)return this._returnResult({data:null,error:i});const a=Object.assign({challenge_id:e.challengeId},"webauthn"in e?{webauthn:Object.assign(Object.assign({},e.webauthn),{credential_response:e.webauthn.type==="create"?Xs(e.webauthn.credential_response):Qs(e.webauthn.credential_response)})}:{code:e.code}),{data:o,error:l}=await _(this.fetch,"POST",`${this.url}/factors/${e.factorId}/verify`,{body:a,headers:this.headers,jwt:(s=n==null?void 0:n.session)===null||s===void 0?void 0:s.access_token});return l?this._returnResult({data:null,error:l}):(await this._saveSession(Object.assign({expires_at:Math.round(Date.now()/1e3)+o.expires_in},o)),await this._notifyAllSubscribers("MFA_CHALLENGE_VERIFIED",o),this._returnResult({data:o,error:l}))})}catch(t){if(y(t))return this._returnResult({data:null,error:t});throw t}})}async _challenge(e){return this._acquireLock(this.lockAcquireTimeout,async()=>{try{return await this._useSession(async t=>{var s;const{data:n,error:i}=t;if(i)return this._returnResult({data:null,error:i});const a=await _(this.fetch,"POST",`${this.url}/factors/${e.factorId}/challenge`,{body:e,headers:this.headers,jwt:(s=n==null?void 0:n.session)===null||s===void 0?void 0:s.access_token});if(a.error)return a;const{data:o}=a;if(o.type!=="webauthn")return{data:o,error:null};switch(o.webauthn.type){case"create":return{data:Object.assign(Object.assign({},o),{webauthn:Object.assign(Object.assign({},o.webauthn),{credential_options:Object.assign(Object.assign({},o.webauthn.credential_options),{publicKey:zs(o.webauthn.credential_options.publicKey)})})}),error:null};case"request":return{data:Object.assign(Object.assign({},o),{webauthn:Object.assign(Object.assign({},o.webauthn),{credential_options:Object.assign(Object.assign({},o.webauthn.credential_options),{publicKey:Ys(o.webauthn.credential_options.publicKey)})})}),error:null}}})}catch(t){if(y(t))return this._returnResult({data:null,error:t});throw t}})}async _challengeAndVerify(e){const{data:t,error:s}=await this._challenge({factorId:e.factorId});return s?this._returnResult({data:null,error:s}):await this._verify({factorId:e.factorId,challengeId:t.id,code:e.code})}async _listFactors(){var e;const{data:{user:t},error:s}=await this.getUser();if(s)return{data:null,error:s};const n={all:[],phone:[],totp:[],webauthn:[]};for(const i of(e=t==null?void 0:t.factors)!==null&&e!==void 0?e:[])n.all.push(i),i.status==="verified"&&n[i.factor_type].push(i);return{data:n,error:null}}async _getAuthenticatorAssuranceLevel(){var e,t;const{data:{session:s},error:n}=await this.getSession();if(n)return this._returnResult({data:null,error:n});if(!s)return{data:{currentLevel:null,nextLevel:null,currentAuthenticationMethods:[]},error:null};const{payload:i}=Ne(s.access_token);let a=null;i.aal&&(a=i.aal);let o=a;((t=(e=s.user.factors)===null||e===void 0?void 0:e.filter(u=>u.status==="verified"))!==null&&t!==void 0?t:[]).length>0&&(o="aal2");const c=i.amr||[];return{data:{currentLevel:a,nextLevel:o,currentAuthenticationMethods:c},error:null}}async _getAuthorizationDetails(e){try{return await this._useSession(async t=>{const{data:{session:s},error:n}=t;return n?this._returnResult({data:null,error:n}):s?await _(this.fetch,"GET",`${this.url}/oauth/authorizations/${e}`,{headers:this.headers,jwt:s.access_token,xform:i=>({data:i,error:null})}):this._returnResult({data:null,error:new U})})}catch(t){if(y(t))return this._returnResult({data:null,error:t});throw t}}async _approveAuthorization(e,t){try{return await this._useSession(async s=>{const{data:{session:n},error:i}=s;if(i)return this._returnResult({data:null,error:i});if(!n)return this._returnResult({data:null,error:new U});const a=await _(this.fetch,"POST",`${this.url}/oauth/authorizations/${e}/consent`,{headers:this.headers,jwt:n.access_token,body:{action:"approve"},xform:o=>({data:o,error:null})});return a.data&&a.data.redirect_url&&j()&&!(t!=null&&t.skipBrowserRedirect)&&window.location.assign(a.data.redirect_url),a})}catch(s){if(y(s))return this._returnResult({data:null,error:s});throw s}}async _denyAuthorization(e,t){try{return await this._useSession(async s=>{const{data:{session:n},error:i}=s;if(i)return this._returnResult({data:null,error:i});if(!n)return this._returnResult({data:null,error:new U});const a=await _(this.fetch,"POST",`${this.url}/oauth/authorizations/${e}/consent`,{headers:this.headers,jwt:n.access_token,body:{action:"deny"},xform:o=>({data:o,error:null})});return a.data&&a.data.redirect_url&&j()&&!(t!=null&&t.skipBrowserRedirect)&&window.location.assign(a.data.redirect_url),a})}catch(s){if(y(s))return this._returnResult({data:null,error:s});throw s}}async _listOAuthGrants(){try{return await this._useSession(async e=>{const{data:{session:t},error:s}=e;return s?this._returnResult({data:null,error:s}):t?await _(this.fetch,"GET",`${this.url}/user/oauth/grants`,{headers:this.headers,jwt:t.access_token,xform:n=>({data:n,error:null})}):this._returnResult({data:null,error:new U})})}catch(e){if(y(e))return this._returnResult({data:null,error:e});throw e}}async _revokeOAuthGrant(e){try{return await this._useSession(async t=>{const{data:{session:s},error:n}=t;return n?this._returnResult({data:null,error:n}):s?(await _(this.fetch,"DELETE",`${this.url}/user/oauth/grants`,{headers:this.headers,jwt:s.access_token,query:{client_id:e.clientId},noResolveJson:!0}),{data:{},error:null}):this._returnResult({data:null,error:new U})})}catch(t){if(y(t))return this._returnResult({data:null,error:t});throw t}}async fetchJwk(e,t={keys:[]}){let s=t.keys.find(o=>o.kid===e);if(s)return s;const n=Date.now();if(s=this.jwks.keys.find(o=>o.kid===e),s&&this.jwks_cached_at+is>n)return s;const{data:i,error:a}=await _(this.fetch,"GET",`${this.url}/.well-known/jwks.json`,{headers:this.headers});if(a)throw a;return!i.keys||i.keys.length===0||(this.jwks=i,this.jwks_cached_at=n,s=i.keys.find(o=>o.kid===e),!s)?null:s}async getClaims(e,t={}){try{let s=e;if(!s){const{data:h,error:p}=await this.getSession();if(p||!h.session)return this._returnResult({data:null,error:p});s=h.session.access_token}const{header:n,payload:i,signature:a,raw:{header:o,payload:l}}=Ne(s);t!=null&&t.allowExpired||Rs(i.exp);const c=!n.alg||n.alg.startsWith("HS")||!n.kid||!("crypto"in globalThis&&"subtle"in globalThis.crypto)?null:await this.fetchJwk(n.kid,t!=null&&t.keys?{keys:t.keys}:t==null?void 0:t.jwks);if(!c){const{error:h}=await this.getUser(s);if(h)throw h;return{data:{claims:i,header:n,signature:a},error:null}}const u=Is(n.alg),f=await crypto.subtle.importKey("jwk",c,u,!0,["verify"]);if(!await crypto.subtle.verify(u,f,a,ms(`${o}.${l}`)))throw new ze("Invalid JWT signature");return{data:{claims:i,header:n,signature:a},error:null}}catch(s){if(y(s))return this._returnResult({data:null,error:s});throw s}}}ve.nextInstanceID={};const ln=ve,cn="2.90.1";let ue="";typeof Deno<"u"?ue="deno":typeof document<"u"?ue="web":typeof navigator<"u"&&navigator.product==="ReactNative"?ue="react-native":ue="node";const un={"X-Client-Info":`supabase-js-${ue}/${cn}`},dn={headers:un},hn={schema:"public"},fn={autoRefreshToken:!0,persistSession:!0,detectSessionInUrl:!0,flowType:"implicit"},pn={};function ye(r){"@babel/helpers - typeof";return ye=typeof Symbol=="function"&&typeof Symbol.iterator=="symbol"?function(e){return typeof e}:function(e){return e&&typeof Symbol=="function"&&e.constructor===Symbol&&e!==Symbol.prototype?"symbol":typeof e},ye(r)}function mn(r,e){if(ye(r)!="object"||!r)return r;var t=r[Symbol.toPrimitive];if(t!==void 0){var s=t.call(r,e);if(ye(s)!="object")return s;throw new TypeError("@@toPrimitive must return a primitive value.")}return(e==="string"?String:Number)(r)}function gn(r){var e=mn(r,"string");return ye(e)=="symbol"?e:e+""}function vn(r,e,t){return(e=gn(e))in r?Object.defineProperty(r,e,{value:t,enumerable:!0,configurable:!0,writable:!0}):r[e]=t,r}function Rt(r,e){var t=Object.keys(r);if(Object.getOwnPropertySymbols){var s=Object.getOwnPropertySymbols(r);e&&(s=s.filter(function(n){return Object.getOwnPropertyDescriptor(r,n).enumerable})),t.push.apply(t,s)}return t}function I(r){for(var e=1;e<arguments.length;e++){var t=arguments[e]!=null?arguments[e]:{};e%2?Rt(Object(t),!0).forEach(function(s){vn(r,s,t[s])}):Object.getOwnPropertyDescriptors?Object.defineProperties(r,Object.getOwnPropertyDescriptors(t)):Rt(Object(t)).forEach(function(s){Object.defineProperty(r,s,Object.getOwnPropertyDescriptor(t,s))})}return r}const yn=r=>r?(...e)=>r(...e):(...e)=>fetch(...e),wn=()=>Headers,bn=(r,e,t)=>{const s=yn(t),n=wn();return async(i,a)=>{var o;const l=(o=await e())!==null&&o!==void 0?o:r;let c=new n(a==null?void 0:a.headers);return c.has("apikey")||c.set("apikey",r),c.has("Authorization")||c.set("Authorization",`Bearer ${l}`),s(i,I(I({},a),{},{headers:c}))}};function _n(r){return r.endsWith("/")?r:r+"/"}function En(r,e){var t,s;const{db:n,auth:i,realtime:a,global:o}=r,{db:l,auth:c,realtime:u,global:f}=e,d={db:I(I({},l),n),auth:I(I({},c),i),realtime:I(I({},u),a),storage:{},global:I(I(I({},f),o),{},{headers:I(I({},(t=f==null?void 0:f.headers)!==null&&t!==void 0?t:{}),(s=o==null?void 0:o.headers)!==null&&s!==void 0?s:{})}),accessToken:async()=>""};return r.accessToken?d.accessToken=r.accessToken:delete d.accessToken,d}function Sn(r){const e=r==null?void 0:r.trim();if(!e)throw new Error("supabaseUrl is required.");if(!e.match(/^https?:\/\//i))throw new Error("Invalid supabaseUrl: Must be a valid HTTP or HTTPS URL.");try{return new URL(_n(e))}catch{throw Error("Invalid supabaseUrl: Provided URL is malformed.")}}var kn=class extends ln{constructor(r){super(r)}},Tn=class{constructor(r,e,t){var s,n;this.supabaseUrl=r,this.supabaseKey=e;const i=Sn(r);if(!e)throw new Error("supabaseKey is required.");this.realtimeUrl=new URL("realtime/v1",i),this.realtimeUrl.protocol=this.realtimeUrl.protocol.replace("http","ws"),this.authUrl=new URL("auth/v1",i),this.storageUrl=new URL("storage/v1",i),this.functionsUrl=new URL("functions/v1",i);const a=`sb-${i.hostname.split(".")[0]}-auth-token`,o={db:hn,realtime:pn,auth:I(I({},fn),{},{storageKey:a}),global:dn},l=En(t??{},o);if(this.storageKey=(s=l.auth.storageKey)!==null&&s!==void 0?s:"",this.headers=(n=l.global.headers)!==null&&n!==void 0?n:{},l.accessToken)this.accessToken=l.accessToken,this.auth=new Proxy({},{get:(u,f)=>{throw new Error(`@supabase/supabase-js: Supabase Client is configured with the accessToken option, accessing supabase.auth.${String(f)} is not possible`)}});else{var c;this.auth=this._initSupabaseAuthClient((c=l.auth)!==null&&c!==void 0?c:{},this.headers,l.global.fetch)}this.fetch=bn(e,this._getAccessToken.bind(this),l.global.fetch),this.realtime=this._initRealtimeClient(I({headers:this.headers,accessToken:this._getAccessToken.bind(this)},l.realtime)),this.accessToken&&this.accessToken().then(u=>this.realtime.setAuth(u)).catch(u=>console.warn("Failed to set initial Realtime auth token:",u)),this.rest=new sr(new URL("rest/v1",i).href,{headers:this.headers,schema:l.db.schema,fetch:this.fetch}),this.storage=new es(this.storageUrl.href,this.headers,this.fetch,t==null?void 0:t.storage),l.accessToken||this._listenForAuthEvents()}get functions(){return new Qt(this.functionsUrl.href,{headers:this.headers,customFetch:this.fetch})}from(r){return this.rest.from(r)}schema(r){return this.rest.schema(r)}rpc(r,e={},t={head:!1,get:!1,count:void 0}){return this.rest.rpc(r,e,t)}channel(r,e={config:{}}){return this.realtime.channel(r,e)}getChannels(){return this.realtime.getChannels()}removeChannel(r){return this.realtime.removeChannel(r)}removeAllChannels(){return this.realtime.removeAllChannels()}async _getAccessToken(){var r=this,e,t;if(r.accessToken)return await r.accessToken();const{data:s}=await r.auth.getSession();return(e=(t=s.session)===null||t===void 0?void 0:t.access_token)!==null&&e!==void 0?e:r.supabaseKey}_initSupabaseAuthClient({autoRefreshToken:r,persistSession:e,detectSessionInUrl:t,storage:s,userStorage:n,storageKey:i,flowType:a,lock:o,debug:l,throwOnError:c},u,f){const d={Authorization:`Bearer ${this.supabaseKey}`,apikey:`${this.supabaseKey}`};return new kn({url:this.authUrl.href,headers:I(I({},d),u),storageKey:i,autoRefreshToken:r,persistSession:e,detectSessionInUrl:t,storage:s,userStorage:n,flowType:a,lock:o,debug:l,throwOnError:c,fetch:f,hasCustomAuthorizationHeader:Object.keys(this.headers).some(h=>h.toLowerCase()==="authorization")})}_initRealtimeClient(r){return new br(this.realtimeUrl.href,I(I({},r),{},{params:I(I({},{apikey:this.supabaseKey}),r==null?void 0:r.params)}))}_listenForAuthEvents(){return this.auth.onAuthStateChange((r,e)=>{this._handleTokenChanged(r,"CLIENT",e==null?void 0:e.access_token)})}_handleTokenChanged(r,e,t){(r==="TOKEN_REFRESHED"||r==="SIGNED_IN")&&this.changedAccessToken!==t?(this.changedAccessToken=t,this.realtime.setAuth(t)):r==="SIGNED_OUT"&&(this.realtime.setAuth(),e=="STORAGE"&&this.auth.signOut(),this.changedAccessToken=void 0)}};const On=(r,e,t)=>new Tn(r,e,t);function An(){if(typeof window<"u")return!1;const r=globalThis.process;if(!r)return!1;const e=r.version;if(e==null)return!1;const t=e.match(/^v(\d+)\./);return t?parseInt(t[1],10)<=18:!1}An()&&console.warn("⚠️  Node.js 18 and below are deprecated and will no longer be supported in future versions of @supabase/supabase-js. Please upgrade to Node.js 20 or later. For more information, visit: https://github.com/orgs/supabase/discussions/37217");const Rn="https://rtqbijolslutowibirpf.supabase.co",In="eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InJ0cWJpam9sc2x1dG93aWJpcnBmIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NjgwMzI2MDMsImV4cCI6MjA4MzYwODYwM30.YjMrJFnem_Fjf9vvUmYNvPMSYdWBgDZxsYknf0tt4oI",k=On(Rn,In);async function Cn(r){r.innerHTML=`
    <div class="page-header">
      <h1><i class="fas fa-chart-line me-2"></i>Dashboard</h1>
      <p class="text-muted">Vue d'ensemble des statistiques</p>
    </div>

    <div class="row g-3 mb-4" id="stats-cards">
      <div class="col-md-6 col-lg-3">
        <div class="stat-card primary">
          <h3 id="total-customers">-</h3>
          <p><i class="fas fa-users me-2"></i>Total Clients</p>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="stat-card success">
          <h3 id="total-products">-</h3>
          <p><i class="fas fa-box me-2"></i>Total Produits</p>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="stat-card warning">
          <h3 id="total-orders">-</h3>
          <p><i class="fas fa-shopping-cart me-2"></i>Commandes</p>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="stat-card info">
          <h3 id="total-revenue">-</h3>
          <p><i class="fas fa-dollar-sign me-2"></i>Revenus</p>
        </div>
      </div>
    </div>

    <div class="row g-3 mb-4">
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Statut des Commandes</h5>
            <div class="chart-container">
              <canvas id="orderStatusChart"></canvas>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Répartition des Produits</h5>
            <div class="chart-container">
              <canvas id="productCategoryChart"></canvas>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="row g-3 mb-4">
      <div class="col-md-8">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Évolution des Commandes</h5>
            <div class="chart-container">
              <canvas id="ordersLineChart"></canvas>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Statut des Factures</h5>
            <div class="chart-container">
              <canvas id="invoiceStatusChart"></canvas>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="row g-3">
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Distribution du Stock</h5>
            <div class="chart-container">
              <canvas id="stockBarChart"></canvas>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <h5 class="card-title">Répartition des Rôles</h5>
            <div class="chart-container">
              <canvas id="userRoleChart"></canvas>
            </div>
          </div>
        </div>
      </div>
    </div>
  `,await $n()}async function $n(){try{const[r,e,t,s,n]=await Promise.all([k.from("customers").select("*",{count:"exact"}),k.from("products").select("*"),k.from("orders").select("*"),k.from("invoices").select("*"),k.from("users").select("*")]),i=r.data||[],a=e.data||[],o=t.data||[],l=s.data||[],c=n.data||[];document.getElementById("total-customers").textContent=i.length,document.getElementById("total-products").textContent=a.length,document.getElementById("total-orders").textContent=o.length;const u=o.reduce((f,d)=>f+parseFloat(d.total_amount||0),0);document.getElementById("total-revenue").textContent=`${u.toFixed(2)}€`,Pn(o),jn(a),xn(o),Un(l),Nn(a),Bn(c)}catch(r){console.error("Error loading dashboard data:",r)}}function Pn(r){const e=r.reduce((s,n)=>(s[n.status]=(s[n.status]||0)+1,s),{}),t=document.getElementById("orderStatusChart");new Chart(t,{type:"pie",data:{labels:Object.keys(e),datasets:[{data:Object.values(e),backgroundColor:["#667eea","#11998e","#f093fb","#fa709a"]}]},options:{responsive:!0,maintainAspectRatio:!1,plugins:{legend:{position:"bottom"}}}})}function jn(r){const e=r.reduce((s,n)=>(s[n.category]=(s[n.category]||0)+1,s),{}),t=document.getElementById("productCategoryChart");new Chart(t,{type:"doughnut",data:{labels:Object.keys(e),datasets:[{data:Object.values(e),backgroundColor:["#4facfe","#38ef7d","#f5576c","#fee140","#764ba2"]}]},options:{responsive:!0,maintainAspectRatio:!1,plugins:{legend:{position:"bottom"}}}})}function xn(r){const e=r.reduce((s,n)=>{const i=new Date(n.order_date).toLocaleDateString("fr-FR",{month:"short"});return s[i]=(s[i]||0)+1,s},{}),t=document.getElementById("ordersLineChart");new Chart(t,{type:"line",data:{labels:Object.keys(e),datasets:[{label:"Commandes",data:Object.values(e),borderColor:"#667eea",backgroundColor:"rgba(102, 126, 234, 0.1)",tension:.4,fill:!0}]},options:{responsive:!0,maintainAspectRatio:!1,plugins:{legend:{display:!1}},scales:{y:{beginAtZero:!0}}}})}function Un(r){const e=r.reduce((s,n)=>(s[n.status]=(s[n.status]||0)+1,s),{}),t=document.getElementById("invoiceStatusChart");new Chart(t,{type:"polarArea",data:{labels:Object.keys(e),datasets:[{data:Object.values(e),backgroundColor:["#667eea","#11998e","#f093fb","#fa709a"]}]},options:{responsive:!0,maintainAspectRatio:!1,plugins:{legend:{position:"bottom"}}}})}function Nn(r){const e=r.slice(0,5),t=document.getElementById("stockBarChart");new Chart(t,{type:"bar",data:{labels:e.map(s=>s.name),datasets:[{label:"Stock",data:e.map(s=>s.stock),backgroundColor:"#11998e",borderRadius:5}]},options:{responsive:!0,maintainAspectRatio:!1,plugins:{legend:{display:!1}},scales:{y:{beginAtZero:!0}}}})}function Bn(r){const e=r.reduce((s,n)=>(s[n.role]=(s[n.role]||0)+1,s),{}),t=document.getElementById("userRoleChart");new Chart(t,{type:"radar",data:{labels:Object.keys(e),datasets:[{label:"Utilisateurs",data:Object.values(e),backgroundColor:"rgba(102, 126, 234, 0.2)",borderColor:"#667eea",pointBackgroundColor:"#667eea"}]},options:{responsive:!0,maintainAspectRatio:!1,plugins:{legend:{display:!1}}}})}async function Dn(r){r.innerHTML=`
    <div class="page-header d-flex justify-content-between align-items-center">
      <div>
        <h1><i class="fas fa-users me-2"></i>Gestion des Clients</h1>
        <p class="text-muted">Liste complète des clients</p>
      </div>
      <button class="btn btn-primary" onclick="window.addCustomer()">
        <i class="fas fa-plus me-2"></i>Nouveau Client
      </button>
    </div>

    <div class="table-container">
      <div class="mb-3">
        <input type="text" class="form-control" id="searchCustomers" placeholder="Rechercher un client...">
      </div>
      <div class="table-responsive">
        <table class="table table-hover">
          <thead>
            <tr>
              <th>Nom</th>
              <th>Email</th>
              <th>Téléphone</th>
              <th>Adresse</th>
              <th>Date de création</th>
              <th>Actions</th>
            </tr>
          </thead>
          <tbody id="customers-table-body">
            <tr>
              <td colspan="6" class="text-center">
                <div class="loading-spinner">
                  <div class="spinner-border" role="status"></div>
                </div>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>

    <div class="modal fade" id="customerModal" tabindex="-1">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="customerModalTitle">Nouveau Client</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
          </div>
          <div class="modal-body">
            <form id="customerForm">
              <input type="hidden" id="customerId">
              <div class="mb-3">
                <label for="customerName" class="form-label">Nom</label>
                <input type="text" class="form-control" id="customerName" required>
              </div>
              <div class="mb-3">
                <label for="customerEmail" class="form-label">Email</label>
                <input type="email" class="form-control" id="customerEmail" required>
              </div>
              <div class="mb-3">
                <label for="customerPhone" class="form-label">Téléphone</label>
                <input type="tel" class="form-control" id="customerPhone">
              </div>
              <div class="mb-3">
                <label for="customerAddress" class="form-label">Adresse</label>
                <textarea class="form-control" id="customerAddress" rows="2"></textarea>
              </div>
            </form>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Annuler</button>
            <button type="button" class="btn btn-primary" onclick="window.saveCustomer()">Enregistrer</button>
          </div>
        </div>
      </div>
    </div>
  `,await tt(),Ln()}async function tt(){try{const{data:r,error:e}=await k.from("customers").select("*").order("created_at",{ascending:!1});if(e)throw e;const t=document.getElementById("customers-table-body");if(r.length===0){t.innerHTML=`
        <tr>
          <td colspan="6">
            <div class="empty-state">
              <i class="fas fa-users"></i>
              <p>Aucun client trouvé</p>
            </div>
          </td>
        </tr>
      `;return}t.innerHTML=r.map(s=>`
      <tr>
        <td>${s.name}</td>
        <td>${s.email}</td>
        <td>${s.phone||"-"}</td>
        <td>${s.address||"-"}</td>
        <td>${new Date(s.created_at).toLocaleDateString("fr-FR")}</td>
        <td>
          <div class="action-buttons">
            <button class="btn btn-sm btn-info" onclick="window.editCustomer('${s.id}')">
              <i class="fas fa-edit"></i>
            </button>
            <button class="btn btn-sm btn-danger" onclick="window.deleteCustomer('${s.id}')">
              <i class="fas fa-trash"></i>
            </button>
          </div>
        </td>
      </tr>
    `).join("")}catch(r){console.error("Error loading customers:",r)}}function Ln(){document.getElementById("searchCustomers").addEventListener("input",async r=>{const e=r.target.value.toLowerCase(),{data:t}=await k.from("customers").select("*").order("created_at",{ascending:!1}),s=t.filter(i=>i.name.toLowerCase().includes(e)||i.email.toLowerCase().includes(e)),n=document.getElementById("customers-table-body");n.innerHTML=s.map(i=>`
      <tr>
        <td>${i.name}</td>
        <td>${i.email}</td>
        <td>${i.phone||"-"}</td>
        <td>${i.address||"-"}</td>
        <td>${new Date(i.created_at).toLocaleDateString("fr-FR")}</td>
        <td>
          <div class="action-buttons">
            <button class="btn btn-sm btn-info" onclick="window.editCustomer('${i.id}')">
              <i class="fas fa-edit"></i>
            </button>
            <button class="btn btn-sm btn-danger" onclick="window.deleteCustomer('${i.id}')">
              <i class="fas fa-trash"></i>
            </button>
          </div>
        </td>
      </tr>
    `).join("")})}window.addCustomer=function(){document.getElementById("customerModalTitle").textContent="Nouveau Client",document.getElementById("customerForm").reset(),document.getElementById("customerId").value="",new bootstrap.Modal(document.getElementById("customerModal")).show()};window.editCustomer=async function(r){const{data:e}=await k.from("customers").select("*").eq("id",r).single();document.getElementById("customerModalTitle").textContent="Modifier Client",document.getElementById("customerId").value=e.id,document.getElementById("customerName").value=e.name,document.getElementById("customerEmail").value=e.email,document.getElementById("customerPhone").value=e.phone||"",document.getElementById("customerAddress").value=e.address||"",new bootstrap.Modal(document.getElementById("customerModal")).show()};window.saveCustomer=async function(){const r=document.getElementById("customerId").value,e={name:document.getElementById("customerName").value,email:document.getElementById("customerEmail").value,phone:document.getElementById("customerPhone").value,address:document.getElementById("customerAddress").value};try{r?await k.from("customers").update(e).eq("id",r):await k.from("customers").insert([e]),bootstrap.Modal.getInstance(document.getElementById("customerModal")).hide(),await tt()}catch(t){console.error("Error saving customer:",t),alert("Erreur lors de l'enregistrement")}};window.deleteCustomer=async function(r){if(confirm("Êtes-vous sûr de vouloir supprimer ce client ?"))try{await k.from("customers").delete().eq("id",r),await tt()}catch(e){console.error("Error deleting customer:",e),alert("Erreur lors de la suppression")}};async function qn(r){r.innerHTML=`
    <div class="page-header d-flex justify-content-between align-items-center">
      <div>
        <h1><i class="fas fa-box me-2"></i>Gestion des Produits</h1>
        <p class="text-muted">Catalogue de produits</p>
      </div>
      <button class="btn btn-primary" onclick="window.addProduct()">
        <i class="fas fa-plus me-2"></i>Nouveau Produit
      </button>
    </div>

    <div class="table-container">
      <div class="mb-3">
        <input type="text" class="form-control" id="searchProducts" placeholder="Rechercher un produit...">
      </div>
      <div class="table-responsive">
        <table class="table table-hover">
          <thead>
            <tr>
              <th>Nom</th>
              <th>Catégorie</th>
              <th>Prix</th>
              <th>Stock</th>
              <th>Description</th>
              <th>Actions</th>
            </tr>
          </thead>
          <tbody id="products-table-body"></tbody>
        </table>
      </div>
    </div>

    <div class="modal fade" id="productModal" tabindex="-1">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="productModalTitle">Nouveau Produit</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
          </div>
          <div class="modal-body">
            <form id="productForm">
              <input type="hidden" id="productId">
              <div class="mb-3">
                <label for="productName" class="form-label">Nom</label>
                <input type="text" class="form-control" id="productName" required>
              </div>
              <div class="mb-3">
                <label for="productCategory" class="form-label">Catégorie</label>
                <select class="form-select" id="productCategory">
                  <option value="Électronique">Électronique</option>
                  <option value="Vêtements">Vêtements</option>
                  <option value="Alimentation">Alimentation</option>
                  <option value="Mobilier">Mobilier</option>
                  <option value="Général">Général</option>
                </select>
              </div>
              <div class="mb-3">
                <label for="productPrice" class="form-label">Prix (€)</label>
                <input type="number" class="form-control" id="productPrice" step="0.01" required>
              </div>
              <div class="mb-3">
                <label for="productStock" class="form-label">Stock</label>
                <input type="number" class="form-control" id="productStock" required>
              </div>
              <div class="mb-3">
                <label for="productDescription" class="form-label">Description</label>
                <textarea class="form-control" id="productDescription" rows="3"></textarea>
              </div>
            </form>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Annuler</button>
            <button type="button" class="btn btn-primary" onclick="window.saveProduct()">Enregistrer</button>
          </div>
        </div>
      </div>
    </div>
  `,await rt(),Mn()}async function rt(){const{data:r}=await k.from("products").select("*").order("created_at",{ascending:!1}),e=document.getElementById("products-table-body");if(!r||r.length===0){e.innerHTML='<tr><td colspan="6"><div class="empty-state"><i class="fas fa-box"></i><p>Aucun produit trouvé</p></div></td></tr>';return}e.innerHTML=r.map(t=>`
    <tr>
      <td>${t.name}</td>
      <td><span class="badge bg-secondary">${t.category}</span></td>
      <td>${parseFloat(t.price).toFixed(2)}€</td>
      <td><span class="badge ${t.stock>10?"bg-success":"bg-warning"}">${t.stock}</span></td>
      <td>${t.description||"-"}</td>
      <td>
        <div class="action-buttons">
          <button class="btn btn-sm btn-info" onclick="window.editProduct('${t.id}')"><i class="fas fa-edit"></i></button>
          <button class="btn btn-sm btn-danger" onclick="window.deleteProduct('${t.id}')"><i class="fas fa-trash"></i></button>
        </div>
      </td>
    </tr>
  `).join("")}function Mn(){document.getElementById("searchProducts").addEventListener("input",async r=>{const e=r.target.value.toLowerCase(),{data:t}=await k.from("products").select("*"),s=t.filter(i=>i.name.toLowerCase().includes(e)||i.category.toLowerCase().includes(e)),n=document.getElementById("products-table-body");n.innerHTML=s.map(i=>`
      <tr>
        <td>${i.name}</td>
        <td><span class="badge bg-secondary">${i.category}</span></td>
        <td>${parseFloat(i.price).toFixed(2)}€</td>
        <td><span class="badge ${i.stock>10?"bg-success":"bg-warning"}">${i.stock}</span></td>
        <td>${i.description||"-"}</td>
        <td>
          <div class="action-buttons">
            <button class="btn btn-sm btn-info" onclick="window.editProduct('${i.id}')"><i class="fas fa-edit"></i></button>
            <button class="btn btn-sm btn-danger" onclick="window.deleteProduct('${i.id}')"><i class="fas fa-trash"></i></button>
          </div>
        </td>
      </tr>
    `).join("")})}window.addProduct=function(){document.getElementById("productModalTitle").textContent="Nouveau Produit",document.getElementById("productForm").reset(),document.getElementById("productId").value="",new bootstrap.Modal(document.getElementById("productModal")).show()};window.editProduct=async function(r){const{data:e}=await k.from("products").select("*").eq("id",r).single();document.getElementById("productModalTitle").textContent="Modifier Produit",document.getElementById("productId").value=e.id,document.getElementById("productName").value=e.name,document.getElementById("productCategory").value=e.category,document.getElementById("productPrice").value=e.price,document.getElementById("productStock").value=e.stock,document.getElementById("productDescription").value=e.description||"",new bootstrap.Modal(document.getElementById("productModal")).show()};window.saveProduct=async function(){const r=document.getElementById("productId").value,e={name:document.getElementById("productName").value,category:document.getElementById("productCategory").value,price:parseFloat(document.getElementById("productPrice").value),stock:parseInt(document.getElementById("productStock").value),description:document.getElementById("productDescription").value};try{r?await k.from("products").update(e).eq("id",r):await k.from("products").insert([e]),bootstrap.Modal.getInstance(document.getElementById("productModal")).hide(),await rt()}catch(t){console.error("Error saving product:",t)}};window.deleteProduct=async function(r){confirm("Supprimer ce produit ?")&&(await k.from("products").delete().eq("id",r),await rt())};async function Fn(r){r.innerHTML=`
    <div class="page-header d-flex justify-content-between align-items-center">
      <div>
        <h1><i class="fas fa-shopping-cart me-2"></i>Gestion des Commandes</h1>
        <p class="text-muted">Suivi des commandes</p>
      </div>
      <button class="btn btn-primary" onclick="window.addOrder()">
        <i class="fas fa-plus me-2"></i>Nouvelle Commande
      </button>
    </div>

    <div class="table-container">
      <div class="table-responsive">
        <table class="table table-hover">
          <thead>
            <tr>
              <th>Client</th>
              <th>Montant Total</th>
              <th>Statut</th>
              <th>Date de Commande</th>
              <th>Actions</th>
            </tr>
          </thead>
          <tbody id="orders-table-body"></tbody>
        </table>
      </div>
    </div>

    <div class="modal fade" id="orderModal" tabindex="-1">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="orderModalTitle">Nouvelle Commande</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
          </div>
          <div class="modal-body">
            <form id="orderForm">
              <input type="hidden" id="orderId">
              <div class="mb-3">
                <label for="orderCustomer" class="form-label">Client</label>
                <select class="form-select" id="orderCustomer" required></select>
              </div>
              <div class="mb-3">
                <label for="orderAmount" class="form-label">Montant Total (€)</label>
                <input type="number" class="form-control" id="orderAmount" step="0.01" required>
              </div>
              <div class="mb-3">
                <label for="orderStatus" class="form-label">Statut</label>
                <select class="form-select" id="orderStatus">
                  <option value="pending">En attente</option>
                  <option value="processing">En cours</option>
                  <option value="completed">Complété</option>
                  <option value="cancelled">Annulé</option>
                </select>
              </div>
            </form>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Annuler</button>
            <button type="button" class="btn btn-primary" onclick="window.saveOrder()">Enregistrer</button>
          </div>
        </div>
      </div>
    </div>
  `,await st()}async function st(){const{data:r}=await k.from("orders").select(`
    *,
    customers (name)
  `).order("order_date",{ascending:!1}),e=document.getElementById("orders-table-body");if(!r||r.length===0){e.innerHTML='<tr><td colspan="5"><div class="empty-state"><i class="fas fa-shopping-cart"></i><p>Aucune commande trouvée</p></div></td></tr>';return}e.innerHTML=r.map(t=>{var n;const s={pending:"warning",processing:"info",completed:"success",cancelled:"danger"};return`
      <tr>
        <td>${((n=t.customers)==null?void 0:n.name)||"Client inconnu"}</td>
        <td>${parseFloat(t.total_amount).toFixed(2)}€</td>
        <td><span class="badge bg-${s[t.status]}">${t.status}</span></td>
        <td>${new Date(t.order_date).toLocaleDateString("fr-FR")}</td>
        <td>
          <div class="action-buttons">
            <button class="btn btn-sm btn-info" onclick="window.editOrder('${t.id}')"><i class="fas fa-edit"></i></button>
            <button class="btn btn-sm btn-danger" onclick="window.deleteOrder('${t.id}')"><i class="fas fa-trash"></i></button>
          </div>
        </td>
      </tr>
    `}).join("")}async function Ht(){const{data:r}=await k.from("customers").select("*"),e=document.getElementById("orderCustomer");e.innerHTML='<option value="">Sélectionner un client</option>'+r.map(t=>`<option value="${t.id}">${t.name}</option>`).join("")}window.addOrder=async function(){await Ht(),document.getElementById("orderModalTitle").textContent="Nouvelle Commande",document.getElementById("orderForm").reset(),document.getElementById("orderId").value="",new bootstrap.Modal(document.getElementById("orderModal")).show()};window.editOrder=async function(r){await Ht();const{data:e}=await k.from("orders").select("*").eq("id",r).single();document.getElementById("orderModalTitle").textContent="Modifier Commande",document.getElementById("orderId").value=e.id,document.getElementById("orderCustomer").value=e.customer_id,document.getElementById("orderAmount").value=e.total_amount,document.getElementById("orderStatus").value=e.status,new bootstrap.Modal(document.getElementById("orderModal")).show()};window.saveOrder=async function(){const r=document.getElementById("orderId").value,e={customer_id:document.getElementById("orderCustomer").value,total_amount:parseFloat(document.getElementById("orderAmount").value),status:document.getElementById("orderStatus").value};try{r?await k.from("orders").update(e).eq("id",r):await k.from("orders").insert([e]),bootstrap.Modal.getInstance(document.getElementById("orderModal")).hide(),await st()}catch(t){console.error("Error saving order:",t)}};window.deleteOrder=async function(r){confirm("Supprimer cette commande ?")&&(await k.from("orders").delete().eq("id",r),await st())};async function Wn(r){r.innerHTML=`
    <div class="page-header d-flex justify-content-between align-items-center">
      <div>
        <h1><i class="fas fa-file-invoice me-2"></i>Gestion des Factures</h1>
        <p class="text-muted">Suivi des factures</p>
      </div>
      <button class="btn btn-primary" onclick="window.addInvoice()">
        <i class="fas fa-plus me-2"></i>Nouvelle Facture
      </button>
    </div>

    <div class="table-container">
      <div class="table-responsive">
        <table class="table table-hover">
          <thead>
            <tr>
              <th>Client</th>
              <th>Commande</th>
              <th>Montant</th>
              <th>Statut</th>
              <th>Date d'émission</th>
              <th>Date d'échéance</th>
              <th>Actions</th>
            </tr>
          </thead>
          <tbody id="invoices-table-body"></tbody>
        </table>
      </div>
    </div>

    <div class="modal fade" id="invoiceModal" tabindex="-1">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="invoiceModalTitle">Nouvelle Facture</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
          </div>
          <div class="modal-body">
            <form id="invoiceForm">
              <input type="hidden" id="invoiceId">
              <div class="mb-3">
                <label for="invoiceCustomer" class="form-label">Client</label>
                <select class="form-select" id="invoiceCustomer" required></select>
              </div>
              <div class="mb-3">
                <label for="invoiceOrder" class="form-label">Commande</label>
                <select class="form-select" id="invoiceOrder" required></select>
              </div>
              <div class="mb-3">
                <label for="invoiceAmount" class="form-label">Montant (€)</label>
                <input type="number" class="form-control" id="invoiceAmount" step="0.01" required>
              </div>
              <div class="mb-3">
                <label for="invoiceStatus" class="form-label">Statut</label>
                <select class="form-select" id="invoiceStatus">
                  <option value="draft">Brouillon</option>
                  <option value="sent">Envoyée</option>
                  <option value="paid">Payée</option>
                  <option value="overdue">En retard</option>
                </select>
              </div>
              <div class="mb-3">
                <label for="invoiceDueDate" class="form-label">Date d'échéance</label>
                <input type="date" class="form-control" id="invoiceDueDate" required>
              </div>
            </form>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Annuler</button>
            <button type="button" class="btn btn-primary" onclick="window.saveInvoice()">Enregistrer</button>
          </div>
        </div>
      </div>
    </div>
  `,await nt()}async function nt(){const{data:r}=await k.from("invoices").select(`
    *,
    customers (name),
    orders (id)
  `).order("issue_date",{ascending:!1}),e=document.getElementById("invoices-table-body");if(!r||r.length===0){e.innerHTML='<tr><td colspan="7"><div class="empty-state"><i class="fas fa-file-invoice"></i><p>Aucune facture trouvée</p></div></td></tr>';return}e.innerHTML=r.map(t=>{var n,i;const s={draft:"secondary",sent:"info",paid:"success",overdue:"danger"};return`
      <tr>
        <td>${((n=t.customers)==null?void 0:n.name)||"Client inconnu"}</td>
        <td>#${(i=t.orders)==null?void 0:i.id.slice(0,8)}</td>
        <td>${parseFloat(t.amount).toFixed(2)}€</td>
        <td><span class="badge bg-${s[t.status]}">${t.status}</span></td>
        <td>${new Date(t.issue_date).toLocaleDateString("fr-FR")}</td>
        <td>${new Date(t.due_date).toLocaleDateString("fr-FR")}</td>
        <td>
          <div class="action-buttons">
            <button class="btn btn-sm btn-info" onclick="window.editInvoice('${t.id}')"><i class="fas fa-edit"></i></button>
            <button class="btn btn-sm btn-danger" onclick="window.deleteInvoice('${t.id}')"><i class="fas fa-trash"></i></button>
          </div>
        </td>
      </tr>
    `}).join("")}async function Jt(){const[r,e]=await Promise.all([k.from("customers").select("*"),k.from("orders").select("*")]),t=document.getElementById("invoiceCustomer");t.innerHTML='<option value="">Sélectionner un client</option>'+r.data.map(n=>`<option value="${n.id}">${n.name}</option>`).join("");const s=document.getElementById("invoiceOrder");s.innerHTML='<option value="">Sélectionner une commande</option>'+e.data.map(n=>`<option value="${n.id}">Commande #${n.id.slice(0,8)}</option>`).join("")}window.addInvoice=async function(){await Jt(),document.getElementById("invoiceModalTitle").textContent="Nouvelle Facture",document.getElementById("invoiceForm").reset(),document.getElementById("invoiceId").value="",new Date().toISOString().split("T")[0];const r=new Date;r.setDate(r.getDate()+30),document.getElementById("invoiceDueDate").value=r.toISOString().split("T")[0],new bootstrap.Modal(document.getElementById("invoiceModal")).show()};window.editInvoice=async function(r){await Jt();const{data:e}=await k.from("invoices").select("*").eq("id",r).single();document.getElementById("invoiceModalTitle").textContent="Modifier Facture",document.getElementById("invoiceId").value=e.id,document.getElementById("invoiceCustomer").value=e.customer_id,document.getElementById("invoiceOrder").value=e.order_id,document.getElementById("invoiceAmount").value=e.amount,document.getElementById("invoiceStatus").value=e.status,document.getElementById("invoiceDueDate").value=new Date(e.due_date).toISOString().split("T")[0],new bootstrap.Modal(document.getElementById("invoiceModal")).show()};window.saveInvoice=async function(){const r=document.getElementById("invoiceId").value,e={customer_id:document.getElementById("invoiceCustomer").value,order_id:document.getElementById("invoiceOrder").value,amount:parseFloat(document.getElementById("invoiceAmount").value),status:document.getElementById("invoiceStatus").value,due_date:document.getElementById("invoiceDueDate").value};try{r?await k.from("invoices").update(e).eq("id",r):await k.from("invoices").insert([e]),bootstrap.Modal.getInstance(document.getElementById("invoiceModal")).hide(),await nt()}catch(t){console.error("Error saving invoice:",t)}};window.deleteInvoice=async function(r){confirm("Supprimer cette facture ?")&&(await k.from("invoices").delete().eq("id",r),await nt())};async function Kn(r){r.innerHTML=`
    <div class="page-header d-flex justify-content-between align-items-center">
      <div>
        <h1><i class="fas fa-user-shield me-2"></i>Gestion des Utilisateurs</h1>
        <p class="text-muted">Gestion des comptes utilisateurs</p>
      </div>
      <button class="btn btn-primary" onclick="window.addUser()">
        <i class="fas fa-plus me-2"></i>Nouvel Utilisateur
      </button>
    </div>

    <div class="table-container">
      <div class="table-responsive">
        <table class="table table-hover">
          <thead>
            <tr>
              <th>Nom d'utilisateur</th>
              <th>Email</th>
              <th>Rôle</th>
              <th>Statut</th>
              <th>Date de création</th>
              <th>Actions</th>
            </tr>
          </thead>
          <tbody id="users-table-body"></tbody>
        </table>
      </div>
    </div>

    <div class="modal fade" id="userModal" tabindex="-1">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="userModalTitle">Nouvel Utilisateur</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
          </div>
          <div class="modal-body">
            <form id="userForm">
              <input type="hidden" id="userId">
              <div class="mb-3">
                <label for="username" class="form-label">Nom d'utilisateur</label>
                <input type="text" class="form-control" id="username" required>
              </div>
              <div class="mb-3">
                <label for="userEmail" class="form-label">Email</label>
                <input type="email" class="form-control" id="userEmail" required>
              </div>
              <div class="mb-3">
                <label for="userRole" class="form-label">Rôle</label>
                <select class="form-select" id="userRole">
                  <option value="admin">Administrateur</option>
                  <option value="manager">Manager</option>
                  <option value="employee">Employé</option>
                </select>
              </div>
              <div class="mb-3">
                <label for="userStatus" class="form-label">Statut</label>
                <select class="form-select" id="userStatus">
                  <option value="active">Actif</option>
                  <option value="inactive">Inactif</option>
                </select>
              </div>
            </form>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Annuler</button>
            <button type="button" class="btn btn-primary" onclick="window.saveUser()">Enregistrer</button>
          </div>
        </div>
      </div>
    </div>
  `,await it()}async function it(){const{data:r}=await k.from("users").select("*").order("created_at",{ascending:!1}),e=document.getElementById("users-table-body");if(!r||r.length===0){e.innerHTML='<tr><td colspan="6"><div class="empty-state"><i class="fas fa-user-shield"></i><p>Aucun utilisateur trouvé</p></div></td></tr>';return}e.innerHTML=r.map(t=>{const s={admin:"danger",manager:"warning",employee:"info"},n={active:"success",inactive:"secondary"};return`
      <tr>
        <td>${t.username}</td>
        <td>${t.email}</td>
        <td><span class="badge bg-${s[t.role]}">${t.role}</span></td>
        <td><span class="badge bg-${n[t.status]}">${t.status}</span></td>
        <td>${new Date(t.created_at).toLocaleDateString("fr-FR")}</td>
        <td>
          <div class="action-buttons">
            <button class="btn btn-sm btn-info" onclick="window.editUser('${t.id}')"><i class="fas fa-edit"></i></button>
            <button class="btn btn-sm btn-danger" onclick="window.deleteUser('${t.id}')"><i class="fas fa-trash"></i></button>
          </div>
        </td>
      </tr>
    `}).join("")}window.addUser=function(){document.getElementById("userModalTitle").textContent="Nouvel Utilisateur",document.getElementById("userForm").reset(),document.getElementById("userId").value="",new bootstrap.Modal(document.getElementById("userModal")).show()};window.editUser=async function(r){const{data:e}=await k.from("users").select("*").eq("id",r).single();document.getElementById("userModalTitle").textContent="Modifier Utilisateur",document.getElementById("userId").value=e.id,document.getElementById("username").value=e.username,document.getElementById("userEmail").value=e.email,document.getElementById("userRole").value=e.role,document.getElementById("userStatus").value=e.status,new bootstrap.Modal(document.getElementById("userModal")).show()};window.saveUser=async function(){const r=document.getElementById("userId").value,e={username:document.getElementById("username").value,email:document.getElementById("userEmail").value,role:document.getElementById("userRole").value,status:document.getElementById("userStatus").value};try{r?await k.from("users").update(e).eq("id",r):await k.from("users").insert([e]),bootstrap.Modal.getInstance(document.getElementById("userModal")).hide(),await it()}catch(t){console.error("Error saving user:",t)}};window.deleteUser=async function(r){confirm("Supprimer cet utilisateur ?")&&(await k.from("users").delete().eq("id",r),await it())};const Vn=[{path:"/",component:Cn},{path:"/customers",component:Dn},{path:"/products",component:qn},{path:"/orders",component:Fn},{path:"/invoices",component:Wn},{path:"/users",component:Kn}];new Gt(Vn);

#invoices.js
import { supabase } from './supabase.js';

export async function renderInvoices(container) {
  container.innerHTML = `
    <div class="page-header d-flex justify-content-between align-items-center">
      <div>
        <h1><i class="fas fa-file-invoice me-2"></i>Gestion des Factures</h1>
        <p class="text-muted">Suivi des factures</p>
      </div>
      <button class="btn btn-primary" onclick="window.addInvoice()">
        <i class="fas fa-plus me-2"></i>Nouvelle Facture
      </button>
    </div>

    <div class="table-container">
      <div class="table-responsive">
        <table class="table table-hover">
          <thead>
            <tr>
              <th>Client</th>
              <th>Commande</th>
              <th>Montant</th>
              <th>Statut</th>
              <th>Date d'émission</th>
              <th>Date d'échéance</th>
              <th>Actions</th>
            </tr>
          </thead>
          <tbody id="invoices-table-body"></tbody>
        </table>
      </div>
    </div>

    <div class="modal fade" id="invoiceModal" tabindex="-1">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="invoiceModalTitle">Nouvelle Facture</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
          </div>
          <div class="modal-body">
            <form id="invoiceForm">
              <input type="hidden" id="invoiceId">
              <div class="mb-3">
                <label for="invoiceCustomer" class="form-label">Client</label>
                <select class="form-select" id="invoiceCustomer" required></select>
              </div>
              <div class="mb-3">
                <label for="invoiceOrder" class="form-label">Commande</label>
                <select class="form-select" id="invoiceOrder" required></select>
              </div>
              <div class="mb-3">
                <label for="invoiceAmount" class="form-label">Montant (€)</label>
                <input type="number" class="form-control" id="invoiceAmount" step="0.01" required>
              </div>
              <div class="mb-3">
                <label for="invoiceStatus" class="form-label">Statut</label>
                <select class="form-select" id="invoiceStatus">
                  <option value="draft">Brouillon</option>
                  <option value="sent">Envoyée</option>
                  <option value="paid">Payée</option>
                  <option value="overdue">En retard</option>
                </select>
              </div>
              <div class="mb-3">
                <label for="invoiceDueDate" class="form-label">Date d'échéance</label>
                <input type="date" class="form-control" id="invoiceDueDate" required>
              </div>
            </form>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Annuler</button>
            <button type="button" class="btn btn-primary" onclick="window.saveInvoice()">Enregistrer</button>
          </div>
        </div>
      </div>
    </div>
  `;

  await loadInvoices();
}

async function loadInvoices() {
  const { data: invoices } = await supabase.from('invoices').select(`
    *,
    customers (name),
    orders (id)
  `).order('issue_date', { ascending: false });

  const tbody = document.getElementById('invoices-table-body');

  if (!invoices || invoices.length === 0) {
    tbody.innerHTML = '<tr><td colspan="7"><div class="empty-state"><i class="fas fa-file-invoice"></i><p>Aucune facture trouvée</p></div></td></tr>';
    return;
  }

  tbody.innerHTML = invoices.map(invoice => {
    const statusColors = {
      draft: 'secondary',
      sent: 'info',
      paid: 'success',
      overdue: 'danger'
    };

    return `
      <tr>
        <td>${invoice.customers?.name || 'Client inconnu'}</td>
        <td>#${invoice.orders?.id.slice(0, 8)}</td>
        <td>${parseFloat(invoice.amount).toFixed(2)}€</td>
        <td><span class="badge bg-${statusColors[invoice.status]}">${invoice.status}</span></td>
        <td>${new Date(invoice.issue_date).toLocaleDateString('fr-FR')}</td>
        <td>${new Date(invoice.due_date).toLocaleDateString('fr-FR')}</td>
        <td>
          <div class="action-buttons">
            <button class="btn btn-sm btn-info" onclick="window.editInvoice('${invoice.id}')"><i class="fas fa-edit"></i></button>
            <button class="btn btn-sm btn-danger" onclick="window.deleteInvoice('${invoice.id}')"><i class="fas fa-trash"></i></button>
          </div>
        </td>
      </tr>
    `;
  }).join('');
}

async function loadInvoiceDropdowns() {
  const [customersRes, ordersRes] = await Promise.all([
    supabase.from('customers').select('*'),
    supabase.from('orders').select('*')
  ]);

  const customerSelect = document.getElementById('invoiceCustomer');
  customerSelect.innerHTML = '<option value="">Sélectionner un client</option>' +
    customersRes.data.map(c => `<option value="${c.id}">${c.name}</option>`).join('');

  const orderSelect = document.getElementById('invoiceOrder');
  orderSelect.innerHTML = '<option value="">Sélectionner une commande</option>' +
    ordersRes.data.map(o => `<option value="${o.id}">Commande #${o.id.slice(0, 8)}</option>`).join('');
}

window.addInvoice = async function () {
  await loadInvoiceDropdowns();
  document.getElementById('invoiceModalTitle').textContent = 'Nouvelle Facture';
  document.getElementById('invoiceForm').reset();
  document.getElementById('invoiceId').value = '';
  const today = new Date().toISOString().split('T')[0];
  const dueDate = new Date();
  dueDate.setDate(dueDate.getDate() + 30);
  document.getElementById('invoiceDueDate').value = dueDate.toISOString().split('T')[0];
  new bootstrap.Modal(document.getElementById('invoiceModal')).show();
};

window.editInvoice = async function (id) {
  await loadInvoiceDropdowns();
  const { data } = await supabase.from('invoices').select('*').eq('id', id).single();
  document.getElementById('invoiceModalTitle').textContent = 'Modifier Facture';
  document.getElementById('invoiceId').value = data.id;
  document.getElementById('invoiceCustomer').value = data.customer_id;
  document.getElementById('invoiceOrder').value = data.order_id;
  document.getElementById('invoiceAmount').value = data.amount;
  document.getElementById('invoiceStatus').value = data.status;
  document.getElementById('invoiceDueDate').value = new Date(data.due_date).toISOString().split('T')[0];
  new bootstrap.Modal(document.getElementById('invoiceModal')).show();
};

window.saveInvoice = async function () {
  const id = document.getElementById('invoiceId').value;
  const invoiceData = {
    customer_id: document.getElementById('invoiceCustomer').value,
    order_id: document.getElementById('invoiceOrder').value,
    amount: parseFloat(document.getElementById('invoiceAmount').value),
    status: document.getElementById('invoiceStatus').value,
    due_date: document.getElementById('invoiceDueDate').value
  };

  try {
    if (id) {
      await supabase.from('invoices').update(invoiceData).eq('id', id);
    } else {
      await supabase.from('invoices').insert([invoiceData]);
    }
    bootstrap.Modal.getInstance(document.getElementById('invoiceModal')).hide();
    await loadInvoices();
  } catch (error) {
    console.error('Error saving invoice:', error);
  }
};

window.deleteInvoice = async function (id) {
  if (confirm('Supprimer cette facture ?')) {
    await supabase.from('invoices').delete().eq('id', id);
    await loadInvoices();
  }
};
#main.js
import 'style.css';
import { Router } from './router.js';
import { renderDashboard } from './dashboard.js';
import { renderCustomers } from './customers.js';
import { renderProducts } from './products.js';
import { renderOrders } from './orders.js';
import { renderInvoices } from './invoices.js';
import { renderUsers } from './users.js';

const routes = [
  { path: '/', component: renderDashboard },
  { path: '/customers', component: renderCustomers },
  { path: '/products', component: renderProducts },
  { path: '/orders', component: renderOrders },
  { path: '/invoices', component: renderInvoices },
  { path: '/users', component: renderUsers }
];

new Router(routes);
#orders.js
import { supabase } from './supabase.js';

export async function renderOrders(container) {
  container.innerHTML = `
    <div class="page-header d-flex justify-content-between align-items-center">
      <div>
        <h1><i class="fas fa-shopping-cart me-2"></i>Gestion des Commandes</h1>
        <p class="text-muted">Suivi des commandes</p>
      </div>
      <button class="btn btn-primary" onclick="window.addOrder()">
        <i class="fas fa-plus me-2"></i>Nouvelle Commande
      </button>
    </div>

    <div class="table-container">
      <div class="table-responsive">
        <table class="table table-hover">
          <thead>
            <tr>
              <th>Client</th>
              <th>Montant Total</th>
              <th>Statut</th>
              <th>Date de Commande</th>
              <th>Actions</th>
            </tr>
          </thead>
          <tbody id="orders-table-body"></tbody>
        </table>
      </div>
    </div>

    <div class="modal fade" id="orderModal" tabindex="-1">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="orderModalTitle">Nouvelle Commande</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
          </div>
          <div class="modal-body">
            <form id="orderForm">
              <input type="hidden" id="orderId">
              <div class="mb-3">
                <label for="orderCustomer" class="form-label">Client</label>
                <select class="form-select" id="orderCustomer" required></select>
              </div>
              <div class="mb-3">
                <label for="orderAmount" class="form-label">Montant Total (€)</label>
                <input type="number" class="form-control" id="orderAmount" step="0.01" required>
              </div>
              <div class="mb-3">
                <label for="orderStatus" class="form-label">Statut</label>
                <select class="form-select" id="orderStatus">
                  <option value="pending">En attente</option>
                  <option value="processing">En cours</option>
                  <option value="completed">Complété</option>
                  <option value="cancelled">Annulé</option>
                </select>
              </div>
            </form>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Annuler</button>
            <button type="button" class="btn btn-primary" onclick="window.saveOrder()">Enregistrer</button>
          </div>
        </div>
      </div>
    </div>
  `;

  await loadOrders();
}

async function loadOrders() {
  const { data: orders } = await supabase.from('orders').select(`
    *,
    customers (name)
  `).order('order_date', { ascending: false });

  const tbody = document.getElementById('orders-table-body');

  if (!orders || orders.length === 0) {
    tbody.innerHTML = '<tr><td colspan="5"><div class="empty-state"><i class="fas fa-shopping-cart"></i><p>Aucune commande trouvée</p></div></td></tr>';
    return;
  }

  tbody.innerHTML = orders.map(order => {
    const statusColors = {
      pending: 'warning',
      processing: 'info',
      completed: 'success',
      cancelled: 'danger'
    };

    return `
      <tr>
        <td>${order.customers?.name || 'Client inconnu'}</td>
        <td>${parseFloat(order.total_amount).toFixed(2)}€</td>
        <td><span class="badge bg-${statusColors[order.status]}">${order.status}</span></td>
        <td>${new Date(order.order_date).toLocaleDateString('fr-FR')}</td>
        <td>
          <div class="action-buttons">
            <button class="btn btn-sm btn-info" onclick="window.editOrder('${order.id}')"><i class="fas fa-edit"></i></button>
            <button class="btn btn-sm btn-danger" onclick="window.deleteOrder('${order.id}')"><i class="fas fa-trash"></i></button>
          </div>
        </td>
      </tr>
    `;
  }).join('');
}

async function loadCustomersDropdown() {
  const { data: customers } = await supabase.from('customers').select('*');
  const select = document.getElementById('orderCustomer');
  select.innerHTML = '<option value="">Sélectionner un client</option>' +
    customers.map(c => `<option value="${c.id}">${c.name}</option>`).join('');
}

window.addOrder = async function () {
  await loadCustomersDropdown();
  document.getElementById('orderModalTitle').textContent = 'Nouvelle Commande';
  document.getElementById('orderForm').reset();
  document.getElementById('orderId').value = '';
  new bootstrap.Modal(document.getElementById('orderModal')).show();
};

window.editOrder = async function (id) {
  await loadCustomersDropdown();
  const { data } = await supabase.from('orders').select('*').eq('id', id).single();
  document.getElementById('orderModalTitle').textContent = 'Modifier Commande';
  document.getElementById('orderId').value = data.id;
  document.getElementById('orderCustomer').value = data.customer_id;
  document.getElementById('orderAmount').value = data.total_amount;
  document.getElementById('orderStatus').value = data.status;
  new bootstrap.Modal(document.getElementById('orderModal')).show();
};

window.saveOrder = async function () {
  const id = document.getElementById('orderId').value;
  const orderData = {
    customer_id: document.getElementById('orderCustomer').value,
    total_amount: parseFloat(document.getElementById('orderAmount').value),
    status: document.getElementById('orderStatus').value
  };

  try {
    if (id) {
      await supabase.from('orders').update(orderData).eq('id', id);
    } else {
      await supabase.from('orders').insert([orderData]);
    }
    bootstrap.Modal.getInstance(document.getElementById('orderModal')).hide();
    await loadOrders();
  } catch (error) {
    console.error('Error saving order:', error);
  }
};

window.deleteOrder = async function (id) {
  if (confirm('Supprimer cette commande ?')) {
    await supabase.from('orders').delete().eq('id', id);
    await loadOrders();
  }
};
#products.js
export class Router {
  constructor(routes) {
    this.routes = routes;
    this.currentRoute = null;

    window.addEventListener('hashchange', () => this.handleRoute());
    window.addEventListener('load', () => this.handleRoute());
  }

  handleRoute() {
    const hash = window.location.hash.slice(1) || '/';
    const route = this.routes.find(r => r.path === hash) || this.routes[0];

    this.updateActiveNavLink(hash);

    if (this.currentRoute !== route) {
      this.currentRoute = route;
      const content = document.getElementById('content');
      content.innerHTML = '';
      route.component(content);
    }
  }

  updateActiveNavLink(path) {
    const links = document.querySelectorAll('.sidebar .nav-link');
    links.forEach(link => {
      const href = link.getAttribute('href').slice(1);
      if (href === path) {
        link.classList.add('active');
      } else {
        link.classList.remove('active');
      }
    });
  }

  navigate(path) {
    window.location.hash = path;
  }
}
#seed-note.js
import dotenv from 'dotenv';
import { createClient } from './supabase-js';

dotenv.config();

const supabase = createClient(
  process.env.VITE_SUPABASE_URL,
  process.env.VITE_SUPABASE_ANON_KEY
);

async function seedDatabase() {
  console.log('Seeding database...');

  const customers = [
    { name: 'Jean Dupont', email: 'jean.dupont@email.com', phone: '0601020304', address: '12 Rue de la Paix, 75001 Paris' },
    { name: 'Marie Martin', email: 'marie.martin@email.com', phone: '0605060708', address: '45 Avenue des Champs, 69001 Lyon' },
    { name: 'Pierre Bernard', email: 'pierre.bernard@email.com', phone: '0609101112', address: '78 Boulevard Victor Hugo, 13001 Marseille' },
    { name: 'Sophie Dubois', email: 'sophie.dubois@email.com', phone: '0613141516', address: '23 Rue du Commerce, 31000 Toulouse' },
    { name: 'Luc Petit', email: 'luc.petit@email.com', phone: '0617181920', address: '56 Place de la République, 33000 Bordeaux' }
  ];

  const { data: insertedCustomers } = await supabase.from('customers').insert(customers).select();
  console.log('Customers inserted:', insertedCustomers?.length);

  const products = [
    { name: 'Ordinateur Portable HP', description: 'HP Pavilion 15.6" avec processeur Intel Core i5', price: 699.99, stock: 25, category: 'Électronique' },
    { name: 'Smartphone Samsung Galaxy', description: 'Samsung Galaxy S23 128GB', price: 899.99, stock: 40, category: 'Électronique' },
    { name: 'T-Shirt Coton Bio', description: 'T-shirt en coton biologique, plusieurs couleurs', price: 29.99, stock: 150, category: 'Vêtements' },
    { name: 'Jean Slim Fit', description: 'Jean slim fit en denim stretch', price: 79.99, stock: 80, category: 'Vêtements' },
    { name: 'Café Arabica Premium', description: 'Café en grains 100% Arabica 1kg', price: 19.99, stock: 200, category: 'Alimentation' },
    { name: 'Chocolat Noir 70%', description: 'Tablette de chocolat noir 70% cacao', price: 4.99, stock: 300, category: 'Alimentation' },
    { name: 'Bureau en Bois', description: 'Bureau moderne en bois de chêne', price: 349.99, stock: 15, category: 'Mobilier' },
    { name: 'Chaise Ergonomique', description: 'Chaise de bureau ergonomique avec support lombaire', price: 199.99, stock: 30, category: 'Mobilier' }
  ];

  const { data: insertedProducts } = await supabase.from('products').insert(products).select();
  console.log('Products inserted:', insertedProducts?.length);

  const users = [
    { username: 'admin', email: 'admin@mymanager.com', role: 'admin', status: 'active' },
    { username: 'manager1', email: 'manager1@mymanager.com', role: 'manager', status: 'active' },
    { username: 'manager2', email: 'manager2@mymanager.com', role: 'manager', status: 'active' },
    { username: 'employee1', email: 'employee1@mymanager.com', role: 'employee', status: 'active' },
    { username: 'employee2', email: 'employee2@mymanager.com', role: 'employee', status: 'active' },
    { username: 'employee3', email: 'employee3@mymanager.com', role: 'employee', status: 'inactive' }
  ];

  const { data: insertedUsers } = await supabase.from('users').insert(users).select();
  console.log('Users inserted:', insertedUsers?.length);

  if (insertedCustomers && insertedCustomers.length > 0) {
    const orders = [
      { customer_id: insertedCustomers[0].id, total_amount: 729.98, status: 'completed', order_date: new Date('2024-01-15') },
      { customer_id: insertedCustomers[1].id, total_amount: 899.99, status: 'completed', order_date: new Date('2024-01-20') },
      { customer_id: insertedCustomers[2].id, total_amount: 549.98, status: 'processing', order_date: new Date('2024-02-05') },
      { customer_id: insertedCustomers[3].id, total_amount: 109.98, status: 'pending', order_date: new Date('2024-02-10') },
      { customer_id: insertedCustomers[4].id, total_amount: 349.99, status: 'completed', order_date: new Date('2024-02-15') },
      { customer_id: insertedCustomers[0].id, total_amount: 199.99, status: 'cancelled', order_date: new Date('2024-02-20') }
    ];

    const { data: insertedOrders } = await supabase.from('orders').insert(orders).select();
    console.log('Orders inserted:', insertedOrders?.length);

    if (insertedOrders && insertedOrders.length > 0) {
      const invoices = [
        {
          order_id: insertedOrders[0].id,
          customer_id: insertedCustomers[0].id,
          amount: 729.98,
          status: 'paid',
          issue_date: new Date('2024-01-15'),
          due_date: new Date('2024-02-15')
        },
        {
          order_id: insertedOrders[1].id,
          customer_id: insertedCustomers[1].id,
          amount: 899.99,
          status: 'paid',
          issue_date: new Date('2024-01-20'),
          due_date: new Date('2024-02-20')
        },
        {
          order_id: insertedOrders[2].id,
          customer_id: insertedCustomers[2].id,
          amount: 549.98,
          status: 'sent',
          issue_date: new Date('2024-02-05'),
          due_date: new Date('2024-03-05')
        },
        {
          order_id: insertedOrders[3].id,
          customer_id: insertedCustomers[3].id,
          amount: 109.98,
          status: 'draft',
          issue_date: new Date('2024-02-10'),
          due_date: new Date('2024-03-10')
        },
        {
          order_id: insertedOrders[4].id,
          customer_id: insertedCustomers[4].id,
          amount: 349.99,
          status: 'paid',
          issue_date: new Date('2024-02-15'),
          due_date: new Date('2024-03-15')
        }
      ];

      const { data: insertedInvoices } = await supabase.from('invoices').insert(invoices).select();
      console.log('Invoices inserted:', insertedInvoices?.length);
    }
  }

  console.log('Database seeding completed!');
  process.exit(0);
}

seedDatabase().catch(err => {
  console.error('Error seeding database:', err);
  process.exit(1);
});
#seed.js
import { supabase } from './supabase.js';

async function seedDatabase() {
  console.log('Seeding database...');

  const customers = [
    { name: 'Jean Dupont', email: 'jean.dupont@email.com', phone: '0601020304', address: '12 Rue de la Paix, 75001 Paris' },
    { name: 'Marie Martin', email: 'marie.martin@email.com', phone: '0605060708', address: '45 Avenue des Champs, 69001 Lyon' },
    { name: 'Pierre Bernard', email: 'pierre.bernard@email.com', phone: '0609101112', address: '78 Boulevard Victor Hugo, 13001 Marseille' },
    { name: 'Sophie Dubois', email: 'sophie.dubois@email.com', phone: '0613141516', address: '23 Rue du Commerce, 31000 Toulouse' },
    { name: 'Luc Petit', email: 'luc.petit@email.com', phone: '0617181920', address: '56 Place de la République, 33000 Bordeaux' }
  ];

  const { data: insertedCustomers } = await supabase.from('customers').insert(customers).select();
  console.log('Customers inserted:', insertedCustomers?.length);

  const products = [
    { name: 'Ordinateur Portable HP', description: 'HP Pavilion 15.6" avec processeur Intel Core i5', price: 699.99, stock: 25, category: 'Électronique' },
    { name: 'Smartphone Samsung Galaxy', description: 'Samsung Galaxy S23 128GB', price: 899.99, stock: 40, category: 'Électronique' },
    { name: 'T-Shirt Coton Bio', description: 'T-shirt en coton biologique, plusieurs couleurs', price: 29.99, stock: 150, category: 'Vêtements' },
    { name: 'Jean Slim Fit', description: 'Jean slim fit en denim stretch', price: 79.99, stock: 80, category: 'Vêtements' },
    { name: 'Café Arabica Premium', description: 'Café en grains 100% Arabica 1kg', price: 19.99, stock: 200, category: 'Alimentation' },
    { name: 'Chocolat Noir 70%', description: 'Tablette de chocolat noir 70% cacao', price: 4.99, stock: 300, category: 'Alimentation' },
    { name: 'Bureau en Bois', description: 'Bureau moderne en bois de chêne', price: 349.99, stock: 15, category: 'Mobilier' },
    { name: 'Chaise Ergonomique', description: 'Chaise de bureau ergonomique avec support lombaire', price: 199.99, stock: 30, category: 'Mobilier' }
  ];

  const { data: insertedProducts } = await supabase.from('products').insert(products).select();
  console.log('Products inserted:', insertedProducts?.length);

  const users = [
    { username: 'admin', email: 'admin@mymanager.com', role: 'admin', status: 'active' },
    { username: 'manager1', email: 'manager1@mymanager.com', role: 'manager', status: 'active' },
    { username: 'manager2', email: 'manager2@mymanager.com', role: 'manager', status: 'active' },
    { username: 'employee1', email: 'employee1@mymanager.com', role: 'employee', status: 'active' },
    { username: 'employee2', email: 'employee2@mymanager.com', role: 'employee', status: 'active' },
    { username: 'employee3', email: 'employee3@mymanager.com', role: 'employee', status: 'inactive' }
  ];

  const { data: insertedUsers } = await supabase.from('users').insert(users).select();
  console.log('Users inserted:', insertedUsers?.length);

  if (insertedCustomers && insertedCustomers.length > 0) {
    const orders = [
      { customer_id: insertedCustomers[0].id, total_amount: 729.98, status: 'completed', order_date: new Date('2024-01-15') },
      { customer_id: insertedCustomers[1].id, total_amount: 899.99, status: 'completed', order_date: new Date('2024-01-20') },
      { customer_id: insertedCustomers[2].id, total_amount: 549.98, status: 'processing', order_date: new Date('2024-02-05') },
      { customer_id: insertedCustomers[3].id, total_amount: 109.98, status: 'pending', order_date: new Date('2024-02-10') },
      { customer_id: insertedCustomers[4].id, total_amount: 349.99, status: 'completed', order_date: new Date('2024-02-15') },
      { customer_id: insertedCustomers[0].id, total_amount: 199.99, status: 'cancelled', order_date: new Date('2024-02-20') }
    ];

    const { data: insertedOrders } = await supabase.from('orders').insert(orders).select();
    console.log('Orders inserted:', insertedOrders?.length);

    if (insertedOrders && insertedOrders.length > 0) {
      const invoices = [
        {
          order_id: insertedOrders[0].id,
          customer_id: insertedCustomers[0].id,
          amount: 729.98,
          status: 'paid',
          issue_date: new Date('2024-01-15'),
          due_date: new Date('2024-02-15')
        },
        {
          order_id: insertedOrders[1].id,
          customer_id: insertedCustomers[1].id,
          amount: 899.99,
          status: 'paid',
          issue_date: new Date('2024-01-20'),
          due_date: new Date('2024-02-20')
        },
        {
          order_id: insertedOrders[2].id,
          customer_id: insertedCustomers[2].id,
          amount: 549.98,
          status: 'sent',
          issue_date: new Date('2024-02-05'),
          due_date: new Date('2024-03-05')
        },
        {
          order_id: insertedOrders[3].id,
          customer_id: insertedCustomers[3].id,
          amount: 109.98,
          status: 'draft',
          issue_date: new Date('2024-02-10'),
          due_date: new Date('2024-03-10')
        },
        {
          order_id: insertedOrders[4].id,
          customer_id: insertedCustomers[4].id,
          amount: 349.99,
          status: 'paid',
          issue_date: new Date('2024-02-15'),
          due_date: new Date('2024-03-15')
        }
      ];

      const { data: insertedInvoices } = await supabase.from('invoices').insert(invoices).select();
      console.log('Invoices inserted:', insertedInvoices?.length);
    }
  }

  console.log('Database seeding completed!');
}

seedDatabase().catch(console.error);
#supabase.js
import { createClient } from './supabase-js';

const supabaseUrl = import.meta.env.VITE_SUPABASE_URL;
const supabaseAnonKey = import.meta.env.VITE_SUPABASE_ANON_KEY;

export const supabase = createClient(supabaseUrl, supabaseAnonKey);
#users.js
import { supabase } from './supabase.js';

export async function renderUsers(container) {
  container.innerHTML = `
    <div class="page-header d-flex justify-content-between align-items-center">
      <div>
        <h1><i class="fas fa-user-shield me-2"></i>Gestion des Utilisateurs</h1>
        <p class="text-muted">Gestion des comptes utilisateurs</p>
      </div>
      <button class="btn btn-primary" onclick="window.addUser()">
        <i class="fas fa-plus me-2"></i>Nouvel Utilisateur
      </button>
    </div>

    <div class="table-container">
      <div class="table-responsive">
        <table class="table table-hover">
          <thead>
            <tr>
              <th>Nom d'utilisateur</th>
              <th>Email</th>
              <th>Rôle</th>
              <th>Statut</th>
              <th>Date de création</th>
              <th>Actions</th>
            </tr>
          </thead>
          <tbody id="users-table-body"></tbody>
        </table>
      </div>
    </div>

    <div class="modal fade" id="userModal" tabindex="-1">
      <div class="modal-dialog">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="userModalTitle">Nouvel Utilisateur</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
          </div>
          <div class="modal-body">
            <form id="userForm">
              <input type="hidden" id="userId">
              <div class="mb-3">
                <label for="username" class="form-label">Nom d'utilisateur</label>
                <input type="text" class="form-control" id="username" required>
              </div>
              <div class="mb-3">
                <label for="userEmail" class="form-label">Email</label>
                <input type="email" class="form-control" id="userEmail" required>
              </div>
              <div class="mb-3">
                <label for="userRole" class="form-label">Rôle</label>
                <select class="form-select" id="userRole">
                  <option value="admin">Administrateur</option>
                  <option value="manager">Manager</option>
                  <option value="employee">Employé</option>
                </select>
              </div>
              <div class="mb-3">
                <label for="userStatus" class="form-label">Statut</label>
                <select class="form-select" id="userStatus">
                  <option value="active">Actif</option>
                  <option value="inactive">Inactif</option>
                </select>
              </div>
            </form>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Annuler</button>
            <button type="button" class="btn btn-primary" onclick="window.saveUser()">Enregistrer</button>
          </div>
        </div>
      </div>
    </div>
  `;

  await loadUsers();
}

async function loadUsers() {
  const { data: users } = await supabase.from('users').select('*').order('created_at', { ascending: false });
  const tbody = document.getElementById('users-table-body');

  if (!users || users.length === 0) {
    tbody.innerHTML = '<tr><td colspan="6"><div class="empty-state"><i class="fas fa-user-shield"></i><p>Aucun utilisateur trouvé</p></div></td></tr>';
    return;
  }

  tbody.innerHTML = users.map(user => {
    const roleColors = {
      admin: 'danger',
      manager: 'warning',
      employee: 'info'
    };

    const statusColors = {
      active: 'success',
      inactive: 'secondary'
    };

    return `
      <tr>
        <td>${user.username}</td>
        <td>${user.email}</td>
        <td><span class="badge bg-${roleColors[user.role]}">${user.role}</span></td>
        <td><span class="badge bg-${statusColors[user.status]}">${user.status}</span></td>
        <td>${new Date(user.created_at).toLocaleDateString('fr-FR')}</td>
        <td>
          <div class="action-buttons">
            <button class="btn btn-sm btn-info" onclick="window.editUser('${user.id}')"><i class="fas fa-edit"></i></button>
            <button class="btn btn-sm btn-danger" onclick="window.deleteUser('${user.id}')"><i class="fas fa-trash"></i></button>
          </div>
        </td>
      </tr>
    `;
  }).join('');
}

window.addUser = function () {
  document.getElementById('userModalTitle').textContent = 'Nouvel Utilisateur';
  document.getElementById('userForm').reset();
  document.getElementById('userId').value = '';
  new bootstrap.Modal(document.getElementById('userModal')).show();
};

window.editUser = async function (id) {
  const { data } = await supabase.from('users').select('*').eq('id', id).single();
  document.getElementById('userModalTitle').textContent = 'Modifier Utilisateur';
  document.getElementById('userId').value = data.id;
  document.getElementById('username').value = data.username;
  document.getElementById('userEmail').value = data.email;
  document.getElementById('userRole').value = data.role;
  document.getElementById('userStatus').value = data.status;
  new bootstrap.Modal(document.getElementById('userModal')).show();
};

window.saveUser = async function () {
  const id = document.getElementById('userId').value;
  const userData = {
    username: document.getElementById('username').value,
    email: document.getElementById('userEmail').value,
    role: document.getElementById('userRole').value,
    status: document.getElementById('userStatus').value
  };

  try {
    if (id) {
      await supabase.from('users').update(userData).eq('id', id);
    } else {
      await supabase.from('users').insert([userData]);
    }
    bootstrap.Modal.getInstance(document.getElementById('userModal')).hide();
    await loadUsers();
  } catch (error) {
    console.error('Error saving user:', error);
  }
};

window.deleteUser = async function (id) {
  if (confirm('Supprimer cet utilisateur ?')) {
    await supabase.from('users').delete().eq('id', id);
    await loadUsers();
  }
};


