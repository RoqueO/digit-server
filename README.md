<!-- Improved compatibility of back to top link: See: https://github.com/pull/73 -->
<a name="readme-top"></a>

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]


<!-- PROJECT LOGO AND TITLE -->
<p align="center">
  <a href="https://github.com/username/Project-Name">
    <img src="images/logo.png" alt="Logo" width="100" height="100">
  </a>

  <h2 align="center">Digit Server Docker Compose</h2>
  <p align="center">
    Docker compose script for digit server providing nginx, qbittorent, home assistant and portainer.
    <br />
    <a href="https://github.com/username/Project-Name"><strong>Check the Documentation »</strong></a>
    <br />
    <a href="https://github.com/username/Project-Name">View a Live Demo</a>
    •
    <a href="https://github.com/username/Project-Name/issues/new?template=bug_report.md">Report a Bug</a>
    •
    <a href="https://github.com/username/Project-Name/issues/new?template=feature_request.md">Request a Feature</a>
  </p>
</p>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about">About This Project</a></li>
    <li><a href="#start">Getting Started</a></li>
    <li><a href="#use">Usage Guidelines</a></li>
    <li><a href="#roadmap-section">Project Roadmap</a></li>
    <li><a href="#contrib-section">Contribution Guidelines</a></li>
    <li><a href="#license-section">License Information</a></li>
    <li><a href="#contact-section">Contact Details</a></li>
    <li><a href="#thanks">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## <a name="about"></a>About This Project

![Project Screenshot][project-image]

This is the docker compose configuration file for the digit server.  
It features the following docker based services:
- Portainer for docker container management
- Home Assistant for home automation controller
- QBittorent for torrenting - The torrent server utilizes VLAN 20 which is configured in my network to utilize PIA VPN on my PFSense router
- Nginx as a reverse proxy.

Network-wise:
- Portainer, Home Assistant and Nginx use the default brdige provided by docker
- QBittorent uses an:
    - vlan bridge to tag frames on pfsense so that they can be sent out pia vpn interface
    - internal bridge so that nginx can provide reverse proxy services

[🔝 Back to Top](#readme-top-anchor)

<!-- GETTING STARTED -->
## <a name="start"></a>Getting Started

To get the project up and running on your local system, follow these steps:

### Setting up:

* Use docker compose to launch the script:

  ```bash
  docker compose up -d
  ````

### Accessing the services:

Launch a web browser and point it to:
- digit.eclipsehome.lan/portainer
- digit.eclipsehome.lan/qbittorent
- digit.eclipsehome.lan/homeassistant

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 