---
layout: tech
title: API Documentation
---

<section class="hero" style="min-height: 40vh;">
    <div class="hero-content">
        <h1>API Documentation</h1>
        <p class="subtitle">REST API Documentation & Integration Guides</p>
    </div>
</section>

<section class="section">
    <div class="container">
        <div class="card">
            <h2>Sample: E-Commerce API Documentation</h2>
            <p><strong>Project Overview:</strong> Complete REST API documentation for a fictional e-commerce platform, demonstrating authentication, endpoints, error handling, and code examples.</p>
            
            <h3 style="margin-top: 2rem;">Key Features Demonstrated:</h3>
            <ul style="color: #90a4ae; margin-left: 1.5rem;">
                <li>OpenAPI/Swagger specification</li>
                <li>Interactive API endpoints with examples</li>
                <li>Authentication workflow documentation</li>
                <li>Error code reference</li>
                <li>Rate limiting and best practices</li>
                <li>SDK integration guides</li>
            </ul>
            
            <h3 style="margin-top: 2rem;">Sample Endpoint Documentation:</h3>
            
            <div style="background: rgba(0, 0, 0, 0.3); border-radius: 8px; padding: 1.5rem; margin: 1rem 0; border-left: 4px solid #00e5ff;">
                <h4>GET /api/v1/products</h4>
                <p><strong>Description:</strong> Retrieve a list of products with optional filtering and pagination.</p>
                
                <h5>Parameters:</h5>
                <ul style="color: #90a4ae;">
                    <li><code>category</code> (optional) - Filter by product category</li>
                    <li><code>page</code> (optional) - Page number for pagination</li>
                    <li><code>limit</code> (optional) - Number of items per page</li>
                </ul>
                
                <h5>Response Example:</h5>
                <pre style="background: rgba(0, 0, 0, 0.5); padding: 1rem; border-radius: 4px; overflow-x: auto;">
{
  "data": [
    {
      "id": "prod_123",
      "name": "Wireless Headphones",
      "category": "electronics",
      "price": 199.99,
      "in_stock": true
    }
  ],
  "pagination": {
    "page": 1,
    "limit": 20,
    "total": 150
  }
}</pre>
            </div>
            
            <div style="margin-top: 2rem;">
                <h3>Tools & Technologies Used:</h3>
                <ul style="color: #90a4ae;">
                    <li>OpenAPI 3.0 Specification</li>
                    <li>Swagger UI for interactive documentation</li>
                    <li>Postman for API testing</li>
                    <li>Git for version control</li>
                    <li>Markdown for content formatting</li>
                </ul>
            </div>
        </div>
        
        <div class="card" style="margin-top: 2rem;">
            <h2>Additional API Documentation Skills</h2>
            <ul style="color: #90a4ae;">
                <li><strong>Authentication Flows:</strong> OAuth2, API Keys, JWT tokens</li>
                <li><strong>SDK Development:</strong> Python, JavaScript, Java client libraries</li>
                <li><strong>Webhook Documentation:</strong> Event-driven architecture</li>
                <li><strong>GraphQL:</strong> Query language documentation</li>
                <li><strong>Versioning:</strong> API version management and migration guides</li>
            </ul>
        </div>
    </div>
</section>

<div style="text-align: center; margin-top: 3rem;">
    <a href="/portfolio/" class="btn-gradient">← Back to Portfolio</a>
</div>
