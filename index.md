---
layout: default
---
<style>
    #navbar {
        background-color: rgba(255, 255, 255, 0.8);
        padding: 10px;
        box-sizing: border-box;
        position: fixed;
        top: 0;
        left: 0; 
        right: 0;
        width: 100%;
        display: flex;
        justify-content: center;
        transition: top 0.5s;
        z-index: 1000;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    #navbar ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        display: flex;
    }

    #navbar li {
        margin: 0 20px;
    }

    #navbar a {
        color: #333;
        text-decoration: none;
        padding: 10px 20px;
        display: block;
    }

    #navbar a:hover {
        background-color: rgba(240, 240, 240, 0.8);
        border-radius: 5px;
    }

    #navbar.hidden {
        top: -80px;
    }

    .content { 
        margin-top: 60px; 
    }
    #back-to-top {
            display: none;
            position: fixed;
            bottom: 30px; 
            right: 30px; 
            background-color: rgba(240, 240, 240, 0.8);
            color: #333;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            z-index: 1000;
        }
        #back-to-top:hover {
            background-color: rgba(240, 240, 240, 0.8);
        }
        .navbar-placeholder {
        height: 60px;
    }

/*   @media screen and (max-width: 1440px) {
    body {
      padding: 10px;
    }

    .site-header, .site-footer {
      padding: 1.5rem;
    }

    .page {
      padding: 1.5rem;
    }

    .image-container {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
      margin-top: 20px; 
    }

    .image-wrapper {
        max-width: 300px;
    }

.image-wrapper img {
  width: 100%;
  height: auto;
  display: block;
}

    #navbar {
      flex-direction: column;
      align-items: stretch;
    }

    #navbar ul {
      flex-direction: column;
    }

    #navbar li {
      margin: 5px 0;
    }

    #navbar a {
      text-align: center;
      padding: 15px 0;
    }
  }

  @media screen and (max-width: 768px) {    
    #navbar {
      flex-direction: column;
      align-items: center;
    }

    #navbar li {
      margin: 5px 0;
    }
  }

  @media screen and (max-width: 480px) {  
    #navbar {
      flex-direction: column;
      align-items: stretch;
    }
    #navbar ul {
      flex-direction: column;
    }
    #navbar li {
      margin: 0;
      width: 100%;
    }

    #navbar a {
      text-align: center;
      padding: 15px 0;
    }
  }

  @media screen and (min-width: 2000px) {
    #navbar {
      flex-direction: row;
      padding: 20px;
    }

    #navbar li {
      margin: 0 20px;
    }

    #navbar a {
      padding: 15px 20px;
    }
  } */
</style>

<button id="back-to-top"> Top </button>

<script>
    document.addEventListener('scroll', function() {
        const navbar = document.getElementById('navbar');
        if (window.scrollY > 50) {
            navbar.classList.add('hidden');
        } else {
            navbar.classList.remove('hidden');
        }
    });

    document.addEventListener('DOMContentLoaded', function() {
        const navbar = document.getElementById('navbar');
        navbar.addEventListener('mouseenter', function() {
            navbar.classList.remove('hidden');
        });

        navbar.addEventListener('mouseleave', function() {
            if (window.scrollY > 50) {
                navbar.classList.add('hidden');
            }
        });
    });

    var backToTopButton = document.getElementById("back-to-top");
    window.addEventListener("scroll", function() {
        if (window.scrollY > 300) {
            backToTopButton.style.display = "block";
        } else {
            backToTopButton.style.display = "none";
        }
    });
    backToTopButton.addEventListener("click", function() {
        window.scrollTo({
            top: 0,
            behavior: "smooth"
        });
    });
</script>

<div id="navbar" class="hidden">
    <ul>
        <li><a href="#overview">Overview</a></li>
        <li><a href="#challenge">Challenge</a></li>
        <li><a href="#details-of-the-challenge">Details</a></li>
        <li><a href="#important-dates">Important Dates</a></li>
        <li><a href="#organizing-committee">Organizing Committee</a></li>
    </ul>
</div>
<!-- <div class="navbar-placeholder"></div> -->

<div class="image-container">
  <div class="image-wrapper">
    <img src="/figs/icon/MMVPR-logo.png" alt="MMVPR">
  </div>
  <div class="image-wrapper">
    <img src="./figs/icon/icon.png" alt="ICPR">
  </div>
</div>

The workshop on Multi-Modal Visual Pattern Recognition aims to provide a comprehensive platform for researchers and practitioners to discuss recent advancements, challenges, and opportunities in the field of multi-modal visual pattern recognition. The workshop is held in conjunction with the 27th [International Conference on Pattern Recognition (ICPR 2024)](https://icpr2024.org/).



## **Overview**
{% include_relative docs/overview.md %}

## **Challenge**
{% include_relative docs/challenge.md %}

## **Details of the challenge**
{% include_relative docs/details-of-the-challenge.md %}

## **Important Dates**
{% include_relative docs/important-dates.md %}

## **Organizing Committee**
{% include_relative docs/organizing-committee.md %}

## **Challenge Group**
{% include_relative docs/challenge-group.md %}

