<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Surya Global School Lost and Found Portal</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: #f4f7fb;
      color: #222;
    }

    .hidden {
      display: none !important;
    }

    header {
      background: linear-gradient(135deg, #1d4ed8, #4338ca);
      color: white;
      padding: 25px 20px;
      text-align: center;
    }

    header img {
      width: 120px;
      margin-bottom: 10px;
    }

    header h1 {
      font-size: 32px;
      margin-bottom: 8px;
    }

    header p {
      font-size: 15px;
      max-width: 800px;
      margin: auto;
      line-height: 1.5;
    }

    .container {
      width: 90%;
      max-width: 1250px;
      margin: 25px auto;
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 20px;
    }

    .card {
      background: white;
      border-radius: 16px;
      padding: 20px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.08);
    }

    .card h2 {
      margin-bottom: 15px;
      color: #1d4ed8;
      font-size: 24px;
    }

    .form-group {
      margin-bottom: 15px;
    }

    .form-group label {
      display: block;
      margin-bottom: 6px;
      font-weight: bold;
      font-size: 14px;
    }

    .form-group input,
    .form-group textarea,
    .form-group select {
      width: 100%;
      padding: 10px 12px;
      border: 1px solid #cbd5e1;
      border-radius: 10px;
      font-size: 14px;
      outline: none;
    }

    .form-group textarea {
      resize: vertical;
      min-height: 90px;
    }

    .btn {
      width: 100%;
      background: #1d4ed8;
      color: white;
      border: none;
      padding: 12px;
      border-radius: 10px;
      font-size: 15px;
      cursor: pointer;
      transition: 0.3s;
    }

    .btn:hover {
      background: #163fb0;
    }

    .btn-danger {
      background: #dc2626;
    }

    .btn-danger:hover {
      background: #b91c1c;
    }

    .top-bar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      margin-bottom: 20px;
      flex-wrap: wrap;
    }

    .top-bar-right {
      display: flex;
      gap: 10px;
      align-items: center;
      flex-wrap: wrap;
    }

    .search-box {
      margin-bottom: 20px;
      display: flex;
      gap: 10px;
    }

    .search-box input,
    .search-box select {
      flex: 1;
      padding: 12px;
      border: 1px solid #cbd5e1;
      border-radius: 10px;
      font-size: 14px;
    }

    .items-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 18px;
    }

    .item-card {
      background: #fff;
      border-radius: 14px;
      overflow: hidden;
      box-shadow: 0 6px 16px rgba(0,0,0,0.08);
      transition: transform 0.3s;
    }

    .item-card:hover {
      transform: translateY(-4px);
    }

    .item-card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
      background: #e5e7eb;
    }

    .item-content {
      padding: 15px;
    }

    .item-content h3 {
      color: #111827;
      margin-bottom: 8px;
      font-size: 20px;
    }

    .item-content p {
      font-size: 14px;
      margin-bottom: 6px;
      color: #374151;
      line-height: 1.4;
    }

    .badge {
      display: inline-block;
      padding: 6px 10px;
      border-radius: 20px;
      font-size: 12px;
      font-weight: bold;
      margin-top: 8px;
      margin-right: 6px;
    }

    .available {
      background: #dcfce7;
      color: #166534;
    }

    .claimed {
      background: #fee2e2;
      color: #991b1b;
    }

    .admin-badge {
      background: #dbeafe;
      color: #1d4ed8;
    }

    .action-row {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
      margin-top: 12px;
    }

    .small-btn {
      width: 100%;
      padding: 10px;
      border: none;
      border-radius: 10px;
      color: white;
      cursor: pointer;
      font-size: 14px;
    }

    .toggle-btn {
      background: #4338ca;
    }

    .toggle-btn:hover {
      background: #312e81;
    }

    .delete-btn {
      background: #dc2626;
    }

    .delete-btn:hover {
      background: #b91c1c;
    }

    .preview {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 12px;
      margin-top: 10px;
      display: none;
      border: 1px solid #cbd5e1;
    }

    .empty-message {
      background: white;
      padding: 20px;
      border-radius: 12px;
      text-align: center;
      color: #6b7280;
      box-shadow: 0 6px 16px rgba(0,0,0,0.05);
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
      margin-bottom: 18px;
    }

    .stat-box {
      background: white;
      border-radius: 12px;
      padding: 16px;
      box-shadow: 0 6px 16px rgba(0,0,0,0.05);
      text-align: center;
    }

    .stat-box h3 {
      font-size: 14px;
      color: #6b7280;
      margin-bottom: 6px;
    }

    .stat-box p {
      font-size: 24px;
      font-weight: bold;
      color: #1d4ed8;
    }

    .login-page {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
      background: linear-gradient(135deg, #dbeafe, #e0e7ff);
    }

    .login-card {
      width: 100%;
      max-width: 430px;
      background: white;
      border-radius: 20px;
      padding: 28px;
      box-shadow: 0 12px 30px rgba(0,0,0,0.12);
    }

    .login-card h1 {
      text-align: center;
      color: #1d4ed8;
      margin-bottom: 10px;
    }

    .login-card p {
      text-align: center;
      color: #6b7280;
      margin-bottom: 22px;
      line-height: 1.5;
    }

    .login-info {
      background: #eff6ff;
      color: #1e3a8a;
      padding: 12px;
      border-radius: 12px;
      font-size: 14px;
      margin-bottom: 16px;
      line-height: 1.6;
    }

    .error-message,
    .success-message {
      margin-top: 12px;
      padding: 10px 12px;
      border-radius: 10px;
      font-size: 14px;
    }

    .error-message {
      background: #fee2e2;
      color: #991b1b;
    }

    .success-message {
      background: #dcfce7;
      color: #166534;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 15px;
      background: white;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 6px 16px rgba(0,0,0,0.05);
    }

    th, td {
      padding: 12px;
      text-align: left;
      border-bottom: 1px solid #e5e7eb;
      font-size: 14px;
      vertical-align: top;
    }

    th {
      background: #eff6ff;
      color: #1e3a8a;
    }

    @media (max-width: 900px) {
      .container {
        grid-template-columns: 1fr;
      }

      header h1 {
        font-size: 26px;
      }

      .stats {
        grid-template-columns: 1fr;
      }
    }

    @media (max-width: 600px) {
      .action-row {
        grid-template-columns: 1fr;
      }

      .search-box {
        flex-direction: column;
      }

      .top-bar {
        flex-direction: column;
        align-items: stretch;
      }

      .top-bar-right {
        justify-content: stretch;
      }
    }
  </style>
</head>
<body>

  <section id="loginPage" class="login-page">
    <div class="login-card">
      <h1>School Login</h1>
      <p>Login for staff and admin to manage the school lost and found system.</p>



      <form id="loginForm">
        <div class="form-group">
          <label for="username">Username</label>
          <input type="text" id="username" placeholder="Enter username" required>
        </div>

        <div class="form-group">
          <label for="password">Password</label>
          <input type="password" id="password" placeholder="Enter password" required>
        </div>

        <button type="submit" class="btn">Login</button>
      </form>

      <div id="loginMessage"></div>
    </div>
  </section>

  <section id="mainApp" class="hidden">
    <header>
           <h1>Surya Global School</h1>
      <p>
        School Lost and Found Portal – Students can search lost items and staff can upload found items with photo,
        floor, class, and staff details.
      </p>
    </header>

    <div class="container">
      <div>
        <div class="card" id="staffPanel">
          <div class="top-bar">
            <h2>Staff Upload Panel</h2>
          </div>

          <form id="itemForm">
            <div class="form-group">
              <label for="itemName">Item Name</label>
              <input type="text" id="itemName" placeholder="Enter item name" required>
            </div>

            <div class="form-group">
              <label for="description">Description</label>
              <textarea id="description" placeholder="Enter item details" required></textarea>
            </div>

            <div class="form-group">
              <label for="floor">Floor Found</label>
              <input type="text" id="floor" placeholder="Example: 2nd Floor" required>
            </div>

            <div class="form-group">
              <label for="classRoom">Classroom</label>
              <input type="text" id="classRoom" placeholder="Example: Class 9A" required>
            </div>

            <div class="form-group">
              <label for="staffName">Staff Name</label>
              <input type="text" id="staffName" placeholder="Enter staff name" required>
            </div>

            <div class="form-group">
              <label for="staffContact">Staff Contact</label>
              <input type="text" id="staffContact" placeholder="Enter contact number">
            </div>

            <div class="form-group">
              <label for="dateFound">Date Found</label>
              <input type="date" id="dateFound" required>
            </div>

            <div class="form-group">
              <label for="itemImage">Upload Item Photo</label>
              <input type="file" id="itemImage" accept="image/*">
              <img id="imagePreview" class="preview" alt="Preview Image">
            </div>

            <button type="submit" class="btn">Add Item</button>
            <div id="formMessage"></div>
          </form>
        </div>
      </div>

      <div>
        <div class="top-bar">
          <h2 id="welcomeText">Dashboard</h2>
          <div class="top-bar-right">
            <span id="roleBadge" class="badge admin-badge">Role</span>
            <button id="logoutBtn" class="btn btn-danger" style="width:auto; padding:10px 16px;">Logout</button>
          </div>
        </div>

        <div class="stats">
          <div class="stat-box">
            <h3>Total Items</h3>
            <p id="totalItems">0</p>
          </div>
          <div class="stat-box">
            <h3>Available</h3>
            <p id="availableItems">0</p>
          </div>
          <div class="stat-box">
            <h3>Claimed</h3>
            <p id="claimedItems">0</p>
          </div>
        </div>

        <div class="search-box">
          <input type="text" id="searchInput" placeholder="Search by item, floor, class, or staff name...">
          <select id="statusFilter">
            <option value="All">All Status</option>
            <option value="Available">Available</option>
            <option value="Claimed">Claimed</option>
          </select>
        </div>

        <div id="itemsContainer" class="items-grid"></div>

        <div id="adminPanel" class="card hidden" style="margin-top:20px;">
          <h2>Admin Panel</h2>
          <p style="color:#6b7280; margin-bottom: 12px; line-height:1.5;">
            Admin can view all records, manage status, and delete wrong or duplicate entries.
          </p>
          <div style="overflow-x:auto;">
            <table>
              <thead>
                <tr>
                  <th>Item</th>
                  <th>Floor</th>
                  <th>Class</th>
                  <th>Staff</th>
                  <th>Status</th>
                  <th>Date</th>
                  <th>Action</th>
                </tr>
              </thead>
              <tbody id="adminTableBody"></tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  </section>

  <script>
    const loginPage = document.getElementById("loginPage");
    const mainApp = document.getElementById("mainApp");
    const loginForm = document.getElementById("loginForm");
    const loginMessage = document.getElementById("loginMessage");
    const logoutBtn = document.getElementById("logoutBtn");
    const roleBadge = document.getElementById("roleBadge");
    const welcomeText = document.getElementById("welcomeText");
    const adminPanel = document.getElementById("adminPanel");
    const staffPanel = document.getElementById("staffPanel");

    const itemForm = document.getElementById("itemForm");
    const itemsContainer = document.getElementById("itemsContainer");
    const searchInput = document.getElementById("searchInput");
    const statusFilter = document.getElementById("statusFilter");
    const itemImage = document.getElementById("itemImage");
    const imagePreview = document.getElementById("imagePreview");
    const formMessage = document.getElementById("formMessage");
    const adminTableBody = document.getElementById("adminTableBody");

    const totalItems = document.getElementById("totalItems");
    const availableItems = document.getElementById("availableItems");
    const claimedItems = document.getElementById("claimedItems");

    const users = [
      { username: "Surya", password: "Surya123", role: "Surya" },
    
    ];

    let currentUser = null;
    let imageData = "";

    let items = [];

    function showMessage(element, text, type) {
      element.innerHTML = `<div class="${type === 'error' ? 'error-message' : 'success-message'}">${text}</div>`;
      setTimeout(() => {
        element.innerHTML = "";
      }, 2500);
    }

    function saveData() {
      localStorage.setItem("lostFoundItems", JSON.stringify(items));
    }

    function loadData() {
      const saved = localStorage.getItem("lostFoundItems");
      if (saved) {
        items = JSON.parse(saved);
      }
    }

    function updateStats() {
      totalItems.textContent = items.length;
      availableItems.textContent = items.filter(item => item.status === "Available").length;
      claimedItems.textContent = items.filter(item => item.status === "Claimed").length;
    }

    function getFilteredItems() {
      const searchText = searchInput.value.toLowerCase();
      const selectedStatus = statusFilter.value;

      return items.filter(item => {
        const matchesSearch =
          item.itemName.toLowerCase().includes(searchText) ||
          item.description.toLowerCase().includes(searchText) ||
          item.floor.toLowerCase().includes(searchText) ||
          item.classRoom.toLowerCase().includes(searchText) ||
          item.staffName.toLowerCase().includes(searchText);

        const matchesStatus = selectedStatus === "All" || item.status === selectedStatus;
        return matchesSearch && matchesStatus;
      });
    }

    function renderItems() {
      const filteredItems = getFilteredItems();
      itemsContainer.innerHTML = "";

      if (filteredItems.length === 0) {
        itemsContainer.innerHTML = `<div class="empty-message">No items found.</div>`;
        return;
      }

      filteredItems.forEach(item => {
        const card = document.createElement("div");
        card.className = "item-card";

        const adminActions = currentUser && currentUser.role === "Admin"
          ? `
            <div class="action-row">
              <button class="small-btn toggle-btn" onclick="toggleStatus(${item.id})">
                Mark ${item.status === "Available" ? "Claimed" : "Available"}
              </button>
              <button class="small-btn delete-btn" onclick="deleteItem(${item.id})">Delete</button>
            </div>
          `
          : `
            <div class="action-row">
              <button class="small-btn toggle-btn" onclick="toggleStatus(${item.id})">
                Mark ${item.status === "Available" ? "Claimed" : "Available"}
              </button>
            </div>
          `;

        card.innerHTML = `
          <img src="${item.image}" alt="${item.itemName}">
          <div class="item-content">
            <h3>${item.itemName}</h3>
            <p><strong>Description:</strong> ${item.description}</p>
            <p><strong>Floor:</strong> ${item.floor}</p>
            <p><strong>Class:</strong> ${item.classRoom}</p>
            <p><strong>Staff:</strong> ${item.staffName}</p>
            <p><strong>Contact:</strong> ${item.staffContact || "Not given"}</p>
            <p><strong>Date Found:</strong> ${item.dateFound}</p>
            <span class="badge ${item.status === "Available" ? "available" : "claimed"}">${item.status}</span>
            ${adminActions}
          </div>
        `;

        itemsContainer.appendChild(card);
      });
    }

    function renderAdminTable() {
      adminTableBody.innerHTML = "";

      items.forEach(item => {
        const row = document.createElement("tr");
        row.innerHTML = `
          <td>${item.itemName}</td>
          <td>${item.floor}</td>
          <td>${item.classRoom}</td>
          <td>${item.staffName}</td>
          <td>${item.status}</td>
          <td>${item.dateFound}</td>
          <td>
            <button class="small-btn toggle-btn" style="margin-bottom:6px;" onclick="toggleStatus(${item.id})">Toggle</button>
            <button class="small-btn delete-btn" onclick="deleteItem(${item.id})">Delete</button>
          </td>
        `;
        adminTableBody.appendChild(row);
      });
    }

    function refreshUI() {
      updateStats();
      renderItems();
      if (currentUser && currentUser.role === "Admin") {
        renderAdminTable();
      }
      saveData();
    }

    loginForm.addEventListener("submit", function(e) {
      e.preventDefault();

      const username = document.getElementById("username").value.trim();
      const password = document.getElementById("password").value.trim();

      const foundUser = users.find(user => user.username === username && user.password === password);

      if (!foundUser) {
        showMessage(loginMessage, "Invalid username or password.", "error");
        return;
      }

      currentUser = foundUser;
      loginPage.classList.add("hidden");
      mainApp.classList.remove("hidden");

      roleBadge.textContent = currentUser.role;
      welcomeText.textContent = `Welcome, ${currentUser.role}`;

      if (currentUser.role === "Admin") {
        adminPanel.classList.remove("hidden");
        staffPanel.classList.remove("hidden");
      } else {
        adminPanel.classList.add("hidden");
        staffPanel.classList.remove("hidden");
      }

      refreshUI();
    });

    logoutBtn.addEventListener("click", function() {
      currentUser = null;
      mainApp.classList.add("hidden");
      loginPage.classList.remove("hidden");
      loginForm.reset();
      loginMessage.innerHTML = "";
    });

    itemImage.addEventListener("change", function () {
      const file = this.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = function (e) {
          imageData = e.target.result;
          imagePreview.src = imageData;
          imagePreview.style.display = "block";
        };
        reader.readAsDataURL(file);
      }
    });

    itemForm.addEventListener("submit", function (e) {
      e.preventDefault();

      const newItem = {
        id: Date.now(),
        itemName: document.getElementById("itemName").value,
        description: document.getElementById("description").value,
        floor: document.getElementById("floor").value,
        classRoom: document.getElementById("classRoom").value,
        staffName: document.getElementById("staffName").value,
        staffContact: document.getElementById("staffContact").value,
        dateFound: document.getElementById("dateFound").value,
        image: imageData || "https://via.placeholder.com/400x250?text=No+Image",
        status: "Available"
      };

      items.unshift(newItem);
      refreshUI();
      itemForm.reset();
      imageData = "";
      imagePreview.style.display = "none";
      showMessage(formMessage, "Item added successfully.", "success");
    });

    searchInput.addEventListener("input", renderItems);
    statusFilter.addEventListener("change", renderItems);

    function toggleStatus(id) {
      items = items.map(item => {
        if (item.id === id) {
          return {
            ...item,
            status: item.status === "Available" ? "Claimed" : "Available"
          };
        }
        return item;
      });
      refreshUI();
    }

    function deleteItem(id) {
      if (!currentUser || currentUser.role !== "Admin") {
        alert("Only admin can delete items.");
        return;
      }

      const confirmDelete = confirm("Are you sure you want to delete this item?");
      if (!confirmDelete) return;

      items = items.filter(item => item.id !== id);
      refreshUI();
    }

    loadData();
    refreshUI();
  </script>
</body>
</html>
