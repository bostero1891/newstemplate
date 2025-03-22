---
layout: deportes
title: Player
author: PEÑAROLPRESS 1891
---

  <video id="videoPlayer" controls width="100%"></video>
  <script>
    async function loadVideo() {
      const videoUrl = 'https://m140.uqload.net/3rfkw7xd4nwwhldqdks7vkvsde353t76jdgzurrrpzkltciptitus47p4rfa/v.mp4'; // Replace with the actual video URL
      const proxyUrl = `http://localhost:3000/my-video-proxy?url=${encodeURIComponent(videoUrl)}`;

      try {
        const response = await fetch(proxyUrl);
        if (!response.ok) {
          throw new Error('Network response was not ok');
        }
        const blob = await response.blob();
        const videoElement = document.getElementById('videoPlayer');
        videoElement.src = URL.createObjectURL(blob);
        videoElement.play();
      } catch (error) {
        console.error('Error fetching video:', error);
      }
    }

    loadVideo();
  </script>
