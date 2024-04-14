<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Wedding Event Planner</title>
  <link rel="stylesheet" href="styles.css">
  <style>
    .categories {
      display: flex;
    }
    .category {
      flex: 1;
      text-align: center;
      cursor: pointer;
    }
    .plans {
      display: flex;
      flex-wrap: wrap;
    }
    .service-card, .decoration-card, .food-item, .option {
      flex: 0 0 calc(33.33% - 20px);
      margin: 10px;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
  </style>
</head>
<body>

  <header>
    <h1>Wedding Event Planner</h1>
    <p>Your dream wedding awaits...</p>
  </header>

  <main>
    <section class="categories">
      <div class="category" onclick="showAllPlans('venue')">Venue Selection</div>
      <div class="category" onclick="showAllPlans('decoration')">Decoration</div>
      <div class="category" onclick="showAllPlans('catering')">Catering</div>
      <div class="category" onclick="showAllPlans('entertainment')">Entertainment</div>
      <div class="category" onclick="showAllPlans('lighting')">Lighting</div>
    </section>

    <section class="plans">
      <!-- Plans will be displayed here dynamically -->
    </section>
  </main>

  <footer>
    <p>&copy; 2024 Wedding Event Planner</p>
  </footer>

  <script>
    function showAllPlans(category) {
      const plansSection = document.querySelector('.plans');
      plansSection.innerHTML = ''; // Clear previous content

      // Create and append plan cards based on the selected category
      switch (category) {
        case 'venue':
          plansSection.innerHTML = `
            <div class="service-card">
              <h2>Outdoor Garden</h2>
              <p class="price">Starting from ₹50,000</p>
              <p>Enjoy your wedding amidst lush greenery and natural beauty.</p>
              <button class="select-plan">Select Plan</button>
            </div>
            <div class="service-card">
              <h2>Grand Ballroom</h2>
              <p class="price">Starting from ₹100,000</p>
              <p>Host a lavish reception in a spacious and elegant ballroom.</p>
              <button class="select-plan">Select Plan</button>
            </div>
            <div class="service-card">
              <h2>Beachfront Venue</h2>
              <p class="price">Starting from ₹150,000</p>
              <p>Exchange vows with the sound of waves as your backdrop.</p>
              <button class="select-plan">Select Plan</button>
            </div>
          `;
          break;
        case 'decoration':
          plansSection.innerHTML = `
            <div class="decoration-card">
              <h2>Classic Elegance</h2>
              <p class="price">₹10,000 - ₹20,000</p>
              <div class="image classic"></div>
              <ul>
                <li>Roses</li>
                <li>Lilies</li>
                <li>Carnations</li>
              </ul>
              <button class="select-plan">Select Plan</button>
            </div>
            <div class="decoration-card">
              <h2>Modern Chic</h2>
              <p class="price">₹1,20,000 - ₹1,30,000</p>
              <div class="image modern"></div>
              <ul>
                <li>Orchids</li>
                <li>Tulips</li>
                <li>Hydrangeas</li>
              </ul>
              <button class="select-plan">Select Plan</button>
            </div>
            <div class="decoration-card">
              <h2>Rustic Romance</h2>
              <p class="price">₹2,30,000 - ₹2,40,000</p>
              <div class="image rustic"></div>
              <ul>
                <li>Peonies</li>
                <li>Sunflowers</li>
                <li>Daisies</li>
              </ul>
              <button class="select-plan">Select Plan</button>
            </div>
            <div class="decoration-card">
              <h2>Luxurious Garden</h2>
              <p class="price">₹3,40,000 - ₹3,50,000</p>
              <div class="image luxurious-garden"></div>
              <ul>
                <li>Gardenias</li>
                <li>Hyacinths</li>
                <li>Calla Lilies</li>
              </ul>
              <button class="select-plan">Select Plan</button>
            </div>
          `;
          break;
        case 'catering':
          plansSection.innerHTML = `
            <div class="food-item">
              <h2>Indian Cuisine</h2>
              <p class="price">Starting from ₹300 per person</p>
              <img src="indian_cuisine.jpg" alt="Indian Cuisine">
              <p>Experience the rich flavors of traditional Indian dishes.</p>
              <button class="select-plan">Select Plan</button>
            </div>
            <div class="food-item">
              <h2>Italian Delights</h2>
              <p class="price">Starting from ₹400 per person</p>
              <img src="italian_delights.jpg" alt="Italian Delights">
              <p>Savor the taste of Italy with our authentic pasta and pizza.</p>
              <button class="select-plan">Select Plan</button>
            </div>
            <div class="food-item">
              <h2>Asian Fusion</h2>
              <p class="price">Starting from ₹350 per person</p>
              <img src="asian_fusion.jpg" alt="Asian Fusion">
              <p>Explore a blend of Asian flavors in our fusion cuisine.</p>
              <button class="select-plan">Select Plan</button>
            </div>
          `;
          break;
        case 'entertainment':
          plansSection.innerHTML = `
            <div class="option">
              <h2>DJ Services</h2>
              <p class="price">Starting from ₹10,000</p>
              <p>Get the party started with our professional DJs.</p>
              <button class="select-plan">Select Plan</button>
            </div>
            <div class="option">
              <h2>Live Band Performances</h2>
              <p class="price">Starting from ₹20,000</p>
              <p>Enjoy live music performances to enhance your event.</p>
              <button class="select-plan">Select Plan</button>
            </div>
            <div class="option">
              <h2>Magicians and Illusionists</h2>
              <p class="price">Starting from ₹15,000</p>
              <p>Add a touch of magic with mesmerizing illusions.</p>
              <button class="select-plan">Select Plan</button>
            </div>
          `;
          break;
        case 'lighting':
          plansSection.innerHTML = `
            <div class="option">
              <h2>LED Lights</h2>
              <p class="price">Starting from ₹15,000</p>
              <p>Add modern lighting with energy-efficient LED lights.</p>
              <button class="select-plan">Select Plan</button>
            </div>
            <div class="option">
              <h2>Fairy Lights</h2>
              <p class="price">Starting from ₹10,000</p>
              <p>Create a magical ambiance with twinkling fairy lights.</p>
              <button class="select-plan">Select Plan</button>
            </div>
            <div class="option">
              <h2>Spotlights and Uplighting</h2>
              <p class="price">Starting from ₹20,000</p>
              <p>Highlight key features of your venue with spotlights.</p>
              <button class="select-plan">Select Plan</button>
            </div>
          `;
          break;
        default:
          break;
      }
    }
  </script>
</body>
</html>
