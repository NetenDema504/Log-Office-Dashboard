* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Segoe UI", sans-serif;
}

body {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #0078d4, #50c7f2);
}

.login-container {
  width: 100%;
  max-width: 380px;
  background: white;
  padding: 40px 30px;
  border-radius: 16px;
  box-shadow: 0 12px 30px rgba(0,0,0,0.15);
}

.logo {
  text-align: center;
  font-size: 33px;
  font-weight: 600;
  margin-bottom: 25px;
  color: #333;
}

.logo span {
  color: #42be31;
}

h2 {
  text-align: center;
  margin-bottom: 25px;
  font-weight: 500;
  color: #444;
}

.input-group {
  margin-bottom: 20px;
}

.input-group input {
  width: 100%;
  padding: 12px;
  border-radius: 8px;
  border: 1px solid #ccc;
  font-size: 14px;
  transition: 0.2s;
}

.input-group input:focus {
  border-color: #0078d4;
  outline: none;
  box-shadow: 0 0 0 2px rgba(0,120,212,0.2);
}

.login-btn {
  width: 100%;
  padding: 12px;
  background: #0078d4;
  border: none;
  border-radius: 8px;
  color: rgb(72, 78, 97);
  font-size: 15px;
  cursor: pointer;
  margin-top: 10px;
}

.login-btn:hover {
  background: #2a7ab7;
}

.divider {
  text-align: center;
  margin: 20px 0;
  font-size: 13px;
  color: #888;
}

.microsoft-btn {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  padding: 11px;
  border-radius: 8px;
  border: 1px solid #ccc;
  cursor: pointer;
  transition: 0.2s;
  background: #fff;
}

.microsoft-btn:hover {
  background: #f3f3f3;
}

.microsoft-btn img {
  width: 18px;
}

.footer {
  text-align: center;
  font-size: 12px;
  color: #777;
  margin-top: 15px;
}

@media (max-width: 420px) {
  .login-container {
    margin: 20px;
    padding: 30px;
  }
}
