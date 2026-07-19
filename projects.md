---
layout: default
title: Projects
permalink: /projects/
---

<article class="projects-grid">
  <section class="project-item">
    <div class="project-orbit orbit-raft" aria-hidden="true"><span></span><span></span><span></span></div>
    <p class="project-category">Distributed Systems</p>
    <h2>Raft Consensus Algorithm</h2>
    <p class="project-stack">Python · Multithreading</p>
    <p class="project-summary">Implementation of the Raft leader election and consensus algorithm. Developed a robust system to handle node failures and maintain a consistent log across a distributed cluster.</p>
    <p class="project-actions"><a href="https://github.com/kevkjun" target="_blank" rel="noopener">GitHub <span aria-hidden="true">↗</span></a></p>
  </section>

  <section class="project-item">
    <div class="project-orbit orbit-numba" aria-hidden="true"><span></span><span></span><span></span></div>
    <p class="project-category">High Performance Computing</p>
    <h2>Smith-Waterman on Numba</h2>
    <p class="project-stack">Numba · CUDA · Python</p>
    <p class="project-summary">Optimized the Smith-Waterman sequence alignment algorithm using Numba for both CPU and GPU execution. Achieved significant speedup through parallelization and memory management on CUDA-enabled hardware.</p>
    <p class="project-actions"><a href="https://github.com/kevkjun/smith-waterman-numba" target="_blank" rel="noopener">GitHub <span aria-hidden="true">↗</span></a><a href="{{ site.baseurl }}/images/SWNumbaPresentation.pdf" target="_blank">Results <span aria-hidden="true">↗</span></a></p>
  </section>

  <section class="project-item">
    <div class="project-orbit orbit-cache" aria-hidden="true"><span></span><span></span></div>
    <p class="project-category">Computer Architecture</p>
    <h2>Cache Emulator</h2>
    <p class="project-stack">Java</p>
    <p class="project-summary">Emulation of CPU, RAM, and L1 Cache interactions. Validated performance using daxpy, matrix multiplication, and blocked matrix multiplication algorithms to analyze cache hit/miss ratios.</p>
    <p class="project-actions"><a href="https://github.com/kevkjun/CacheEmulator" target="_blank" rel="noopener">GitHub <span aria-hidden="true">↗</span></a></p>
  </section>

  <section class="project-item">
    <div class="project-orbit orbit-prime" aria-hidden="true"><span></span><span></span><span></span></div>
    <p class="project-category">Systems Programming</p>
    <h2>Mersenne Prime Scanner</h2>
    <p class="project-stack">MIPS Assembly · C</p>
    <p class="project-summary">Low-level implementation of a scanner to find Mersenne primes. Compared efficiency between MIPS assembly and C implementations to explore hardware-level optimizations.</p>
    <p class="project-actions"><a href="https://github.com/kevkjun/MIPS-MersenneScan" target="_blank" rel="noopener">GitHub <span aria-hidden="true">↗</span></a></p>
  </section>
</article>
