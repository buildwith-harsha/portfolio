<template>
  <section class="section letters">
    <!-- Section label -->
    <p class="kicker">Letters to the Editor</p>

    <!-- Heading -->
    <h2 class="heading">Correspondence</h2>

    <!-- Dateline -->
    <p class="dateline">Chennai — Portfolio Edition</p>

    <!-- Editorial intro -->
    <p class="intro">
      Readers wishing to discuss collaboration, opportunities, or professional
      inquiry are invited to submit correspondence below.
    </p>

    <!-- Contact form -->
    <form class="contact-form">
      <label>
        <span>Name</span>
        <input type="text" placeholder="Your Name" />
      </label>

      <label>
        <span>Email</span>
        <input type="email" placeholder="you@example.com" />
      </label>

      <label>
        <span>Message</span>
        <textarea rows="4" placeholder="Your message"></textarea>
      </label>

      <button type="submit" class="submit-btn">
        Submit Letter
      </button>
    </form>
  </section>
</template>

<style scoped>
/* =========================
   SECTION SPACING
========================= */
.letters {
  padding: 80px 60px 140px;
  text-align: center;
}

/* =========================
   KICKER
========================= */
.kicker {
  font-size: 11px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--muted-ink);
  margin-bottom: 6px;
  font-family: var(--font-body);
}

/* =========================
   HEADING
========================= */
.heading {
  font-family: var(--font-heading);
  font-size: 32px;
  margin-bottom: 6px;
}

/* =========================
   DATELINE
========================= */
.dateline {
  font-size: 12px;
  font-style: italic;
  color: var(--muted-ink);
  margin-bottom: 24px;
}

/* =========================
   INTRO TEXT
========================= */
.intro {
  max-width: 520px;
  margin: 0 auto 40px;
  font-size: 14.5px;
  line-height: 1.7;
  color: var(--muted-ink);
  font-family: var(--font-body);
}

/* =========================
   FORM LAYOUT
========================= */
.contact-form {
  max-width: 360px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 18px;
  text-align: left;
}

/* =========================
   LABELS
========================= */
label span {
  display: block;
  font-size: 11px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  margin-bottom: 6px;
  font-family: var(--font-heading);
}

/* =========================
   INPUTS
========================= */
input,
textarea {
  width: 100%;
  padding: 9px 10px;
  font-family: var(--font-body);
  font-size: 13.5px;
  border: 1px solid var(--line);
  background: transparent;
  outline: none;
}

/* focus */
input:focus,
textarea:focus {
  border-color: var(--ink);
}

/* =========================
   BUTTON
========================= */
.submit-btn {
  margin-top: 14px;
  align-self: center;
  padding: 8px 24px;
  font-family: var(--font-heading);
  font-size: 12px;
  letter-spacing: 2px;
  text-transform: uppercase;
  background: transparent;
  color: var(--ink);
  border: 2px solid var(--ink);
  cursor: pointer;
}

/* hover */
.submit-btn:hover {
  background: var(--ink);
  color: var(--paper);
}

/* =========================
   RESPONSIVE
========================= */
@media (max-width: 480px) {
  .contact-form {
    width: 100%;
  }
}
</style>
