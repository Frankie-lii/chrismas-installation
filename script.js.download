// JavaScript for the Updated Website

document.addEventListener("DOMContentLoaded", () => {
    // Smooth Scroll for Navigation Links
    const navLinks = document.querySelectorAll("nav ul li a");
    navLinks.forEach(link => {
        link.addEventListener("click", event => {
            event.preventDefault();
            const targetId = event.target.getAttribute("href").slice(1);
            const targetElement = document.getElementById(targetId);
            targetElement.scrollIntoView({ behavior: "smooth" });
        });
    });

    // Form Validation for Booking and Contact Forms
    const forms = document.querySelectorAll(".booking-form, .contact-form");
    forms.forEach(form => {
        form.addEventListener("submit", event => {
            event.preventDefault();
            const inputs = form.querySelectorAll("input, textarea");
            let isValid = true;

            inputs.forEach(input => {
                if (!input.value.trim()) {
                    input.classList.add("error");
                    isValid = false;
                } else {
                    input.classList.remove("error");
                }
            });

            if (isValid) {
                alert("Your form has been submitted successfully!");
                form.reset(); // Clear the form
            } else {
                alert("Please fill in all the required fields.");
            }
        });
    });

    // Gallery Image Lightbox Effect
    const galleryImages = document.querySelectorAll(".gallery-item img");
    const lightbox = document.createElement("div");
    lightbox.id = "lightbox";
    document.body.appendChild(lightbox);

    galleryImages.forEach(image => {
        image.addEventListener("click", () => {
            lightbox.classList.add("active");
            const img = document.createElement("img");
            img.src = image.src;
            while (lightbox.firstChild) {
                lightbox.removeChild(lightbox.firstChild);
            }
            lightbox.appendChild(img);
        });
    });

    lightbox.addEventListener("click", () => {
        lightbox.classList.remove("active");
    });

    // Testimonial Hover Animation
    const testimonials = document.querySelectorAll(".testimonial-item");
    testimonials.forEach(item => {
        item.addEventListener("mouseover", () => {
            item.style.transform = "scale(1.05)";
            item.style.transition = "transform 0.3s ease";
        });
        item.addEventListener("mouseout", () => {
            item.style.transform = "scale(1)";
        });
    });

    // Header Scroll Effect
    const header = document.querySelector("header");
    window.addEventListener("scroll", () => {
        if (window.scrollY > 50) {
            header.classList.add("scrolled");
        } else {
            header.classList.remove("scrolled");
        }
    });

    // Responsive Navbar Toggle
    const burgerMenu = document.querySelector(".burger-menu");
    const navMenu = document.querySelector("nav ul");
    burgerMenu.addEventListener("click", () => {
        navMenu.classList.toggle("active");
        burgerMenu.classList.toggle("active");
    });

    // Dynamic Year in Footer
    const yearElement = document.querySelector(".year");
    if (yearElement) {
        const currentYear = new Date().getFullYear();
        yearElement.textContent = currentYear;
    }
});