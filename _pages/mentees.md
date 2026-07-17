---
layout: archive
title: ""
permalink: /mentees/
author_profile: true
---

<style>
/* Mentorship Section Base Styling */
.mentorship-section {
    max-width: 800px;
    margin: 40px auto;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    color: #333;
    line-height: 1.6;
}

.philosophy {
    font-style: italic;
    color: #666;
    margin-bottom: 30px;
}

/* Mentee Card Structure */
.mentee-card {
    background: #ffffff;
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    padding: 24px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.05);
    margin-bottom: 25px;
}

.mentee-header {
    border-bottom: 2px solid #f0f2f5;
    padding-bottom: 16px;
    margin-bottom: 20px;
}

.mentee-meta h3 {
    margin: 0 0 6px 0;
    font-size: 1.4rem;
    color: #0366d6; /* Academic Blue */
}

.institution {
    margin: 0 0 12px 0;
    color: #586069;
    font-weight: 500;
}

/* Timeline Badges */
.timeline-badges {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
}

.badge {
    font-size: 0.8rem;
    padding: 4px 10px;
    border-radius: 12px;
    font-weight: 600;
}

.badge.active {
    background-color: #e2f0fe;
    color: #0366d6;
}

.badge.alumni {
    background-color: #f1f8ed;
    color: #28a745;
}

/* Body Content Elements */
.research-focus h4, 
.mentee-awards h4, 
.mentee-publications h4 {
    margin: 20px 0 8px 0;
    font-size: 1.1rem;
    color: #24292e;
}

.thesis-title {
    font-weight: 600;
    color: #444;
    padding-left: 8px;
    border-left: 3px solid #0366d6;
}

/* Lists */
.mentee-awards ul, 
.pub-list {
    margin: 0;
    padding-left: 20px;
}

.pub-subheading {
    margin: 12px 0 6px 0;
    font-size: 0.95rem;
    color: #6a737d;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

.pub-list li, .mentee-awards li {
    margin-bottom: 8px;
    font-size: 0.95rem;
}

/* Testimonial Box Styling */
.mentee-testimonial {
    background-color: #f8f9fa;
    border-left: 4px solid #6f42c1; /* Distinct deep purple highlight */
    padding: 16px;
    margin-top: 25px;
    position: relative;
    border-radius: 0 8px 8px 0;
}

.quote-icon {
    position: absolute;
    top: -5px;
    left: 10px;
    font-size: 3rem;
    color: #e1e4e8;
    line-height: 1;
    font-family: serif;
}

.quote-text {
    margin: 0 0 10px 0;
    font-style: italic;
    color: #4a5568;
    position: relative;
    z-index: 1;
}

.quote-source {
    margin: 0;
    font-size: 0.85rem;
    color: #718096;
    font-weight: 600;
    text-align: right;
}

/* Hide default summary arrow in all browsers */
.mentee-details summary {
    list-style: none;
}
.mentee-details summary::-webkit-details-marker {
    display: none;
}

/* Styled Dropdown Toggle Button */
.toggle-btn {
    display: inline-block;
    padding: 8px 16px;
    font-size: 0.85rem;
    font-weight: 600;
    color: #0366d6;
    background-color: #f6f8fa;
    border: 1px solid #d1d5da;
    border-radius: 6px;
    cursor: pointer;
    user-select: none;
    transition: background-color 0.2s ease;
}

.toggle-btn:hover {
    background-color: #f3f4f6;
    border-color: #0366d6;
}

/* Magic switch behavior for text when open vs closed */
.mentee-details[open] .btn-text-show {
    display: none;
}
.mentee-details:not([open]) .btn-text-hide {
    display: none;
}

/* Content spacing inside the open drawer */
.mentee-body {
    padding-top: 15px;
    animation: slideDown 0.3s ease-out; /* Smooth entrance */
}

@keyframes slideDown {
    from { opacity: 0; transform: translateY(-5px); }
    to { opacity: 1; transform: translateY(0); }
}


/* Align Name and Scholar Link side-by-side */
.name-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 10px;
    margin-bottom: 6px;
}

.name-row h3 {
    margin: 0 !important;
}

/* Scholar Link Button styling */
.scholar-link {
    display: inline-flex;
    align-items: center;
    gap: 4px;
    font-size: 0.85rem;
    color: #4a5568;
    text-decoration: none;
    padding: 2px 8px;
    border: 1px solid #e2e8f0;
    border-radius: 4px;
    background: #f8fafc;
    transition: all 0.2s ease;
}

.scholar-link:hover {
    color: #0366d6;
    border-color: #0366d6;
    background: #e2f0fe;
}

.scholar-icon {
    width: 14px;
    height: 14px;
    fill: currentColor;
}

/* Research Interest Specific Badges */
.badge.tag-security {
    background-color: #fff3cd;
    color: #856404;
}

.badge.tag-vision {
    background-color: #e1f5fe;
    color: #01579b;
}

.badge.tag-comm {
    background-color: #f3e5f5;
    color: #4a148c;
}

</style>

<section id="mentorship" class="mentorship-section">
    <h2>Mentorship & Academic Guidance</h2>
    <p class="philosophy">
        Guiding the next generation of researchers by advancing core techniques in secure image retrieval and computer vision, 
        as well as translating deep learning frameworks to solve cross-disciplinary engineering challenges.
    </p>

    <!-- Mentee Card 1: Md. Shahriar Uzzal -->
    <div class="mentee-card">
        <div class="mentee-header">
            <div class="mentee-meta">
                <div class="name-row">
                    <h3>Md. Shahriar Uzzal</h3>
                    <!-- Google Scholar Link Anchor -->
                    <a href="https://scholar.google.com/citations?user=NhOePDEAAAAJ&hl=en" target="_blank" class="scholar-link" title="Google Scholar Profile">
                        <svg class="scholar-icon" viewBox="0 0 24 24"><path d="M12 2L1 21h22L12 2zm0 4l7.5 13h-15L12 6z"/></svg> Scholar
                    </a>
                </div>
                <p class="institution">Department of Computer Engineering, Chosun University</p>
                <div class="timeline-badges">
                    <span class="badge active">Ph.D. Candidate (2026 — Present)</span>
                    <span class="badge alumni">M.S. Alumnus (2024 — 2026)</span>
                    <!-- Research Interest Tag -->
                    <span class="badge tag-security">🔐 Secure Image Retrieval</span>
                </div>
            </div>
        </div>

        <details class="mentee-details">
            <summary class="toggle-btn">
                <span class="btn-text-show">✨ View Full Research, Awards & Testimonial</span>
                <span class="btn-text-hide">✨ Hide Details</span>
            </summary>
            
            <div class="mentee-body">
                <div class="research-focus">
                    <h4>Master's Thesis</h4>
                    <p class="thesis-title">"Secure Content-based Image Retrieval with Perceptual Encryption"</p>
                </div>

                <div class="mentee-awards">
                    <h4>🏆 Awards & Recognition</h4>
                    <ul>
                        <li><strong>NOLTA Student Paper Award (2025)</strong> – IEICE NOLTA Conference</li>
                        <li><strong>KINGPC Best Paper Award (2025)</strong> – KINGPC Spring Conference</li>
                        <li><strong>KICS Excellent Paper Award (2024)</strong> – KICS Korea AI Conference</li>
                    </ul>
                </div>

                <div class="mentee-publications">
                    <h4>📚 Joint Publications</h4>
                    <h5 class="pub-subheading">International Journals</h5>
                    <ul class="pub-list">
                        <li>M.S. Uzzal, <strong>I. Ahmad</strong>, and S. Shin. "SCBIR-PE: Secure Content-based Image Retrieval with Perceptual Encryption." <em>IEEE Transactions on Dependable and Secure Computing</em>, 2025.</li>
                    </ul>

                    <h5 class="pub-subheading">International Conferences</h5>
                    <ul class="pub-list">
                        <li>M.S. Uzzal, <strong>I. Ahmad</strong>, and S. Shin. "Chaos Theory-Based Secure Image Retrieval with Fuzzy Color and Texture Feature Fusion." <em>APSIPA ASC</em>, 2026.</li>
                        <li>M.S. Uzzal, <strong>I. Ahmad</strong>, and S. Shin. "A Fast and Secure Content-based Image Retrieval Scheme using Clustering and Searchable Encryption." <em>IEEE ICOIN</em>, 2026.</li>
                        <li>M.S. Uzzal, <strong>I. Ahmad</strong>, and S. Shin. "Chaos-based Searchable Encryption Scheme for Secure Medical Image Retrieval using Edge Histogram Descriptor." <em>IEICE NOLTA</em>, 2025.</li>
                        <li>M.S. Uzzal, <strong>I. Ahmad</strong>, and S. Shin. "Perceptual Encryption-based Privacy-Preserving Image Retrieval Application." <em>KINGPC ICNGC</em>, 2024.</li>
                    </ul>

                    <h5 class="pub-subheading">Domestic Journals & Conferences (Korea)</h5>
                    <ul class="pub-list">
                        <li>M.S. Uzzal, <strong>I. Ahmad</strong>, and S. Shin. "Perceptual Encryption-based Secure Image Retrieval Scheme with Feature Fusion Descriptor." <em>KINGPC J-KINGPC</em>, 2025.</li>
                        <li>M.S. Uzzal, <strong>I. Ahmad</strong>, and S. Shin. "Perceptual Encryption-based Secure Image Retrieval using CEDD." <em>KINGPC Spring Conference</em>, 2025.</li>
                        <li>M.S. Uzzal, <strong>I. Ahmad</strong>, and S. Shin. "Edge Histogram Descriptor with DWT Decomposition for Medical Image Retrieval Applications." <em>KICS KoreaAI</em>, 2024.</li>
                    </ul>
                </div>

                <div class="mentee-testimonial">
                    <span class="quote-icon">“</span>
                    <p class="quote-text">
                        A special note of appreciation goes to Dr. Ijaz Ahmad... To me, he is more than a mentor, he is a guide, a motivator, and a genuine friend. His advice and constant support led me to achieve several publications and awards during my master's journey... His kindness, humor, and leadership has created an environment where hard work feels meaningful and growth becomes inevitable.
                    </p>
                    <p class="quote-source">— Excerpt from M.S. Thesis Acknowledgements</p>
                </div>
            </div>
        </details>
    </div>

    <!-- Mentee Card 2: Ghazal Saadloonia -->
    <div class="mentee-card">
        <div class="mentee-header">
            <div class="mentee-meta">
                <div class="name-row">
                    <h3>Ghazal Saadloonia</h3>
                    <a href="https://scholar.google.com/citations?user=lEqglTEAAAAJ&hl=en" target="_blank" class="scholar-link" title="Google Scholar Profile">
                        <svg class="scholar-icon" viewBox="0 0 24 24"><path d="M12 2L1 21h22L12 2zm0 4l7.5 13h-15L12 6z"/></svg> Scholar
                    </a>
                </div>
                <p class="institution">Department of Computer Engineering, Chosun University</p>
                <div class="timeline-badges">
                    <span class="badge active">Ph.D. Candidate (2026 — Present)</span>
                    <span class="badge alumni">M.S. Alumnus (2025 — 2026)</span>
                    <!-- Research Interest Tag -->
                    <span class="badge tag-vision">👁️ CV & Efficient Deep Learning</span>
                </div>
            </div>
        </div>

        <details class="mentee-details">
            <summary class="toggle-btn">
                <span class="btn-text-show">✨ View Full Research, Awards & Testimonial</span>
                <span class="btn-text-hide">✨ Hide Details</span>
            </summary>
            
            <div class="mentee-body">
                <div class="research-focus">
                    <h4>Master's Thesis</h4>
                    <p class="thesis-title">"Efficient Deep Learning-Based Feature Extraction for Image Retrieval Applications"</p>
                </div>

                <div class="mentee-awards">
                    <h4>🏆 Awards & Recognition</h4>
                    <ul>
                        <li><strong>KICS Excellent Paper Award (2025)</strong> – KICS Korea AI Conference</li>
                    </ul>
                </div>

                <div class="mentee-publications">
                    <h4>📚 Joint Publications</h4>
                    <h5 class="pub-subheading">International Journals</h5>
                    <ul class="pub-list">
                        <li>G. Saadloonia, <strong>I. Ahmad</strong>, and S. Shin. "Heterogeneity-Aware Federated Learning: A Quantitative Survey on Aggregation Paradigms in Non-IID IoT Networks." <em>IEEE Access</em>. <span style="color: #d93f0b; font-weight: 600;">(Under review)</span></li>
                    </ul>

                    <h5 class="pub-subheading">International Conferences</h5>
                    <ul class="pub-list">
                        <li>G. Saadloonia, <strong>I. Ahmad</strong>, and S. Shin. "Fine-Tuning EfficientNet Feature Extraction for Efficiency in Image Retrieval Applications." <em>IEEE ICAIIC</em>, 2026.</li>
                    </ul>

                    <h5 class="pub-subheading">Domestic Conferences (Korea)</h5>
                    <ul class="pub-list">
                        <li>G. Saadloonia, <strong>I. Ahmad</strong>, and S. Shin. "EfficientNet Models with Dimensionality Reduction for Image Retrieval Applications." <em>KICS KoreaAI</em>, 2025.</li>
                        <li>G. Saadloonia, <strong>I. Ahmad</strong>, and S. Shin. "Device Heterogeneity Challenges and Solutions in Federated Learning." <em>KINGPC Spring Conference</em>, 2025.</li>
                    </ul>
                </div>

                <div class="mentee-testimonial">
                    <span class="quote-icon">“</span>
                    <p class="quote-text">
                        I would like to express my profound gratitude to Dr. Ijaz Ahmad—the one who enlightened my young mind. He has been a mentor, teacher, guide, inspiration, supporter, and above all, a true friend... Learning from him felt like a real-life application of transfer learning, I had the privilege of learning from a remarkable researcher trained on an exceptionally large dataset of knowledge and experience... Among the many advice he gave me, one remains deeply engraved in my mind: “Once you are good at research, you will be good at many other things, because the way you do one thing determines the way you do other things.”
                    </p>
                    <p class="quote-source">— Excerpt from M.S. Thesis Acknowledgements</p>
                </div>
            </div>
        </details>
    </div>

	<!-- Mentee Card 3: Abdullah Al Mahbub -->
	<div class="mentee-card">
		<div class="mentee-header">
			<div class="mentee-meta">
				<h3>Abdullah Al Mahbub</h3>
				<div class="name-row">
				<a href="https://scholar.google.com/citations?user=g4loMOYAAAAJ&hl=en" target="_blank" class="scholar-link" title="Google Scholar Profile">
                        <svg class="scholar-icon" viewBox="0 0 24 24"><path d="M12 2L1 21h22L12 2zm0 4l7.5 13h-15L12 6z"/></svg> Scholar
                </a>
				</div>
				<p class="institution">Department of Computer Engineering, Chosun University</p>
				<div class="timeline-badges">
					<span class="badge alumni">M.S. Alumnus (2024 — 2026)</span>
					<span class="badge tag-security">📡 Wireless Comm & Deep Learning </span>
				</div>
			</div>
		</div>

		<!-- HTML-Native Dropdown Component -->
		<details class="mentee-details">
			<summary class="toggle-btn">
				<span class="btn-text-show">✨ View Full Research & Awards</span>
				<span class="btn-text-hide">✨ Hide Details</span>
			</summary>
			
			<div class="mentee-body">
				<!-- Master's Thesis -->
				<div class="research-focus">
					<h4>Master's Thesis</h4>
					<p class="thesis-title">"Comprehensive Analysis of Efficient Deep Learning-Based SNR Estimation for OFDM Systems"</p>
				</div>

				<!-- Awards Section -->
				<div class="mentee-awards">
					<h4>🏆 Awards & Recognition</h4>
					<ul>
						<li><strong>KINGPC Excellent Paper Award (2025)</strong> – KINGPC ICNGC Conference</li>
					</ul>
				</div>

				<!-- Publications -->
				<div class="mentee-publications">
					<h4>📚 Joint Publications</h4>
					
					<h5 class="pub-subheading">International Journals</h5>
					<ul class="pub-list">
						<li>A.A. Mahbub, <strong>I. Ahmad</strong>, and S. Shin. "Comprehensive Analysis of CNN-based Models for SNR Estimation." <em>IEEE Access</em>, 2025.</li>
					</ul>

					<h5 class="pub-subheading">International Conferences</h5>
					<ul class="pub-list">
						<li>A.A. Mahbub, <strong>I. Ahmad</strong>, and S. Shin. "Lightweight CNN Model Design using Bayesian Optimization and Truncated Singular Value Decomposition for SNR Estimation." <em>IEEE ICUFN</em>, 2026.</li>
						<li>A.A. Mahbub, <strong>I. Ahmad</strong>, and S. Shin. "A Lightweight CNN Model for SNR Estimation in OFDM Systems." <em>KINGPC ICNGC</em>, 2025.</li>
						<li>A.A. Mahbub, <strong>I. Ahmad</strong>, and S. Shin. "Comparative Analysis of CNN Models for SNR Estimation." <em>IEEE ICUFN</em>, 2025.</li>
					</ul>

					<h5 class="pub-subheading">Domestic Conferences (Korea)</h5>
					<ul class="pub-list">
						<li>A.A. Mahbub, <strong>I. Ahmad</strong>, and S. Shin. "Low-Rank Model Compression for Energy-Efficient Deep Learning–based SNR Estimation." <em>KINGPC Spring Conference</em>, 2026.</li>
					</ul>
				</div>
			</div>
		</details>
	</div>


</section>
