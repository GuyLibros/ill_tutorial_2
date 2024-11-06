# Welcome to My GitHub Page

<!-- Add Shepherd.js CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/shepherd.js@8.1.0/dist/css/shepherd.css">

<!-- Page Content -->
<h1 id="welcome">Welcome to My Page</h1>
<p id="description">This page is about...</p>

<!-- Add Shepherd.js JavaScript and tour script -->
<script src="https://cdn.jsdelivr.net/npm/shepherd.js@8.1.0/dist/js/shepherd.min.js"></script>
<script>
  document.addEventListener("DOMContentLoaded", function() {
    const tour = new Shepherd.Tour({
      defaultStepOptions: {
        cancelIcon: { enabled: true },
        scrollTo: { behavior: 'smooth', block: 'center' }
      }
    });

    tour.addStep({
      id: 'welcome-step',
      text: 'Welcome to the page!',
      attachTo: { element: '#welcome', on: 'bottom' },
      buttons: [{ text: 'Next', action: tour.next }]
    });

    tour.addStep({
      id: 'description-step',
      text: 'Here is what this page is about.',
      attachTo: { element: '#description', on: 'right' },
      buttons: [
        { text: 'Back', action: tour.back },
        { text: 'Finish', action: tour.complete }
      ]
    });

    tour.start();
  });
</script>
