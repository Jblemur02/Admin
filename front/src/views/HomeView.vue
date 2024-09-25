<template>
  <main>
    <h1>Welcome back Brother<span> Jethro</span></h1>

    <div id="boxes">
      <div id="updates">
        <h2>Updates</h2>
        <p>
          Stay tuned for the latest updates on our admin console. New features and updates will be
          added regularly.
        </p>
      </div>

      <div id="news">
        <h2>News</h2>
        <div class="incoming">
          <div class="news-item">
            <h3>Latest Update</h3>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin ac neque nec urna
              fringilla tempor.
            </p>
            <a href="news.php?id=1">Read more</a>
          </div>

          <div class="news-item">
            <h3>System Announcement</h3>
            <p>
              Suspendisse potenti. Quisque scelerisque nulla at eros vulputate, vel pretium erat
              scelerisque.
            </p>
            <a href="news.php?id=2">Read more</a>
          </div>
        </div>
      </div>

      <div id="sermons">
        <h2>Sermons</h2>
        <div class="incoming">
          <div class="sermon-item">
            <h3></h3>
            <p><strong>Date:</strong></p>
            <a href="">View sermon</a>
          </div>
        </div>
      </div>

      <div id="contact">
        <h2>Incoming Contact Forms</h2>
        <div class="incoming">
          <div class="contact-form-item">
            <h3>From " "</h3>
            <p><strong>Date:</strong></p>
            <a href="church.com">View submission</a>
          </div>
          <p>No recent contact forms found.</p>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  width: 100%;
  display: flex;
  justify-content: center;
  flex-direction: column;
}

h1 {
  text-align: center;
}

h1 span {
  color: var(--accent);
}

#boxes {
  display: grid;
  gap: 20px;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 30% 70%;
  grid-template-areas:
    'updates updates updates'
    'news contact sermons';
  height: 90%;
}

#boxes > div {
  padding: 5%;
  text-align: center;
  border-radius: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background-color: var(--mini-background);
  box-shadow: var(--shadow);
}

#boxes div a {
  color: var(--accent);
  padding: 10px;
  border-radius: 10px;
  box-shadow: var(--hshadow);
}

#boxes div a:hover {
  background-color: var(--hover);
}

#updates {
  grid-area: updates;
}

#news {
  grid-area: news;
}

#sermons {
  grid-area: sermons;
}

#contact {
  grid-area: contact;
}

.contact-form-item,
.sermon-item,
.news-item {
  margin-bottom: 10px;
  border: 1px solid var(--text-color);
  padding: 2%;
  border-radius: 20px;
  width: 100%;
  box-shadow: var(--shadow);
  box-sizing: border-box;
}

.incoming {
  margin-top: 20px;
  padding: 10px;
  border-radius: 5px;
  background-color: var(--mini-background);
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 100%;
}

@media screen and (max-width: 800px) {
  #boxes {
    overflow-y: scroll;
    grid-template-columns: 1fr;
    grid-template-rows: auto;
    grid-template-areas:
      'updates'
      'news'
      'contact'
      'sermons';
  }

  #boxes > div {
    box-shadow: none;
  }
}
</style>
