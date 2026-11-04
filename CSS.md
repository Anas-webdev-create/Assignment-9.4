* {
  box-sizing: border-box;
}

:root {
  --cream: #f8f5ed;
  --paper: #fffdf8;
  --green: #244638;
  --muted-green: #617568;
  --terracotta: #b96545;
  --line: #e5e0d5;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  color: var(--green);
  background: var(--cream);
  font-family: Arial, sans-serif;
  line-height: 1.6;
}

a {
  color: inherit;
  text-decoration: none;
}

.site-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
  padding: 20px 6%;
  border-bottom: 1px solid var(--line);
  background: var(--paper);
}

.logo {
  font-family: Georgia, "Times New Roman", serif;
  font-size: 1.55rem;
  font-weight: bold;
  letter-spacing: -0.04em;
  white-space: nowrap;
}

.logo span {
  color: var(--terracotta);
}

.main-nav {
  display: flex;
  align-items: center;
  gap: 28px;
}

.main-nav a,
.site-footer > a:last-child {
  color: var(--muted-green);
  font-size: 0.94rem;
}

.main-nav a:hover,
.site-footer > a:last-child:hover,
.text-link:hover {
  color: var(--terracotta);
}

.nav-cta,
.button {
  display: inline-block;
  padding: 11px 17px;
  border: 1px solid var(--green);
  border-radius: 4px;
  font-size: 0.9rem;
  font-weight: bold;
}

.nav-cta {
  background: transparent;
}

.hero {
  max-width: 1240px;
  margin: 0 auto;
  padding: 76px 6%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 56px;
}

.hero-copy {
  flex: 1 1 48%;
  max-width: 540px;
}

.eyebrow {
  margin: 0 0 12px;
  color: var(--terracotta);
  font-size: 0.76rem;
  font-weight: bold;
  letter-spacing: 0.14em;
  text-transform: uppercase;
}

.hero h1 {
  margin: 0;
  font-family: Georgia, "Times New Roman", serif;
  font-size: clamp(2.8rem, 5vw, 4.8rem);
  font-weight: normal;
  line-height: 1.04;
  letter-spacing: -0.045em;
}

.hero-description {
  max-width: 470px;
  margin: 22px 0 26px;
  color: var(--muted-green);
  font-size: 1.05rem;
}

.hero-actions {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 18px;
}

.button-primary {
  border-color: var(--green);
  background: var(--green);
  color: white;
}

.button-primary:hover {
  background: #345d49;
}

.text-link {
  color: var(--green);
  font-size: 0.95rem;
  font-weight: bold;
}

.text-link span {
  margin-left: 4px;
}

.hero-image-wrap {
  position: relative;
  flex: 1 1 48%;
  max-width: 570px;
}

.hero-image {
  display: block;
  width: 100%;
  height: 420px;
  border-radius: 48% 48% 4px 4px;
  background: #e4e8dc;
  object-fit: cover;
}

.image-caption {
  position: absolute;
  right: 16px;
  bottom: 14px;
  margin: 0;
  padding: 8px 12px;
  border-radius: 3px;
  background: var(--paper);
  color: var(--green);
  font-family: Georgia, "Times New Roman", serif;
  font-size: 0.9rem;
}

.benefits {
  padding: 62px 6% 72px;
  background: var(--paper);
}

.section-heading {
  max-width: 650px;
  margin: 0 auto 30px;
  text-align: center;
}

.section-heading h2 {
  margin: 0;
  font-family: Georgia, "Times New Roman", serif;
  font-size: clamp(2rem, 4vw, 3rem);
  font-weight: normal;
  line-height: 1.15;
}

.section-heading > p:last-child {
  margin: 10px 0 0;
  color: var(--muted-green);
}

.benefit-grid {
  max-width: 1120px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 20px;
}

.benefit-card {
  min-width: 0;
  padding: 24px;
  border: 1px solid var(--line);
  background: var(--cream);
}

.card-number {
  color: var(--terracotta);
  font-size: 0.8rem;
  font-weight: bold;
  letter-spacing: 0.1em;
}

.benefit-card h3 {
  margin: 18px 0 8px;
  font-family: Georgia, "Times New Roman", serif;
  font-size: 1.35rem;
}

.benefit-card p {
  margin: 0;
  color: var(--muted-green);
}

.site-footer {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  gap: 12px 24px;
  padding: 22px 6%;
  background: var(--green);
  color: white;
}

.footer-logo {
  font-size: 1.3rem;
}

.site-footer p {
  margin: 0;
  color: #d8e2d9;
  font-size: 0.9rem;
}

.site-footer > a:last-child {
  color: white;
}

@media (max-width: 760px) {
  .site-header {
    flex-wrap: wrap;
    justify-content: center;
    padding: 16px 5%;
  }

  .main-nav {
    order: 3;
    width: 100%;
    justify-content: center;
    gap: 20px;
  }

  .hero {
    flex-direction: column;
    align-items: stretch;
    gap: 32px;
    padding: 52px 6%;
  }

  .hero-copy,
  .hero-image-wrap {
    max-width: none;
  }

  .hero-image {
    height: 340px;
  }

  .benefit-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (max-width: 520px) {
  .site-header {
    gap: 12px;
  }

  .nav-cta {
    padding: 9px 12px;
    font-size: 0.82rem;
  }

  .main-nav {
    gap: 14px;
    font-size: 0.9rem;
  }

  .hero {
    padding: 40px 20px;
  }

  .hero h1 {
    font-size: clamp(2.5rem, 12vw, 3.6rem);
  }

  .hero-image {
    height: 270px;
    border-radius: 46% 46% 4px 4px;
  }

  .benefits {
    padding: 46px 20px;
  }

  .benefit-grid {
    grid-template-columns: minmax(0, 1fr);
    gap: 14px;
  }

  .site-footer {
    flex-direction: column;
    text-align: center;
  }
}