---
layout: page
title: Resume
tags: [about, Jekyll, theme, responsive]
modified: 
comments: true
---

<button id="downloadResumeBtn">Download Resume</button>

<div id="resumeModal" style="display: none;">
  <iframe src="/reports/Kundan_Kumar_Fall2023_Resume.docx.pdf" width="100%" height="600px"></iframe>
</div>

*Updated: Nov 12, 2023*

<script>
  document.getElementById("downloadResumeBtn").addEventListener("click", function() {
    document.getElementById("resumeModal").style.display = "block";
  });
</script>
