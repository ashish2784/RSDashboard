<script lang="ts">
  
  function filterCards(status: string) {
    const cards = document.querySelectorAll('[data-status]');

    cards.forEach((card) => {
      const el = card as HTMLElement;
      if (el.dataset.status === status) {
        el.classList.remove('hidden');
      } else {
        el.classList.add('hidden');
      }
    });
    
  }
</script>
      

<main>
    <div class="h-14 bg-white shadow flex items-center px-6 justify-between">
  
  <div class="flex items-center gap-2">
    <label for="section-select" class="hover:text-orange-600 cursor-pointer font-semibold">Section</label>
    <select id="section-select" class="border rounded-2xl p-2 text-sm">
        <option>Assembly Line</option>
        <option>Floor 2</option> 
        <option>Cutting Area</option>
        <option>Welding Area</option>
      </select>
  </div>

  <div class="flex gap-3">
    <button
      on:click={() => location.reload()}
      class="px-3 py-1 rounded-full bg-orange-100 text-orange-700 text-sm hover:ring-2 hover:ring-orange-400"
    >
      All
    </button>

    <button
      on:click={() => filterCards('ACTIVE')}
      class="px-3 py-1 rounded-full bg-green-100 text-green-700 text-sm hover:ring-2 hover:ring-green-400"
    >
      Active
    </button>

    <button
      on:click={() => filterCards('IDLE')}
      class="px-3 py-1 rounded-full bg-yellow-100 text-yellow-700 text-sm hover:ring-2 hover:ring-yellow-300"
    >
      Idle
    </button>

    <button
      on:click={() => filterCards('OFFLINE')}
      class="px-3 py-1 rounded-full bg-gray-100 text-gray-700 text-sm hover:ring-2 hover:ring-gray-300"
    >
      Offline
    </button>

    <button
      on:click={() => filterCards('BREAKDOWN')}
      class="px-3 py-1 rounded-full bg-red-100 text-red-700 text-sm hover:ring-2 hover:ring-red-300"
    >
      Break down
    </button>

    <button
      on:click={() => filterCards('SETUP')}
      class="px-3 py-1 rounded-full bg-blue-100 text-blue-700 text-sm hover:ring-2 hover:ring-blue-300"
    >
      Setup
    </button>
  </div>
</div>

</main>
