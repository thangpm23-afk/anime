<h2>Chỉ Số Nhân Vật (Tự động tính Gold / Rainbow / Secret)</h2>

<style>
  .stat-box {
    border: 1px solid #999;
    padding: 10px;
    margin-bottom: 15px;
    border-radius: 5px;
    width: 250px;
  }
</style>

<!-- BASIC -->
<div class="stat-box">
  <h3>Basic</h3>
  DMG: <input type="number" id="basicDmg" value="10"><br>
  HP: <input type="number" id="basicHp" value="100"><br>
</div>

<button onclick="calcTiers()">Hiện toàn bộ chỉ số</button>

<h3 id="resultStats"></h3>

<script>
function calcTiers() {
    let basicDmg = parseInt(document.getElementById("basicDmg").value);
    let basicHp  = parseInt(document.getElementById("basicHp").value);

    // Tính các tier
    let goldDmg = basicDmg * 4;
    let goldHp  = basicHp * 4;

    let rainbowDmg = goldDmg * 4; // = basic *16
    let rainbowHp  = goldHp * 4;

    let secretDmg = rainbowDmg * 4; // = basic *64
    let secretHp  = rainbowHp * 4;

    let text = 
    `📌 Basic → DMG: ${basicDmg}, HP: ${basicHp}\n` +
    `✨ Gold → DMG: ${goldDmg}, HP: ${goldHp}\n` +
    `🌈 Rainbow → DMG: ${rainbowDmg}, HP: ${rainbowHp}\n` +
    `🔥 Secret → DMG: ${secretDmg}, HP: ${secretHp}`;

    document.getElementById("resultStats").innerText = text;
}
</script>
