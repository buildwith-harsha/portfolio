<template>
  <section class="section contact letters">
    <!-- Section label -->
    <p class="kicker">Letters</p>

    <!-- Heading -->
    <h2 class="heading">Contact</h2>

    <!-- Editorial intro -->
    <p class="intro">
      Interested in collaboration, opportunities, or just a thoughtful
      conversation? Write in.
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
        Send Letter
      </button>
    </form>
  </section>
</template>

<script setup>
</script>

<style scoped>
/* Section spacing */
.letters {
  padding: 80px 60px 140px;
  text-align: center;
}

/* Small editorial label */
.kicker {
  font-size: 12px;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--muted-ink);
  margin-bottom: 10px;
  font-family: var(--font-body);
}

/* Intro text */
.intro {
  max-width: 520px;
  margin: 20px auto 40px;
  font-size: 15px;
  line-height: 1.6;
  color: var(--muted-ink);
  font-family: var(--font-body);
}

/* Form layout */
.contact-form {
  max-width: 360px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 18px;
  text-align: left;
}

/* Labels */
label span {
  display: block;
  font-size: 12px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  margin-bottom: 6px;
  font-family: var(--font-heading);
}

/* Inputs */
input,
textarea {
  width: 100%;
  padding: 10px 12px;
  font-family: var(--font-body);
  font-size: 14px;
  border: 1px solid var(--line);
  background: transparent;
  outline: none;
}

/* Focus style */
input:focus,
textarea:focus {
  border-color: var(--ink);
}

/* Submit button */
.submit-btn {
  margin-top: 10px;
  align-self: center;
  padding: 10px 26px;
  font-family: var(--font-heading);
  font-size: 13px;
  letter-spacing: 2px;
  text-transform: uppercase;
  background: var(--ink);
  color: var(--paper);
  border: none;
  cursor: pointer;
}

/* Hover */
.submit-btn:hover {
  opacity: 0.9;
}

/* Responsive */
@media (max-width: 480px) {
  .contact-form {
    width: 100%;
  }
}
</style>
