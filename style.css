(() => {
  const revealEls = Array.from(document.querySelectorAll('.reveal'));

  if (!('IntersectionObserver' in window)) {
    revealEls.forEach(el => el.classList.add('show'));
    return;
  }

  const io = new IntersectionObserver(
    (entries) => {
      for (const entry of entries) {
        if (entry.isIntersecting) {
          entry.target.classList.add('show');
          io.unobserve(entry.target);
        }
      }
    },
    { threshold: 0.12, rootMargin: '0px 0px -10% 0px' }
  );

  revealEls.forEach(el => io.observe(el));
})();

