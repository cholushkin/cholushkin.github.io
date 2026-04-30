---
layout: default
title: Cheatsheets
permalink: /cheatsheets/
---

<h1>📚 Cheatsheets</h1>

<div id="cheatsheets"></div>

<script>
const cheatsheets = [
  {
    title: "JS Array Methods",
    url: "/cheatsheets/js-array-methods.html",
    categories: ["javascript", "basics"],
    thumbnail: "/assets/thumbs/js-array.png"
  },
  {
    title: "Unity FPS Controller",
    url: "/cheatsheets/fps-demo/",
    categories: ["unity", "gamedev"],
    thumbnail: "/assets/thumbs/unity-fps.png"
  }
];
</script>

<script>
function renderCheatsheets() {
  const container = document.getElementById("cheatsheets");
  container.innerHTML = "";

  const COLUMNS = 2;

  container.style.display = "grid";
  container.style.gridTemplateColumns = `repeat(${COLUMNS}, 1fr)`;
  container.style.gap = "16px";

  cheatsheets.forEach(item => {
    const el = document.createElement("div");

    el.style.border = "1px solid #eee";
    el.style.padding = "16px";
    el.style.borderRadius = "10px";
    el.style.background = "white";
    el.style.cursor = "pointer";

    el.style.display = "flex";
    el.style.flexDirection = "column";
    el.style.justifyContent = "space-between";

    el.onclick = () => {
      window.location.href = item.url;
    };

    el.innerHTML = `
	  <div>
		<div style="
		  width:100%;
		  height:120px;
		  background:#f0f0f0;
		  border-radius:6px;
		  margin-bottom:10px;
		  overflow:hidden;
		">
		  ${item.thumbnail ? `
			<img src="${item.thumbnail}" style="
			  width:100%;
			  height:100%;
			  object-fit:cover;
			  display:block;
			">
		  ` : ``}
		</div>

		<h3 style="margin:0 0 6px 0;">${item.title}</h3>
	  </div>

	  <div style="text-align:center; margin:12px 0; font-weight:500;">
		Read →
	  </div>

	  <div style="font-size:12px; color:#777;">
		${item.categories.map(c => `#${c}`).join(" ")}
	  </div>
	`;

    container.appendChild(el);
  });
}

renderCheatsheets();
</script>