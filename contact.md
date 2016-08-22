---
layout: page
title: Contact Me
permalink: /contact/
published: true
order: 5
---

<div class="container" id="contact">
        <div class="row">
          <div class="text-center">
            <p>If you have any questions please don't hesitate to ask, we will answer you within 24 hours, Monday - Friday!</p>

            <div class="inner contact">
              <!-- Form Area -->
              <div class="contact-form">
                <!-- Form -->
                <form id="contact-us">
                  <!-- Left Inputs -->
                  <div class="left-block">
                    <!-- Name -->
                    <input type="text" name="name" id="name" required="required" class="form" placeholder="Name">
                    <!-- Email -->
                    <input type="email" name="mail" id="mail" required="required" class="form" placeholder="Email">
                    <!-- Subject -->
                    <input type="number" name="phone-number" id="phone-number" required="required" class="form" placeholder="Phone Number">
                  </div><!-- End Left Inputs -->
                  <!-- Right Inputs -->
                  <div class="right-block">
                    <!-- Message -->
                    <textarea name="message" id="message" class="form textarea" placeholder="Message"></textarea>
                  </div><!-- End Right Inputs -->
                  <!-- Bottom Submit -->
                  <div class="submit-button">
                    <!-- Send Button -->
                    <button type="submit" id="submit" name="submit" class="form-btn semibold">Send Message</button> 
                  </div><!-- End Bottom Submit -->
                  <!-- Clear -->
                  <div class="clear"></div>
                </form>

              </div><!-- End Contact Form Area -->
            </div><!-- End Inner -->
            
          </div>
        </div>
      </div>
<script>
$("#contact-us").submit(function (e) {
        e.preventDefault();

        var formData = {
            "name": $('[name="name"]').val(),
            "number" : $('[name="phone-number"]').val(),
            "email" : $('[name="mail"]').val(),
            "message": $('[name="message"]').val()
        };
        window.location = "mailto:dhatripejavar18@gmail.com?subject=Contact Request on D'mod Journey" + "&body="+ formData.message + "%0D%0A%0D%0ARegards,%0D%0A" + formData.name + "%0D%0A" + formData.number + "%0D%0A" + formData.email;
    });
</script>