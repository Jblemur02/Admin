<template>
  <main>
    <nav id="sidebar">
      <div id="top">
        <div id="top-links">
          <li class="nav-link" id="settings-btn">
            <a>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="20px"
                viewBox="0 -960 960 960"
                width="20px"
                fill="#000000"
              >
                <path
                  d="m403-96-22-114q-23-9-44.5-21T296-259l-110 37-77-133 87-76q-2-12-3-24t-1-25q0-13 1-25t3-24l-87-76 77-133 110 37q19-16 40.5-28t44.5-21l22-114h154l22 114q23 9 44.5 21t40.5 28l110-37 77 133-87 76q2 12 3 24t1 25q0 13-1 25t-3 24l87 76-77 133-110-37q-19 16-40.5 28T579-210L557-96H403Zm77-240q60 0 102-42t42-102q0-60-42-102t-102-42q-60 0-102 42t-42 102q0 60 42 102t102 42Z"
                />
              </svg>
            </a>
            <span class="tooltip">Settings</span>
          </li>

          <li class="nav-link" id="users-btn">
            <a>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="20px"
                viewBox="0 -960 960 960"
                width="20px"
                fill="#000000"
              >
                <path
                  d="M480-480q-60 0-102-42t-42-102q0-60 42-102t102-42q60 0 102 42t42 102q0 60-42 102t-102 42ZM192-192v-96q0-23 12.5-43.5T239-366q55-32 116.5-49T480-432q63 0 124.5 17T721-366q22 13 34.5 34t12.5 44v96H192Z"
                />
              </svg>
            </a>
            <span class="tooltip">Users</span>
          </li>

          <li class="nav-link" id="dark-btn">
            <a onclick="enableDarkMode()">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="20px"
                viewBox="0 -960 960 960"
                width="20px"
                fill="#000000"
              >
                <path
                  d="M479.96-144Q340-144 242-242t-98-238q0-140 97.93-238t237.83-98q13.06 0 25.65 1 12.59 1 25.59 3-39 29-62 72t-23 92q0 85 58.5 143.5T648-446q49 0 92-23t72-62q2 13 3 25.59t1 25.65q0 139.9-98.04 237.83t-238 97.93Z"
                />
              </svg>

              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="24px"
                viewBox="0 -960 960 960"
                width="24px"
                fill="#e8eaed"
              >
                <path
                  d="M480-28 346-160H160v-186L28-480l132-134v-186h186l134-132 134 132h186v186l132 134-132 134v186H614L480-28Zm0-252q83 0 141.5-58.5T680-480q0-83-58.5-141.5T480-680v400Zm0 140 100-100h140v-140l100-100-100-100v-140H580L480-820 380-720H240v140L140-480l100 100v140h140l100 100Zm0-340Z"
                />
              </svg>
              <span class="tooltip">Dark Mode</span>
            </a>
          </li>

          <li class="nav-link" id="shrink-btn">
            <a>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="20px"
                viewBox="0 -960 960 960"
                width="20px"
                fill="#000000"
              >
                <path d="M144-264v-72h672v72H144Zm0-180v-72h672v72H144Zm0-180v-72h672v72H144Z" />
              </svg>
              <span class="tooltip">Toggle Sidebar</span>
            </a>
          </li>
        </div>

        <div id="user-info">
          <img src="./pictures/pastor.png" alt="User" id="user-img" />
          <h3 id="user-name">
            <span>Jethro</span>
          </h3>
        </div>
      </div>

      <div id="middle">
        <li>
          <router-link to="/" class="nav-link">
            <span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="20px"
                viewBox="0 -960 960 960"
                width="20px"
                fill="#000000"
              >
                <path d="M192-144v-456l288-216 288 216v456H552v-264H408v264H192Z" />
              </svg>
            </span>
            <span class="nav-text">Home</span>
            <span class="tooltip">Dashboard</span>
          </router-link>
        </li>

        <li>
          <router-link to="/events" class="nav-link">
            <span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="20px"
                viewBox="0 -960 960 960"
                width="20px"
                fill="#000000"
              >
                <path
                  d="M576.23-240Q536-240 508-267.77q-28-27.78-28-68Q480-376 507.77-404q27.78-28 68-28Q616-432 644-404.23q28 27.78 28 68Q672-296 644.23-268q-27.78 28-68 28ZM216-96q-29.7 0-50.85-21.5Q144-139 144-168v-528q0-29 21.15-50.5T216-768h72v-96h72v96h240v-96h72v96h72q29.7 0 50.85 21.5Q816-725 816-696v528q0 29-21.15 50.5T744-96H216Zm0-72h528v-360H216v360Z"
                />
              </svg>
            </span>
            <span class="nav-text">Events</span>
            <span class="tooltip">View Events</span>
          </router-link>
        </li>

        <li>
          <router-link class="nav-link" to="/sermons">
            <span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="20px"
                viewBox="0 -960 960 960"
                width="20px"
                fill="#000000"
              >
                <path
                  d="m253-288 74-129q-47 0-83-37.5T208-544q0-54 37-91t91-37q54 0 91 37t37 91q0 17-5 33t-13 30L336-288h-83Zm288 0 74-129q-47 0-83-37.5T496-544q0-54 37-91t91-37q54 0 91 37t37 91q0 17-4.5 33T735-481L624-288h-83Z"
                />
              </svg>
            </span>
            <span class="nav-text">Sermons</span>
            <span class="tooltip">View Sermons</span>
          </router-link>
        </li>

        <li>
          <router-link to="/contact" class="nav-link">
            <span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="24px"
                viewBox="0 -960 960 960"
                width="24px"
                fill="#e8eaed"
              >
                <path
                  d="M480-80q-83 0-156-31.5T197-197q-54-54-85.5-127T80-480q0-83 31.5-156T197-763q54-54 127-85.5T480-880q83 0 156 31.5T763-763q54 54 85.5 127T880-480v58q0 59-40.5 100.5T740-280q-35 0-66-15t-52-43q-29 29-65.5 43.5T480-280q-83 0-141.5-58.5T280-480q0-83 58.5-141.5T480-680q83 0 141.5 58.5T680-480v58q0 26 17 44t43 18q26 0 43-18t17-44v-58q0-134-93-227t-227-93q-134 0-227 93t-93 227q0 134 93 227t227 93h200v80H480Zm0-280q50 0 85-35t35-85q0-50-35-85t-85-35q-50 0-85 35t-35 85q0 50 35 85t85 35Z"
                />
              </svg>
            </span>
            <span class="nav-text">Contact</span>
            <span class="tooltip">Contact Forms</span>
          </router-link>
        </li>

        <li>
          <router-link to="/members" class="nav-link">
            <span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="20px"
                viewBox="0 -960 960 960"
                width="20px"
                fill="#000000"
              >
                <path
                  d="M48-264v-57q0-39 39-63t105-24q14 0 26 1t23 3q-12 18-18.5 39.11Q216-343.77 216-322v58H48Zm216 0v-58q0-28 14.5-50t43.5-39q29-17 69-25t89.5-8q49.5 0 89 8t68.5 25q29 16 43.5 38.69Q696-349.62 696-322v58H264Zm480 0v-58q0-22-6.5-42.5T719-404q9-2 20.5-3t28.5-1q66 0 105 24t39 63v57H744ZM192-456q-30 0-51-21t-21-51q0-30 21-51t51-21q30 0 51 21t21 51q0 30-21 51t-51 21Zm576 0q-30 0-51-21t-21-51q0-30 21-51t51-21q30 0 51 21t21 51q0 30-21 51t-51 21Zm-288-36q-45 0-76.5-31.52T372-600.07q0-44.93 31.52-76.43 31.52-31.5 76.55-31.5 44.93 0 76.43 31.55Q588-644.9 588-600q0 45-31.55 76.5T480-492Z"
                />
              </svg>
            </span>
            <span class="nav-text">Members</span>
            <span class="tooltip">Manage Members</span>
          </router-link>
        </li>

        <li>
          <router-link to="/news" class="nav-link">
            <span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="20px"
                viewBox="0 -960 960 960"
                width="20px"
                fill="#000000"
              >
                <path
                  d="M168-144q-29.7 0-50.85-21.15Q96-186.3 96-216v-600l64.32 64 63.36-64L288-752l64.32-64 63.36 64L480-816l64.32 64 63.36-64L672-752l64.32-64 63.36 64L864-816v600q0 29.7-21.15 50.85Q821.7-144 792-144H168Zm0-72h276v-216H168v216Zm348 0h276v-72H516v72Zm0-144h276v-72H516v72ZM168-504h624v-144H168v144Z"
                />
              </svg>
            </span>
            <span class="nav-text">News</span>
            <span class="tooltip">View News</span>
          </router-link>
        </li>

        <li>
          <router-link to="/traffic" class="nav-link">
            <span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="20px"
                viewBox="0 -960 960 960"
                width="20px"
                fill="#000000"
              >
                <path
                  d="M480-264q20 0 34-14t14-34q0-20-14-34t-34-14q-20 0-34 14t-14 34q0 20 14 34t34 14Zm0-168q20 0 34-14t14-34q0-20-14-34t-34-14q-20 0-34 14t-14 34q0 20 14 34t34 14Zm0-168q20 0 34-14t14-34q0-20-14-34t-34-14q-20 0-34 14t-14 34q0 20 14 34t34 14ZM288-384v-33q-45-11-70.5-49.5T192-552h96v-33q-45-11-70.5-49.5T192-720h96v-24q0-30 21-51t51-21h240q30 0 51 21t21 51v24h96q0 47-25.5 85T672-585v33h96q0 47-25.5 85T672-417v33h96q0 47-25.5 85.5T672-248v32q0 30-21 51t-51 21H360q-30 0-51-21t-21-51v-32q-45-12-70.5-50.5T192-384h96Z"
                />
              </svg>
            </span>

            <span class="nav-text">Traffic</span>
            <span class="tooltip">View Traffic</span>
          </router-link>
        </li>

        <li>
          <router-link class="nav-link" to="/developer">
            <span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="20px"
                viewBox="0 -960 960 960"
                width="20px"
                fill="#000000"
              >
                <path
                  d="M480-528q147 0 241.5-40.5T816-672q0-59-99-101.5T480-816q-138 0-237 42.5T144-672q0 63 94.5 103.5T480-528Zm0 96q68 0 129-11.5T716-475q46-20 73-46t27-55v96q0 29-27 55t-73 46q-46 20-107 31.5T480-336q-68 0-129-11.5T244-379q-46-20-73-46t-27-55v-96q0 29 27 55t73 46q46 20 107 31.5T480-432Zm0 192q68 0 129-11.5T716-283q46-20 73-46t27-55v96q0 29-27 55t-73 46q-46 20-107 31.5T480-144q-68 0-129-11.5T244-187q-46-20-73-46t-27-55v-96q0 29 27 55t73 46q46 20 107 31.5T480-240Z"
                />
              </svg>
            </span>

            <span class="nav-text">Developer</span>
            <span class="tooltip">View Updates</span>
          </router-link>
        </li>
      </div>

      <div id="bottom">
        <a id="logout-btn" class="nav-link" data-data-title="Log Out">
          <span>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              height="20px"
              viewBox="0 -960 960 960"
              width="20px"
              fill="#000000"
            >
              <path
                d="M216-144q-29.7 0-50.85-21.15Q144-186.3 144-216v-528q0-29.7 21.15-50.85Q186.3-816 216-816h264v72H216v528h264v72H216Zm432-168-51-51 81-81H384v-72h294l-81-81 51-51 168 168-168 168Z"
              />
            </svg>
          </span>

          <span class="nav-text">Logout</span>
          <span class="tooltip">Logout</span>
        </a>
      </div>
    </nav>
  </main>
</template>

<script>
document.addEventListener('DOMContentLoaded', () => {
  // Handle theme selection
  const darkBtn = document.getElementById('dark-btn')
  let darkMode = localStorage.getItem('darkmode')

  // Function to enable dark mode
  const enableDarkMode = () => {
    document.body.classList.add('dark-mode')
    localStorage.setItem('darkmode', 'active')
  }

  // Function to disable dark mode
  const disableDarkMode = () => {
    document.body.classList.remove('dark-mode')
    localStorage.setItem('darkmode', null)
  }

  // Check for dark mode and apply it before loading content
  if (darkMode === 'active') {
    enableDarkMode()
  }

  if (darkBtn) {
    darkBtn.addEventListener('click', () => {
      darkMode = localStorage.getItem('darkmode')
      darkMode !== 'active' ? enableDarkMode() : disableDarkMode()
    })
  }

  // Handle dialogs
  const settingsBtn = document.getElementById('settings-btn')
  const settingsDialog = document.getElementById('settings-dialog')
  const usersBtn = document.getElementById('users-btn')
  const usersDialog = document.getElementById('users-dialog')
  const logoutBtn = document.getElementById('logout-btn')
  const logoutDialog = document.getElementById('logout-dialog')

  function showDialog(dialog, show) {
    if (show) {
      dialog.showModal()
      localStorage.setItem('dialog', dialog.id)
      const wrapper = dialog.querySelector('.wrapper')
      dialog.addEventListener('click', (e) => {
        if (!wrapper.contains(e.target)) {
          showDialog(dialog, false)
        }
      })
    } else {
      dialog.close()
      localStorage.removeItem('dialog')
    }
  }

  // Check for stored dialog on page load
  const dialogId = localStorage.getItem('dialog')
  if (dialogId) {
    const dialog = document.getElementById(dialogId)
    if (dialog) {
      showDialog(dialog, true)
    }
  }

  // Handle settings dialog
  if (settingsBtn) {
    settingsBtn.addEventListener('click', () => showDialog(settingsDialog, true))
  }
  if (logoutBtn) {
    logoutBtn.addEventListener('click', () => showDialog(logoutDialog, true))
  }
  if (usersBtn) {
    usersBtn.addEventListener('click', () => showDialog(usersDialog, true))
  }

  // Handle sidebar and content loading
  const shrinkBtn = document.getElementById('shrink-btn')
  const sidebar = document.getElementById('sidebar')

  let sidebarShrunk = localStorage.getItem('sidebarShrunk')

  // Function to shrink the sidebar
  const shrinkSidebar = () => {
    sidebar.classList.add('shrunk')
    localStorage.setItem('sidebarShrunk', 'true')
  }

  // Function to expand the sidebar
  const expandSidebar = () => {
    sidebar.classList.remove('shrunk')
    localStorage.setItem('sidebarShrunk', 'false')
  }

  // If the sidebar was shrunk before, keep it shrunk
  if (sidebarShrunk === 'true') shrinkSidebar()

  // Add event listener to the button to toggle sidebar shrink state
  shrinkBtn.addEventListener('click', () => {
    sidebarShrunk = localStorage.getItem('sidebarShrunk')
    sidebarShrunk !== 'true' ? shrinkSidebar() : expandSidebar()
  })
})
</script>

<style scoped>
main {
  width: 100%;
  height: 100%;
  background-color: var(--background);
  display: flex;
}

#sidebar {
  height: 100%;
  width: 100%;
  background-color: var(--mini-background);
  padding: 10px;
  box-shadow: var(--shadow);
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 20% auto 5%;
  grid-template-areas:
    'top'
    'middle'
    'bottom';
  border-radius: 20px;
  overflow: hidden;
  position: relative;
}

#top {
  grid-area: top;
  height: 100%;
  gap: 1%;
  border-bottom: 2px solid var(--underline);
  justify-content: space-between;
  padding: 5% 0;
}

#middle {
  grid-area: middle;
  font-size: 1.2rem;
  justify-content: space-between;
  padding: 20px 0px;
}

#bottom {
  grid-area: bottom;
  margin-bottom: 0;
  border-top: 2px solid var(--underline);
  justify-content: center;
}

#top .nav-link,
#bottom .nav-link {
  box-shadow: var(--hshadow);
}

.shrunk #middle .nav-link {
  box-shadow: var(--hshadow);
}

#top,
#middle,
#bottom {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}

svg {
  object-fit: cover;
  fill: var(--fill);
}

#top-links {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 10px;
  width: 100%;
  margin: 0 auto;
}

#user-info {
  display: flex;
  align-items: center;
  flex-direction: column;
  flex-shrink: 0;
}

#user-info img {
  width: 60%;
  height: auto;
  border-radius: 50%;
  border: 2px solid wheat;
  box-shadow: var(--shadow);
}

#main-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  width: 100%;
  overflow: hidden;
  padding: 0.5% 1%;
}

#logout-btn {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 0 0 10px 10px;
}

.nav-link {
  display: block;
  width: 100%;
  padding: 10px 0;
  text-align: center;
  border-radius: 10px;
  white-space: nowrap;
  margin: 5% auto;
  position: relative;
}

.tooltip {
  display: none;
  position: absolute !important;
  padding: 5px 10px;
  border-radius: 5px;
  background-color: var(--background);
  color: var(--text-color);
  left: 110%;
  top: 50%;
  transform: translateY(-50%);
  box-shadow: var(--shadow);
  z-index: 1000;
  white-space: nowrap;
}

.shrunk .nav-link:hover .tooltip {
  display: block;
}

li {
  width: 100%;
}

li:hover {
  cursor: pointer;
}

.nav-link:hover {
  background-color: var(--hover);
  box-shadow: var(--hshadow);
}

a,
a span {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  padding: 5px;
  flex-direction: row;
}

#user-info h3 {
  flex-wrap: wrap;
  display: flex;
  justify-content: center;
}

h3 span {
  color: var(--accent);
  font-weight: normal;
}

.dark-mode #dark-btn a svg:first-child,
#dark-btn a svg:nth-child(2) {
  display: none;
}

.dark-mode #dark-btn a svg:nth-child(2),
#dark-btn a svg:first-child {
  display: block;
}

#sidebar.shrunk {
  width: 5%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 10px 1%;
}

#sidebar.shrunk #user-info img {
  width: 100%;
  margin-bottom: 25%;
}

.shrunk #top,
.shrunk #middle,
.shrunk #bottom {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  height: auto;
  padding: 5% 0;
}

.shrunk #user-info h3,
.shrunk .nav-text {
  display: none;
}

.shrunk svg {
  width: 80%;
  height: auto;
  object-fit: border-box;
}

.shrunk #top-links {
  flex-direction: column-reverse;
}

.active,
.active:hover {
  background-color: var(--active);
  box-shadow: var(--shadow);
}
</style>
