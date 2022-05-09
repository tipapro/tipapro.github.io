---
layout: default
---
<section class="container centered home">
    <div class="about">
        <img class="profile-img" src="{{ site.data.profile.profile_image }}" alt="Profile Picture">
        <h1>{{ site.data.profile.name }}</h1>
        <h2>{{ site.data.profile.whoiam }}</h2>
        <p>{{ site.data.profile.description }}</p>
        {% include common/icon_button_row.liquid content=site.data.profile.links size='large' %}
    </div>
</section>