---
layout: default
---
<style>
    #navbar {
        background-color: white;
        padding: 10px;
        position: fixed;
        top: 0;
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
        background-color: #f0f0f0;
        border-radius: 5px;
    }

    #navbar.hidden {
        top: -80px;
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

The workshop on Multi-modal Visual Pattern Recognition aims to provide a comprehensive platform for researchers and practitioners to discuss recent advancements, challenges, and opportunities in the field of multi-modal visual pattern recognition. 

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

