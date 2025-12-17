<main>
  <div class="flex h-[calc(100vh-56px)]">

  <!-- ========== SIDEBAR ========== -->
  <aside
    id="sidebar"
    class="w-64 bg-gray-50 border-r transition-all duration-300 flex flex-col overflow-hidden items-center">

    <!-- Menu -->
    <nav class="flex-1 w-full px-2 space-y-2 flex flex-col items-center">

      <div class="flex items-center justify-start  gap-3 w-full px-3 py-3 rounded-lg cursor-pointer text-gray-700 sidebar-item primary-item transition-all">

        <img src="images/image3.png" alt="My Factory" class="h-4 w-4 shrink-0 sidebar-icon" />

        <span class="sidebar-text leading-6"><span class={`${collapsed ? 'hidden' : 'inline-block'} sidebar-text`}>My Factory</span></span>

      </div>

      <div class="flex items-center justify-start gap-3 w-full px-3 py-3 rounded-lg cursor-pointer text-gray-700 sidebar-item transition-all">
        <img src="images/image copy.png" alt="Machines" class="h-6 w-6 shrink-0 sidebar-icon" />
        <span class="sidebar-text leading-6"><span class={`${collapsed ? 'hidden' : 'inline-block'} sidebar-text`}>Machines</span></span>
      </div>

      <div class="flex items-center justify-start gap-3 w-full px-3 py-3 rounded-lg cursor-pointer text-gray-700 sidebar-item transition-all">
        <img src="images/image copy.png" alt="Production Info" class="h-6 w-6 shrink-0 sidebar-icon" />
        <span class="sidebar-text leading-6"><span class={`${collapsed ? 'hidden' : 'inline-block'} sidebar-text`}>Production Info</span></span>
      </div>

      <div class="flex items-center justify-start gap-3 w-full px-3 py-3 rounded-lg cursor-pointer text-gray-700 sidebar-item transition-all">
        <img src="images/image copy.png" alt="Operations" class="h-6 w-6 shrink-0 sidebar-icon" />
        <span class="sidebar-text leading-6"><span class={`${collapsed ? 'hidden' : 'inline-block'} sidebar-text`}>Operations</span></span>
      </div>

      <div class="flex items-center justify-start gap-3 w-full px-3 py-3 rounded-lg cursor-pointer text-gray-700 sidebar-item transition-all">
        <img src="images/image copy 4.png" alt="Maintenance" class="h-6 w-6 shrink-0 sidebar-icon" />
        <span class="sidebar-text leading-6"><span class={`${collapsed ? 'hidden' : 'inline-block'} sidebar-text`}>Maintenance Mode</span></span>
      </div>
    </nav>

    <!-- Collapse (Bottom) -->
    <button
      on:click={toggleSidebar}
      class="m-3 mt-auto flex items-center justify-center gap-2 text-sm text-gray-600 hover:text-orange-600"
    >
      <span id="collapse-icon">◀</span>
      <span id="collapse-text" class="sidebar-text">Collapse Menu</span>
    </button>
  </aside>
  <!-- ========== MAIN CONTENT ========== -->
  <main class="flex-1 p-6 overflow-y-auto">

    <!-- Cards Grid -->
    <div class="grid grid-cols-4 sm:grid-cols-2 lg:grid-cols-4 gap-6">

      <!-- CARD -->
      <div class="bg-red-100 rounded-xl shadow-xl p-5" data-status="BREAKDOWN">
        <div class="flex justify-between items-center mb-2">
          <h3 class="font-semibold">MACHINE NAME / ID</h3>
          <span class="text-xs px-2 py-1 bg-red-100 text-red-700 rounded">BREAKDOWN</span>
        </div>

        <p class="text-sm text-gray-500">Total Production</p>
        <p class="text-3xl font-bold mt-1">1004 <span class="text-base font-normal">m</span></p>

        <div class="mt-4 flex items-center gap-3">
          <div class="w-12 h-12 rounded-full border-4 border-green-500 flex items-center justify-center text-sm font-semibold">
            OEE
          </div>
          <span class="text-green-600 text-xl font-bold">50%</span>
        </div>
      </div>

      <!-- CARD -->
      <div class="bg-green-50 rounded-xl shadow-xl p-5" data-status="ACTIVE">
        <div class="flex justify-between items-center mb-2">
          <h3 class="font-semibold">MACHINE NAME / ID</h3>
          <span class="text-xs px-2 py-1 bg-green-100 text-green-700 rounded">ACTIVE</span>
        </div>

        <p class="text-sm text-gray-500">Total Production</p>
        <p class="text-3xl font-bold mt-1">7836 <span class="text-base">m</span></p>

        <div class="mt-4 flex items-center gap-3">
          <div class="w-12 h-12 rounded-full border-4 border-red-400 flex items-center justify-center text-sm font-semibold">
            OEE
          </div>
          <span class="text-red-500 text-xl font-bold">50%</span>
        </div>
      </div>

      <!-- CARD -->
      <div class="bg-yellow-50 rounded-xl shadow-xl p-5" data-status="IDLE">
        <div class="flex justify-between items-center mb-2">
          <h3 class="font-semibold">MACHINE NAME / ID</h3>
          <span class="text-xs px-2 py-1 bg-yellow-100 text-yellow-700 rounded">IDLE</span>
        </div>

        <p class="text-sm text-gray-500">Total Production</p>
        <p class="text-3xl font-bold mt-1">1004 <span class="text-base">m</span></p>

        <div class="mt-4 flex items-center gap-3">
          <div class="w-12 h-12 rounded-full border-4 border-green-500 flex items-center justify-center text-sm font-semibold">
            OEE
          </div>
          <span class="text-green-600 text-xl font-bold">50%</span>
        </div>
      </div>

      <!-- CARD -->
      <div class="bg-blue-50 rounded-xl shadow-xl p-5" data-status="SETUP">
        <div class="flex justify-between items-center mb-2">
          <h3 class="font-semibold">MACHINE NAME / ID</h3>
          <span class="text-xs px-2 py-1 bg-blue-100 text-blue-700 rounded">SETUP</span>
        </div>

        <p class="text-sm text-gray-500">Total Production</p>
        <p class="text-3xl font-bold mt-1">NA</p>

        <div class="mt-4 flex items-center gap-3">
          <div class="w-12 h-12 rounded-full border-4 border-gray-300 flex items-center justify-center text-sm font-semibold">
            OEE
          </div>
          <span class="text-gray-500 text-xl font-bold">NA</span>
        </div>
      </div>


      <div class="bg-yellow-50 rounded-xl shadow-xl p-5" data-status="IDLE">
        <div class="flex justify-between items-center mb-2">
          <h3 class="font-semibold">MACHINE NAME / ID</h3>
          <span class="text-xs px-2 py-1 bg-yellow-100 text-yellow-700 rounded">IDLE</span>
        </div>

        <p class="text-sm text-gray-500">Total Production</p>
        <p class="text-3xl font-bold mt-1">1004 <span class="text-base">m</span></p>

        <div class="mt-4 flex items-center gap-3">
          <div class="w-12 h-12 rounded-full border-4 border-green-500 flex items-center justify-center text-sm font-semibold">
            OEE
          </div>
          <span class="text-green-600 text-xl font-bold">50%</span>
        </div>
      </div>


      <div class="bg-yellow-50 rounded-xl shadow-xl p-5" data-status="IDLE">
        <div class="flex justify-between items-center mb-2">
          <h3 class="font-semibold">MACHINE NAME / ID</h3>
          <span class="text-xs px-2 py-1 bg-yellow-100 text-yellow-700 rounded">IDLE</span>
        </div>

        <p class="text-sm text-gray-500">Total Production</p>
        <p class="text-3xl font-bold mt-1">1004 <span class="text-base">m</span></p>

        <div class="mt-4 flex items-center gap-3">
          <div class="w-12 h-12 rounded-full border-4 border-green-500 flex items-center justify-center text-sm font-semibold">
            OEE
          </div>
          <span class="text-green-600 text-xl font-bold">50%</span>
        </div>
      </div>


     <!-- CARD -->
      <div class="bg-red-100 rounded-xl shadow-xl p-5" data-status="BREAKDOWN">
        <div class="flex justify-between items-center mb-2">
          <h3 class="font-semibold">MACHINE NAME / ID</h3>
          <span class="text-xs px-2 py-1 bg-red-100 text-red-700 rounded">BREAKDOWN</span>
        </div>

        <p class="text-sm text-gray-500">Total Production</p>
        <p class="text-3xl font-bold mt-1">1004 <span class="text-base font-normal">m</span></p>

        <div class="mt-4 flex items-center gap-3">
          <div class="w-12 h-12 rounded-full border-4 border-green-500 flex items-center justify-center text-sm font-semibold">
            OEE
          </div>
          <span class="text-green-600 text-xl font-bold">50%</span>
        </div>
      </div>


       <!-- CARD -->
      <div class="bg-green-50 rounded-xl shadow-xl p-5" data-status="ACTIVE">
        <div class="flex justify-between items-center mb-2">
          <h3 class="font-semibold">MACHINE NAME / ID</h3>
          <span class="text-xs px-2 py-1 bg-green-100 text-green-700 rounded">ACTIVE</span>
        </div>

        <p class="text-sm text-gray-500">Total Production</p>
        <p class="text-3xl font-bold mt-1">7836 <span class="text-base">m</span></p>

        <div class="mt-4 flex items-center gap-3">
          <div class="w-12 h-12 rounded-full border-4 border-red-400 flex items-center justify-center text-sm font-semibold">
            OEE
          </div>
          <span class="text-red-500 text-xl font-bold">50%</span>
        </div>
      </div>



      <div class="bg-yellow-50 rounded-xl shadow-xl p-5" data-status="IDLE">
        <div class="flex justify-between items-center mb-2">
          <h3 class="font-semibold">MACHINE NAME / ID</h3>
          <span class="text-xs px-2 py-1 bg-yellow-100 text-yellow-700 rounded">IDLE</span>
        </div>

        <p class="text-sm text-gray-500">Total Production</p>
        <p class="text-3xl font-bold mt-1">1004 <span class="text-base">m</span></p>

        <div class="mt-4 flex items-center gap-3">
          <div class="w-12 h-12 rounded-full border-4 border-green-500 flex items-center justify-center text-sm font-semibold">
            OEE
          </div>
          <span class="text-green-600 text-xl font-bold">50%</span>
        </div>
      </div>



    <!-- CARD -->
      <div class="bg-green-50 rounded-xl shadow-xl p-5" data-status="ACTIVE">
        <div class="flex justify-between items-center mb-2">
          <h3 class="font-semibold">MACHINE NAME / ID</h3>
          <span class="text-xs px-2 py-1 bg-green-100 text-green-700 rounded">ACTIVE</span>
        </div>

        <p class="text-sm text-gray-500">Total Production</p>
        <p class="text-3xl font-bold mt-1">7836 <span class="text-base">m</span></p>

        <div class="mt-4 flex items-center gap-3">
          <div class="w-12 h-12 rounded-full border-4 border-red-400 flex items-center justify-center text-sm font-semibold">
            OEE
          </div>
          <span class="text-red-500 text-xl font-bold">50%</span>
        </div>
      </div>


      <div class="bg-yellow-50 rounded-xl shadow-xl p-5" data-status="IDLE">
        <div class="flex justify-between items-center mb-2">
          <h3 class="font-semibold">MACHINE NAME / ID</h3>
          <span class="text-xs px-2 py-1 bg-yellow-100 text-yellow-700 rounded">IDLE</span>
        </div>

        <p class="text-sm text-gray-500">Total Production</p>
        <p class="text-3xl font-bold mt-1">1004 <span class="text-base">m</span></p>

        <div class="mt-4 flex items-center gap-3">
          <div class="w-12 h-12 rounded-full border-4 border-green-500 flex items-center justify-center text-sm font-semibold">
            OEE
          </div>
          <span class="text-green-600 text-xl font-bold">50%</span>
        </div>
      </div>

    </div>
  </main>
</div>
</main>


<script>
   let collapsed = false;

  function toggleSidebar() {
    const sidebar = document.getElementById("sidebar");
    const texts = document.querySelectorAll(".sidebar-text");
    const collapseText = document.getElementById("collapse-text");
    const icon = document.getElementById("collapse-icon");

    if (!sidebar || !collapseText || !icon) {
      return;
    }

    collapsed = !collapsed;

    if (collapsed) {
      sidebar.classList.remove("w-64");
      sidebar.classList.add("w-16", "collapsed");
      collapseText.classList.add("hidden");
      icon.textContent = "▶";
    } else {
      sidebar.classList.remove("w-16", "collapsed");
      sidebar.classList.add("w-64");
      collapseText.classList.remove("hidden");
      icon.textContent = "◀";
    }
  }

 function filterCards(status) {
    const cards = document.querySelectorAll('[data-status]');

    cards.forEach(card => {
      if (card.dataset.status === status) {
        card.classList.remove('hidden');
      } else {
        card.classList.add('hidden');
      }
    });
  }
</script>

<style>
  /* ===== SIDEBAR BASE ===== */
  .sidebar-item {
    transition: background-color 0.2s ease, transform 0.2s ease;
  }

  .sidebar-item:hover {
    background-color: #eef2ff;
  }

  /* ===== COLLAPSED MODE ===== */
  

  .collapsed nav {
    padding: 0;
    align-items: center;
  }

  .collapsed .sidebar-item {
    width: 48px;
    height: 48px;
    padding: 0;
    justify-content: center;
    border-radius: 12px;
  }

  .collapsed .sidebar-icon {
    margin: 0;
  }

  .collapsed .sidebar-text {
    display: none;
  }

  /* Hide all items except My Factory when collapsed */
  .collapsed .sidebar-item:not(.primary-item) {
    display: none;
  }

  /* Keep My Factory icon centered in collapsed mode */
  .collapsed .primary-item {
    width: 48px;
    height: 48px;
    padding: 0;
    justify-content: center;
    border-radius: 12px;
  }

  .collapsed .sidebar-item:hover {
    background-color: #e0e7ff;
    transform: scale(1.05);
  }
</style>
