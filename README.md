(function () {
  function init() {
    const box = document.getElementById("external-test");

    if (!box) return;

    box.innerHTML = `
      <strong>🚀 External JS ทำงานแล้ว!</strong>
      <br><br>
      <button id="external-test-button">
        ทดสอบปุ่ม
      </button>
    `;

    document
      .getElementById("external-test-button")
      .addEventListener("click", function () {
        alert("JavaScript จากภายนอกทำงานจริง!");
      });
  }

  if (document.readyState === "loading") {
    document.addEventListener("DOMContentLoaded", init);
  } else {
    init();
  }
})();
