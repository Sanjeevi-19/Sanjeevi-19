<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Git Hut - Overview</title>
  < style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #0d1117;
      color: #c9d1d9;
    }

    header {
      background-color: #161b22;
      padding: 20px;
      border-bottom: 1px solid #30363d;
    }

    .container {
      width: 85%;
      margin: auto;
    }

    .profile {
      display: flex;
      gap: 20px;
      margin-top: 30px;
    }

    .avatar {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      border: 2px solid #30363d;
    }

    .profile-info h1 {
      margin: 0;
      font-size: 28px;
    }

    .profile-info p {
      margin-top: 10px;
      color: #8b949e;
    }

    .repo-section {
      margin-top: 40px;
    }

    .repo-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 20px;
    }

    .repo-card {
      background-color: #161b22;
      padding: 16px;
      border: 1px solid #30363d;
      border-radius: 6px;
    }

    .repo-card h3 {
      margin: 0;
      color: #58a6ff;
    }

    .repo-card p {
      font-size: 14px;
      color: #8b949e;
    }

    .repo-meta {
      display: flex;
      justify-content: space-between;
      margin-top: 10px;
      font-size: 12px;
    }

    footer {
      margin-top: 60px;
      padding: 20px;
      text-align: center;
      color: #8b949e;
      border-top: 1px solid #30363d;
    }
  </style>
</head>
<body>

<header>
  <div class="container">
    <h2>🐙 Git Hut</h2>
  </div>
</header>

<main class="container">
  <section class="profile">
    <img class="avatar" src="https://avatars.githubusercontent.com/u/1?v=4" alt="Avatar">
    <div class="profile-info">
      <h1>Linus Torvalds</h1>
      <p>Creator of Linux and Git. Passionate about open source.</p>
    </div>
  </section>

  <section class="repo-section">
    <h2>Repositories</h2>
    <div class="repo-grid" id="repoGrid"></div>
  </section>
</main>

<footer>
  © 2026 Git Hut — Built with ❤️ using HTML, CSS & JS
</footer>

<script>
  const repositories = [
    {
      name: "linux",
      description: "Linux kernel source tree",
      language: "C",
      stars: 150000
    },
    {
      name: "git",
      description: "Distributed version control system",
      language: "C",
      stars: 45000
    },
    {
      name: "subsurface",
      description: "Dive log software",
      language: "C++",
      stars: 4000
    }
  ];

  const repoGrid = document.getElementById("repoGrid");

  repositories.forEach(repo => {
    const card = document.createElement("div");
    card.className = "repo-card";

    card.innerHTML = `
      <h3>${repo.name}</h3>
      <p>${repo.description}</p>
      <div class="repo-meta">
        <span>⭐ ${repo.stars}</span>
        <span>🧠 ${repo.language}</span>
      </div>
    `;

    repoGrid.appendChild(card);
  });
</script>

</body>
</html>
