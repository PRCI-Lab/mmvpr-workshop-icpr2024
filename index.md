---
layout: default
---
<style>
    body {
        font-family: Arial, sans-serif;
    }
    #navbar {
        background-color: #333;
        padding: 10px;
        position: fixed;
        top: 0;
        width: 100%;
        display: flex;
        justify-content: center;
        transition: top 0.5s;
        z-index: 1000;
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
        color: white;
        text-decoration: none;
        padding: 10px 20px;
        display: block;
    }

    #navbar a:hover {
        background-color: #575757;
        border-radius: 5px;
    }

    #navbar.hidden {
        top: -50px;
    }
    .section {
        padding: 60px 20px 0;
    }
</style>

<script>
    document.addEventListener('scroll', function() {
        const navbar = document.getElementById('navbar');
        if (window.scrollY > 50) {
            navbar.classList.add('hidden');
        } else {
            navbar.classList.remove('hidden');
        }
    });

    document.getElementById('navbar').addEventListener('mouseenter', function() {
        this.classList.remove('hidden');
    });

    document.getElementById('navbar').addEventListener('mouseleave', function() {
        if (window.scrollY > 50) {
            this.classList.add('hidden');
        }
    });
</script>

{% include navbar.html %}

The workshop on Multi-modal Visual Pattern Recognition aims to provide a comprehensive platform for researchers and practitioners to discuss recent advancements, challenges, and opportunities in the field of multi-modal visual pattern recognition. 

<div class="section" id="overview">
    ## **Overview**
    {% include_relative docs/overview.md %}
</div>

<div class="section" id="challenge">
    ## **Challenge**
    {% include_relative docs/challenge.md %}
</div>

<div class="section" id="details-of-the-challenge">
    ## **Details of the challenge**
    {% include_relative docs/details-of-the-challenge.md %}
</div>

<div class="section" id="important-dates">
    ## **Important Dates**
    {% include_relative docs/important-dates.md %}
</div>

<div class="section" id="organizing-committee">
    ## **Organizing Committee**
    {% include_relative docs/organizing-committee.md %}
</div>


