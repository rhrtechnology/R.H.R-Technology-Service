const loginBtn = document.getElementById("loginBtn");
const logoutBtn = document.getElementById("logoutBtn");
const loginModal = document.getElementById("loginModal");
const closeModal = document.getElementById("closeModal");
const submitLogin = document.getElementById("submitLogin");
const loginError = document.getElementById("loginError");

// Show login modal
loginBtn.addEventListener("click", () => {
  loginModal.classList.remove("hidden");
});

// Close modal
document.getElementById("closeModal").addEventListener("click", () => {
  loginModal.classList.add("hidden");
  loginError.classList.add("hidden");
});

// Login check
submitLogin.addEventListener("click", () => {
  const username = document.getElementById("username").value.trim();
  const password = document.getElementById("password").value.trim();

  if (username === "admin" && password === "password123") {
    loginModal.classList.add("hidden");
    loginBtn.classList.add("hidden");
    logoutBtn.classList.remove("hidden");
    alert("Login successful!");
  } else {
    loginError.classList.remove("hidden");
  }
});

// Logout
logoutBtn.addEventListener("click", () => {
  loginBtn.classList.remove("hidden");
  logoutBtn.classList.add("hidden");
  alert("Logged out.");
});
