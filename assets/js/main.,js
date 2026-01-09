/* ==============================
   main.js — Año automático + modo accesible
   ============================== */

/* Mensaje simple para comprobar que el archivo JS se ha cargado */
console.log("main.js cargado");

/* Esperamos a que todo el HTML esté listo antes de ejecutar el código */
document.addEventListener("DOMContentLoaded", () => {

  /* ==============================
     Año automático en el footer
     ============================== */

  /* Buscamos el elemento donde se muestra el año */
  const year = document.getElementById("year");

  /* Si existe, insertamos el año actual automáticamente */
  if (year) {
    year.textContent = new Date().getFullYear();
  }

  /* ==============================
     Botón de accesibilidad
     ============================== */

  /* Botón que activa y desactiva el modo accesible */
  const btn = document.getElementById("a11yToggle");

  /* Referencia al elemento <html> */
  const html = document.documentElement;

  /* Clave usada para guardar la preferencia del usuario */
  const KEY = "a11y-mode";

  /* ==============================
     Cargar preferencia guardada
     ============================== */

  /* Comprobamos si el usuario activó la accesibilidad anteriormente */
  const saved = localStorage.getItem(KEY);

  /* Si estaba activada, aplicamos el modo accesible al cargar la página */
  if (saved === "on") {
    html.setAttribute("data-a11y", "on");
  }

  /* ==============================
     Click en el botón
     ============================== */

  /* Añadimos el evento solo si el botón existe */
  if (btn) {
    btn.addEventListener("click", () => {

      /* Comprobamos si el modo accesible está activo */
      const isOn = html.getAttribute("data-a11y") === "on";

      /* Si está activo, lo desactivamos */
      if (isOn) {
        html.removeAttribute("data-a11y");
        localStorage.setItem(KEY, "off");
      } 
      /* Si no está activo, lo activamos */
      else {
        html.setAttribute("data-a11y", "on");
        localStorage.setItem(KEY, "on");
      }
    });
  }
});
