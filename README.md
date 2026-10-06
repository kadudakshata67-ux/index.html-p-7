<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Interactive FAQ</title>

  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
</head>

<body class="bg-gray-100 min-h-screen">

  <!-- FAQ Section -->
  <section class="max-w-3xl mx-auto px-4 py-12">

    <!-- Heading -->
    <div class="text-center mb-8">
      <h1 class="text-4xl font-bold text-gray-800">
        Frequently Asked Questions
      </h1>

      <p class="text-gray-600 mt-3">
        Click on a question to view the answer.
      </p>
    </div>

    <!-- FAQ Container -->
    <div class="space-y-4">

      <!-- FAQ 1 -->
      <div class="faq-item bg-white rounded-lg shadow">

        <button
          class="faq-question w-full flex justify-between items-center
                 px-6 py-4 text-left font-semibold text-gray-800
                 hover:bg-gray-50"
        >
          <span>What is Tailwind CSS?</span>

          <span class="faq-icon text-2xl text-blue-600">
            +
          </span>
        </button>

        <div class="faq-answer hidden px-6 pb-4 text-gray-600">
          Tailwind CSS is a utility-first CSS framework that allows you
          to create modern and responsive websites using predefined
          utility classes.
        </div>

      </div>

      <!-- FAQ 2 -->
      <div class="faq-item bg-white rounded-lg shadow">

        <button
          class="faq-question w-full flex justify-between items-center
                 px-6 py-4 text-left font-semibold text-gray-800
                 hover:bg-gray-50"
        >
          <span>How does JavaScript work with HTML?</span>

          <span class="faq-icon text-2xl text-blue-600">
            +
          </span>
        </button>

        <div class="faq-answer hidden px-6 pb-4 text-gray-600">
          JavaScript can access and modify HTML elements through the DOM.
          It can also respond to user actions such as clicks and form
          submissions.
        </div>

      </div>

      <!-- FAQ 3 -->
      <div class="faq-item bg-white rounded-lg shadow">

        <button
          class="faq-question w-full flex justify-between items-center
                 px-6 py-4 text-left font-semibold text-gray-800
                 hover:bg-gray-50"
        >
          <span>Is Tailwind CSS responsive?</span>

          <span class="faq-icon text-2xl text-blue-600">
            +
          </span>
        </button>

        <div class="faq-answer hidden px-6 pb-4 text-gray-600">
          Yes. Tailwind CSS provides responsive utility prefixes such as
          sm, md, lg, xl, and 2xl for creating layouts that adapt to
          different screen sizes.
        </div>

      </div>

      <!-- FAQ 4 -->
      <div class="faq-item bg-white rounded-lg shadow">

        <button
          class="faq-question w-full flex justify-between items-center
                 px-6 py-4 text-left font-semibold text-gray-800
                 hover:bg-gray-50"
        >
          <span>Can I open multiple questions?</span>

          <span class="faq-icon text-2xl text-blue-600">
            +
          </span>
        </button>

        <div class="faq-answer hidden px-6 pb-4 text-gray-600">
          Yes. Each FAQ item works independently, so you can open multiple
          answers at the same time.
        </div>

      </div>

    </div>
  </section>


  <!-- JavaScript -->
  <script>

    // Select all FAQ questions
    const questions = document.querySelectorAll(".faq-question");

    // Add click event to every question
    questions.forEach(function(question) {

      question.addEventListener("click", function() {

        // Get the parent FAQ item
        const faqItem = question.parentElement;

        // Find answer and icon inside the current item
        const answer = faqItem.querySelector(".faq-answer");
        const icon = faqItem.querySelector(".faq-icon");

        // Show / hide answer
        answer.classList.toggle("hidden");

        // Change + to −
        if (answer.classList.contains("hidden")) {
          icon.textContent = "+";
        } else {
          icon.textContent = "−";
        }

      });

    });

  </script>

</body>
</html>
