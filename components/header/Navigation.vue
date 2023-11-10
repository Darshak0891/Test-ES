<template>
  <ul class="mainmenu">
    <li><NuxtLink to="/">Home</NuxtLink></li>
    <li><NuxtLink to="/about-us-three">About Us</NuxtLink></li>
    <li class="has-droupdown">
      <NuxtLink to="">Blog</NuxtLink>
      <ul class="submenu">
        <li><NuxtLink to="/blog/blog-masonry">Blog</NuxtLink></li>
        <li><NuxtLink to="/blog/blog-details">Blog Details</NuxtLink></li>
      </ul>
    </li>
    <li class="has-droupdown">
      <NuxtLink to="">Case Study</NuxtLink>
      <ul class="submenu">
        <li><NuxtLink to="/course/course-two">Case Study</NuxtLink></li>
        <li>
          <NuxtLink to="/course/course-details-2">Case Study Detail</NuxtLink>
        </li>
      </ul>
    </li>

    <li class="has-droupdown">
      <NuxtLink to="">Pages</NuxtLink>
      <ul class="submenu">
        <li>
          <NuxtLink to="/instructor/instructor-one">Our Client</NuxtLink>
        </li>
        <li><NuxtLink to="/gallery-grid">Gallery</NuxtLink></li>
        <li>
          <NuxtLink to="/instructor/instructor-three">Service</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/instructor/instructor-two">Our Team</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/blog/blog-standard">Certificate</NuxtLink>
        </li>
      </ul>
    </li>

    <li><NuxtLink to="/contact-us">Contact Us</NuxtLink></li>
    <li><NuxtLink to="/contact-me">Career</NuxtLink></li>
  </ul>
</template>
