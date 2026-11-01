@import "tailwindcss";

:root {
  font-family: Inter, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  line-height: 1.5;
  font-weight: 400;
  color: #ecf3ff;
  background: #07111f;
  font-synthesis: none;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

* {
  box-sizing: border-box;
}

html, body, #root {
  margin: 0;
  min-height: 100%;
  min-height: 100vh;
}

body {
  min-height: 100vh;
  background:
    radial-gradient(circle at top, rgba(51, 128, 255, 0.22), transparent 35%),
    linear-gradient(135deg, #07111f 0%, #0d1e34 50%, #07111f 100%);
}

button,
input {
  font: inherit;
}

.app-shell {
  min-height: 100vh;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
  padding: 2rem;
}

.panel {
  background: rgba(11, 22, 36, 0.8);
  border: 1px solid rgba(164, 192, 255, 0.2);
  border-radius: 20px;
  padding: 1.5rem;
  box-shadow: 0 18px 40px rgba(3, 9, 15, 0.45);
  backdrop-filter: blur(8px);
}

.panel-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  margin-bottom: 1rem;
}

.eyebrow {
  margin: 0 0 0.25rem;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  font-size: 0.72rem;
  color: #7cc7ff;
}

h1,
h2 {
  margin: 0;
  color: #f4f7ff;
}

.auth-form,
.score-box {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.auth-form {
  margin-top: 1rem;
}

label {
  display: flex;
  flex-direction: column;
  gap: 0.55rem;
  font-size: 0.95rem;
  color: #dfeaff;
}

input {
  border: 1px solid rgba(160, 184, 255, 0.28);
  border-radius: 12px;
  background: rgba(12, 25, 39, 0.9);
  color: #eff7ff;
  padding: 0.8rem 0.9rem;
  width: 100%;
}

input:focus {
  outline: 2px solid rgba(99, 179, 255, 0.9);
  outline-offset: 1px;
}

.primary-btn,
.secondary-btn,
.tab {
  border: none;
  border-radius: 12px;
  padding: 0.8rem 1rem;
  cursor: pointer;
  transition: transform 0.2s ease, opacity 0.2s ease;
}

.primary-btn:hover,
.secondary-btn:hover,
.tab:hover {
  transform: translateY(-1px);
}

.primary-btn {
  background: linear-gradient(135deg, #66b3ff 0%, #2a7dff 100%);
  color: #05111a;
  font-weight: 700;
}

.secondary-btn {
  background: rgba(141, 170, 255, 0.15);
  color: #edf5ff;
  border: 1px solid rgba(141, 170, 255, 0.25);
}

.mode-toggle {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.5rem;
  margin-bottom: 0.5rem;
}

.tab {
  background: rgba(141, 170, 255, 0.08);
  color: #dfeaff;
  border: 1px solid transparent;
}

.tab.active {
  background: rgba(102, 179, 255, 0.22);
  border-color: rgba(102, 179, 255, 0.6);
}

.score-box {
  margin-top: 1rem;
  padding-top: 1rem;
  border-top: 1px solid rgba(160, 184, 255, 0.18);
}

.label {
  margin: 0 0 0.25rem;
  color: #a8c5ff;
  font-size: 0.74rem;
  text-transform: uppercase;
  letter-spacing: 0.08em;
}

.score-input-row {
  display: flex;
  gap: 0.75rem;
}

.status-box,
.notice,
.empty-state {
  margin-top: 1rem;
  border-radius: 12px;
  padding: 0.9rem 1rem;
  background: rgba(102, 179, 255, 0.08);
  border: 1px solid rgba(102, 179, 255, 0.18);
  color: #dfeeff;
}

.notice.warning {
  background: rgba(255, 192, 73, 0.12);
  border-color: rgba(255, 192, 73, 0.24);
  color: #ffeba1;
}

.leaderboard-list {
  display: flex;
  flex-direction: column;
  gap: 0.65rem;
  margin-top: 0.75rem;
}

.leaderboard-row {
  display: grid;
  grid-template-columns: 60px 1fr auto;
  gap: 0.75rem;
  align-items: center;
  padding: 0.8rem 0.9rem;
  background: rgba(18, 31, 49, 0.9);
  border-radius: 12px;
  border: 1px solid rgba(164, 192, 255, 0.12);
}

.rank {
  color: #7cc7ff;
  font-weight: 700;
}

.name {
  font-weight: 600;
}

.score {
  color: #ffd76b;
  font-weight: 700;
}

@media (max-width: 900px) {
  .app-shell {
    grid-template-columns: 1fr;
    padding: 1rem;
  }

  .panel {
    padding: 1rem;
  }
}
