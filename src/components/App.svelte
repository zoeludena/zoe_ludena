<script>
  import OneStar from './OneStar.svelte';
  import TwoStar from './TwoStar.svelte';
  import ThreeStar from './ThreeStar.svelte';
  import FourStar from './FourStar.svelte';
  import FiveStar from './FiveStar.svelte';

  import picture from '../lib/picture/IMG_4044.jpg';

  import { onMount } from 'svelte';
  import * as d3 from 'd3';

  export let message = "";
  export let x = 0;
  export let y = 0;
  export let visible = false;

  let tooltip;

  onMount(() => {
    tooltip = d3.select("#tooltip");
  });

  $: if (tooltip) {
    tooltip
      .style("left", `${x + 10}px`)
      .style("top", `${y + 10}px`)
      .style("visibility", visible ? "visible" : "hidden")
      .text(message);
  }
</script>

<main>
  <h1>Zoe Ludena</h1>
  <div class="container">
    <img src= {picture} alt="Picture of Zoe Ludena" class="circle-image">
  </div>
  <p id="centered-paragraph"><a href = "https://github.com/zoeludena">GitHub</a> | <a href = "https://www.linkedin.com/in/zoe-ludena-1906a2168/">LinkedIn</a></p>

  <div class="content">
    <h2>About Me!</h2>
    <p>Hello! 👋</p>
    <p>My name is Zoe Ludena! I am a rising fourth year at the University of California, San Diego. I am a part of the first and finest college, Revelle. My major is Data Science and my minor is Business Economics. I will be graduating Winter Quarter 2025.</p>
    <p>Currently, I work for the San Diego Sheriff Department and as a tutor for the Halıcıoğlu Data Science Institute. I am a tutor for Principles of Data Science in Summer Session One 2024. I have tutored for Principles of Data Science, Programming and Basic Data Structures for Data Science, Data Structures and Algorithms for Data Science, and Theoretical Foundations of Data Science I.</p>
    <p>In my free time I like to spent time with my family and friends, singing, and baking! 🍰</p>
  </div>

  <h2>Skills</h2>
  <div id="tooltip"></div>
  <ul class="skills-list">
    <li>Python <FiveStar /></li>
    <li>Pandas <FiveStar /></li>
    <li>NumPy <FiveStar /></li>
    <li>Scikit Learn <FourStar /></li>
    <li>Tableau <FourStar /></li>
    <li>SQL <FourStar /></li>
    <li>HTML <ThreeStar /></li>
    <li>JavaScript <TwoStar /></li>
    <li>Java <TwoStar /></li>
  </ul>

  <h2>Projects</h2>
  <ol>
    <li>Big O Explained | <a href = "https://github.com/anmarkova2223/big-o-scrolly">GitHub</a> | Mar 2024</li>
      <ul>
        <li>Big O Explained is an interactive visualization that aims to teach python coders about time complexity and Big O Notation.</li>
        <li>This was a group project for Introduction to Data Visualization.</li>
        <li>It was coded using JavaScript, D3, and HTML, just like this webpage!</li>
      </ul>
    <li>Interactive Income | <a href = "https://github.com/zoeludena/dsc106-Interactive-Income">GitHub</a> | Mar 2024</li>
      <ul>
        <li>Interactive Income is an interactive visualization that aims to explore the differences in income between males and females within different work groups.</li>
        <li>This was a group project for Introduction to Data Visualization.</li>
        <li>It was coded using JavaScript, D3, and HTML.</li>
      </ul>
    <li>League of Legends Model Building | <a href = "https://github.com/zoeludena/League-of-Legends-Model-Building">GitHub</a> | Jun 2023</li>
    <ul>
      <li>League of Legends Model Building displays creating a model, fairness analysis, and permutation testing.</li>
      <li>This was a pair-programming project for The Practice and Application of Data Science.</li>
      <li>It was coded using python and HTML.</li>
    </ul>
    <li>League of Legends Soul Analysis | <a href = "https://github.com/zoeludena/League-Of-Legends-Soul-Analysis">GitHub</a> | May 2023</li>
    <ul>
      <li>League of Legends Soul Analysis displays exploratory data analysis, assessing missingness, and permutation testing.</li>
      <li>This was a pair-programming project for The Practice and Application of Data Science.</li>
      <li>It was coded using python and HTML.</li>
    </ul>
    <li>SPISman | <a href = "https://replit.com/@zoeludena/spis21-project-Rena-Zoe">Replit</a> | Aug 2021</li>
    <ul>
      <li>SPISman is a version of Pacman that incorporated every tutor and professor inside the SPIS program.</li>
      <li>This was a pair-programming project for <a href = "https://spis.ucsd.edu/">SPIS</a>.</li>
      <li>Fun fact: This was the first thing I had ever coded using python!</li>
      <li>It was coded using python and pygame.</li>
    </ul>
  </ol>

</main>

<style>
  /* Write your CSS here */
  main {
      max-width: 1500px;
      margin: 20px auto;
      padding: 20px;
      /* background: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); */
      font-family: 'Trebuchet MS', sans-serif;
    }

  h1 {
      text-align: center;
      font-size: 2.5em;
      margin-bottom: 10px;
    }

    h2 {
      font-size: 1.75em;
      margin-top: 30px;
      border-bottom: 2px solid #333;
      padding-bottom: 10px;
    }
    
  p {
      margin: 10px 0;
      font-size: 1.3em;
      padding: 10px;
      /* background-color: #fafafa;
      border-left: 5px solid #333; */
    }
    ol {
      font-size: 1.3em;
      font-family: 'Trebuchet MS', sans-serif;
    }
    ol li {
    margin-bottom: 10px; /* Adjust margin between list items */
    }
    ul {
      font-size: 1.3em;
      font-family: 'Trebuchet MS', sans-serif;
    }
    ul li {
      font-size: .8em;
    }

    .skills-list {
      display: grid;
      grid-template-columns: repeat(3, 1fr); /* Creates three equal-width columns */
      gap: 20px; /* Adds spacing between columns */
      list-style-type: none; /* Removes default bullets */
    }

    .skills-list li {
      font-size: 1.1em;
      padding: 10px;
      text-align: center;
    }

    #centered-paragraph {
    text-align: center;
  }
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .circle-image {
    display: block;
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
    border: 2px solid #ccc;
  }

  @media (max-width: 600px) {
  .skills-list {
    grid-template-columns: 1fr;
    gap: 10px;
  }

  .skills-list li {
    font-size: 1em;
    padding: 10px;
    text-align: left;
  }

  main {
    padding: 10px;
  }

  h1 {
    font-size: 2em;
  }

  h2 {
    font-size: 1.5em;
  }

  p, ol, ul {
    font-size: 1em;
  }
}

#tooltip {
    position: absolute;
    background-color: #333;
    color: #fff;
    padding: 5px;
    border-radius: 5px;
    font-size: 0.8em;
    visibility: hidden;
    opacity: 0;
    transition: opacity 0.2s ease-in-out;
  }

  #tooltip.visible {
    opacity: 1;
  }

</style>
