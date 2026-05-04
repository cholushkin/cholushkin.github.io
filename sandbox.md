---
layout: default
title: Sandbox
permalink: /sandbox/
---

<h1>🧪 Sandbox</h1>

<div id="sandbox"></div>

<script>
const sandbox = [
    {
      title: "Island Generator",
      url: "/sandbox/islandgen/",
      description: "Experiment in generating islands using masks, noise, syntex, and marching cubes.",
      thumbnail: "/assets/thumbs/islandgen.jpg",
      tags: ["terrain", "procedural", "marching-cubes", "generation"]
    }
];
</script>

<script>
function renderSandbox() {
  const container = document.getElementById("sandbox");
  container.innerHTML = "";

  const COLUMNS = 2;

  container.style.display = "grid";
  container.style.gridTemplateColumns = `repeat(${COLUMNS}, 1fr)`;
  container.style.gap = "16px";

  sandbox.forEach(item => {
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
      window.open(item.url, "_blank");
    };

    el.innerHTML = `
      <div>
        <div style="
          width:100%;
          aspect-ratio: 5 / 3;
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

        <div style="font-size:13px; color:#555; margin-bottom:10px;">
          ${item.description || ""}
        </div>
      </div>

      <div style="font-size:12px; color:#777;">
        ${item.tags.map(t => `#${t}`).join(" ")}
      </div>
    `;

    container.appendChild(el);
  });
}

renderSandbox();
</script>