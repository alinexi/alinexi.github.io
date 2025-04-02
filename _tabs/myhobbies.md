---
# the default layout is 'page'
icon: fa-brands fa-pied-piper-hat
order: 5
---
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Entertainment Diary</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Roboto:wght@300;400&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Roboto', sans-serif;
      background: none;
      color: #333;
      line-height: 1.6;
      padding: 40px 20px;
    }

    header {
      text-align: center;
      margin-bottom: 50px;
    }

    header h1 {
      font-family: 'Montserrat', sans-serif;
      font-size: 3.5rem;
      margin-bottom: 15px;
      color: #111;
    }

    header p {
      font-size: 1.3rem;
      color: #444;
    }

    section {
      margin-bottom: 60px;
    }

    section h2 {
      font-family: 'Montserrat', sans-serif;
      margin-bottom: 20px;
      font-size: 2.2rem;
      text-align: center;
      color: #111;
      position: relative;
    }

    section h2::after {
      content: "";
      display: block;
      width: 60px;
      height: 4px;
      background: #111;
      margin: 10px auto 0;
      border-radius: 2px;
    }

    .filter-buttons {
      text-align: center;
      margin-bottom: 30px;
    }

    .filter-buttons button {
      margin: 5px;
      padding: 8px 16px;
      font-family: 'Montserrat', sans-serif;
      font-size: 0.95rem;
      background: #eee;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .filter-buttons button:hover {
      background-color: #ccc;
    }

    .cards-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 30px;
    }

    .card {
      background: #fff;
      border-radius: 16px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
      overflow: hidden;
      max-width: 300px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      display: none;
    }

    .card.visible {
      display: block;
    }

    .card:hover {
      transform: translateY(-8px);
      box-shadow: 0 12px 24px rgba(0, 0, 0, 0.15);
    }

    .card img {
      width: 100%;
      height: auto;
      display: block;
    }

    .card-content {
      padding: 20px 18px;
    }

    .card-content h3 {
      margin-bottom: 12px;
      font-family: 'Montserrat', sans-serif;
      font-size: 1.4rem;
      color: #222;
    }

    .card-content p {
      font-size: 1rem;
      color: #555;
    }

    .load-more {
      display: block;
      margin: 30px auto 0;
      padding: 10px 20px;
      font-size: 1rem;
      font-family: 'Montserrat', sans-serif;
      background-color: #111;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .load-more:hover {
      background-color: #333;
    }

    @media (max-width: 768px) {
      .cards-container {
        flex-direction: column;
        align-items: center;
      }
    }
  </style>
</head>

<body>
  <header>
    <h1>My Entertainment Diary</h1>
    <p>Discover the podcasts I'm listening to and the movies I'm watching or planning to watch.</p>
  </header>

  <section id="podcasts">
    <h2>Podcasts</h2>
    <div class="filter-buttons">
      <button onclick="filterCards('podcast-cards', 'all')">All</button>
      <button onclick="filterCards('podcast-cards', 'self')">Self-Improvement</button>
      <button onclick="filterCards('podcast-cards', 'psych')">Psychology</button>
      <button onclick="filterCards('podcast-cards', 'ent')">Entertainment</button>
    </div>
    <div class="cards-container" id="podcast-cards">
      <div class="card visible" data-category="self">
        <a href="https://bpluspodcast.com/podcast/seventh-season/%d9%85%d9%84%d8%aa-%d8%af%d9%88%d9%be%d8%a7%d9%85%db%8c%d9%86-%d9%be%db%8c%d8%af%d8%a7%da%a9%d8%b1%d8%af%d9%86-%d8%aa%d8%b9%d8%a7%d8%af%d9%84-%d8%af%d8%b1-%d8%b9%d8%b5%d8%b1-%d9%84%d8%b0%d8%aa/" target="_blank">
          <img src="https://bpluspodcast.com/wp-content/uploads/2025/03/E104-Main.png" alt="ملت دوپامین">
        </a>
        <div class="card-content">
          <h3><a href="https://bpluspodcast.com/podcast/seventh-season/%d9%85%d9%84%d8%aa-%d8%af%d9%88%d9%be%d8%a7%d9%85%db%8c%d9%86-%d9%be%db%8c%d8%af%d8%a7%da%a9%d8%b1%d8%af%d9%86-%d8%aa%d8%b9%d8%a7%d8%af%d9%84-%d8%af%d8%b1-%d8%b9%d8%b5%d8%b1-%d9%84%d8%b0%d8%aa/" target="_blank">ملت دوپامین</a></h3>
          <p>یکی از بهترین اپیزود هایی که وقتی گوش کردم دیدم چقدر منم ! مخصوصا قسمت الاکلنگ</p>
        </div>
      </div>
      <div class="card visible" data-category="self">
        <a href="https://castbox.fm/episode/id5278661-id574121324?country=gb" target="_blank">
          <img src="https://locomo.tips/podcast/ep8.jpg" alt="چرا احساس ناکافی بودن میکنیم؟">
        </a>
        <div class="card-content">
          <h3><a href="https://castbox.fm/episode/id5278661-id574121324?country=gb" target="_blank">چرا احساس ناکافی بودن میکنیم؟</a></h3>
          <p>این اپیزود شاهکاره چرا که دست گذاشته روی بزرکترین مسئله و بنیادی ترین مشکل بیشتر آدم ها مخصوصا برای ما که از فرهنگی میایم که این حس ناکافی بودن رو بشدت ساخته و پرداخته و خیلی چیزهامون بر پایه اشتباه ایجاد این حس درگیران ایجاد شده.</p>
        </div>
      </div>
    </div>
    <button class="load-more" onclick="loadMore('podcast-cards')">Load More Podcasts</button>
  </section>

  <section id="movies">
    <h2>Movies</h2>
    <div class="filter-buttons">
      <button onclick="filterCards('movie-cards', 'all')">All</button>
      <button onclick="filterCards('movie-cards', 'self')">Self-Improvement</button>
      <button onclick="filterCards('movie-cards', 'psych')">Psychology</button>
      <button onclick="filterCards('movie-cards', 'ent')">Entertainment</button>
    </div>
    <div class="cards-container" id="movie-cards">
      <div class="card visible" data-category="psych">
        <img src="https://encrypted-tbn3.gstatic.com/images?q=tbn:ANd9GcRXRbfRmmJ2oDyxNvHmg6_H_2NPPjABRFGjTaPICCdTlDj_WagxFqAXB52NFAcYV4lq8STXnw" alt="A Beautiful Mind">
        <div class="card-content">
          <h3>Enemy</h3>
          <p>هیچی نمیگم فقط برید و این فیلم رو ببینید ،‌به هیچعنوان  هم راجبش نخونید قبل دیدن</p>
        </div>
      </div>
      <div class="card visible" data-category="ent">
        <img src="https://lumiere-a.akamaihd.net/v1/images/p_walle_19753_69f7ff00.jpeg" alt="Everything Everywhere All At Once">
        <div class="card-content">
          <h3>WALL-E</h3>
          <p>مگر میشود وال ای رو ندید!! حتما حتما دستمال هم کنارتون باشه </p>
        </div>
      </div>
      <div class="card" data-category="self">
        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSW5mDPXOgS6E_2LJECbHxPT1x6s9Dv__YWcdkPw4Qr7lJ3QK3D7TXko5fj_D9ng1ka1prv" alt="The Pursuit of Happyness">
        <div class="card-content">
          <h3>The Pursuit of Happyness</h3>
          <p>Based on a true story, this film follows one man’s determination to create a better future for himself and his son.</p>
        </div>
      </div>
    </div>
    <button class="load-more" onclick="loadMore('movie-cards')">Load More Movies</button>
  </section>

  <script>
    function loadMore(sectionId) {
      const section = document.getElementById(sectionId);
      const hiddenCards = section.querySelectorAll('.card:not(.visible)');
      for (let i = 0; i < 6 && i < hiddenCards.length; i++) {
        hiddenCards[i].classList.add('visible');
      }
      if (section.querySelectorAll('.card:not(.visible)').length === 0) {
        section.nextElementSibling.style.display = 'none';
      }
    }

    function filterCards(containerId, category) {
      const container = document.getElementById(containerId);
      const cards = container.querySelectorAll('.card');
      cards.forEach(card => {
        const match = category === 'all' || card.dataset.category === category;
        card.style.display = match && card.classList.contains('visible') ? 'block' : 'none';
      });
    }

    document.addEventListener('DOMContentLoaded', () => {
      loadMore('podcast-cards');
      loadMore('movie-cards');
    });
  </script>
</body>
</html>
