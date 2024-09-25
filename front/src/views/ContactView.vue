<template>
  <div id="contact">
    <div id="header">
      <h1>Contact Form Submissions</h1>
      <div id="search">
        <form method="post">
          <input type="text" name="search" placeholder="Search..." />
          <input type="submit" value="Search" />
        </form>
      </div>
    </div>

    <div id="titles">
      <div class="name"><strong>Name</strong></div>
      <div class="email"><strong>Email</strong></div>
      <div class="phone"><strong>Phone</strong></div>
      <div class="date"><strong>Date</strong></div>
      <div class="action"><strong>Action</strong></div>
    </div>

    <!-- Display submissions -->
    <div id="body">
      <div class="item">
        <div class="name">echo $submission['name']; ?></div>
        <div class="email">echo $submission['email']; ?></div>
        <div class="phone">echo $submission['phone']; ?></div>
        $datetime = new DateTime($submission['submission_time']); $date = $datetime->format("F j,
        Y") . " at " . $datetime->format("g:i A"); ?>
        <div class="date">echo $date; ?></div>
        <div class="action">
          <span>
            <a id="viewContact" data-id=" $submission['id']; ?>">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="24px"
                viewBox="0 -960 960 960"
                width="24px"
                fill="#e8eaed"
              >
                <path
                  d="M480-320q75 0 127.5-52.5T660-500q0-75-52.5-127.5T480-680q-75 0-127.5 52.5T300-500q0 75 52.5 127.5T480-320Zm0-72q-45 0-76.5-31.5T372-500q0-45 31.5-76.5T480-608q45 0 76.5 31.5T588-500q0 45-31.5 76.5T480-392Zm0 192q-146 0-266-81.5T40-500q54-137 174-218.5T480-800q146 0 266 81.5T920-500q-54 137-174 218.5T480-200Zm0-300Zm0 220q113 0 207.5-59.5T832-500q-50-101-144.5-160.5T480-720q-113 0-207.5 59.5T128-500q50 101 144.5 160.5T480-280Z"
                />
              </svg>
            </a>
          </span>
          <span>
            <a
              id="deleteContact"
              data-id=" echo $submission['id']; ?>"
              data-name=" echo $submission['name']; ?>"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                height="24px"
                viewBox="0 -960 960 960"
                width="24px"
                fill="#e8eaed"
              >
                <path
                  d="M280-120q-33 0-56.5-23.5T200-200v-520h-40v-80h200v-40h240v40h200v80h-40v520q0 33-23.5 56.5T680-120H280Zm400-600H280v520h400v-520ZM360-280h80v-360h-80v360Zm160 0h80v-360h-80v360ZM280-720v520-520Z"
                />
              </svg>
            </a>
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
#contact {
  width: 90%;
  margin: 0 auto;
  padding: 20px;
  text-align: center;
  height: 100%;
  overflow: hidden;
  border-radius: 20px;
  box-shadow: var(--shadow);
  background-color: var(--mini-background);
  display: flex;
  flex-direction: column;
  justify-content: center;
}

#titles {
  display: grid;
  grid-template-columns: 1fr 3fr 1fr 2fr 1fr;
  border-bottom: 1px solid var(--underline);
}

#header {
  grid-column: span 5;
  text-align: center;
  padding: 1%;
  background-color: var(--active);
  border-radius: 20px;
  box-shadow: var(--hshadow);
}

.item {
  display: grid;
  grid-template-columns: 1fr 3fr 1fr 2fr 1fr;
  border-bottom: 1px solid var(--underline);
}

.name,
.email,
.phone,
.date,
.action {
  padding: 10px;
  text-align: left;
  display: flex;
  flex-direction: row;
}

#body {
  overflow-y: scroll;
  height: 100%;
}

.unviewed {
  font-weight: bold;
}
</style>
