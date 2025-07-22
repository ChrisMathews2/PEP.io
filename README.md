# PEP.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pacific Energy Partners - Investment Information Memorandum</title>
    <style>
        @page {
            size: A4;
            margin: 0;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --primary: #0066cc;
            --secondary: #00a651;
            --accent: #ffd700;
            --dark: #1a1a1a;
            --light: #f8f9fa;
            --gradient: linear-gradient(135deg, #0066cc 0%, #00a651 100%);
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: #333;
            background: white;
        }
        
        /* Cover Page */
        .cover-page {
            height: 100vh;
            background: var(--gradient);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            position: relative;
            overflow: hidden;
            page-break-after: always;
        }
        
        .cover-page::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            animation: rotate 30s linear infinite;
        }
        
        @keyframes rotate {
            to { transform: rotate(360deg); }
        }
        
        .cover-content {
            text-align: center;
            z-index: 1;
            max-width: 800px;
            padding: 0 40px;
        }
        
        .logo-placeholder {
            width: 200px;
            height: 200px;
            background: white;
            border-radius: 50%;
            margin: 0 auto 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3em;
            color: var(--primary);
            font-weight: bold;
            box-shadow: 0 10px 40px rgba(0,0,0,0.2);
        }
        
        .cover-page h1 {
            font-size: 3.5em;
            font-weight: 700;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .cover-page h2 {
            font-size: 1.8em;
            font-weight: 300;
            margin-bottom: 40px;
            opacity: 0.9;
        }
        
        .document-type {
            font-size: 1.2em;
            text-transform: uppercase;
            letter-spacing: 2px;
            opacity: 0.8;
            margin-bottom: 60px;
        }
        
        .cover-date {
            position: absolute;
            bottom: 40px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 1.1em;
            opacity: 0.8;
        }
        
        /* Content Pages */
        .page {
            min-height: 100vh;
            padding: 80px 60px;
            page-break-after: always;
            position: relative;
        }
        
        .page-header {
            position: absolute;
            top: 30px;
            right: 60px;
            color: #999;
            font-size: 0.9em;
        }
        
        .page-footer {
            position: absolute;
            bottom: 30px;
            left: 60px;
            right: 60px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: #999;
            font-size: 0.9em;
            padding-top: 20px;
            border-top: 1px solid #e0e0e0;
        }
        
        h1 {
            font-size: 2.5em;
            color: var(--dark);
            margin-bottom: 30px;
            position: relative;
            padding-bottom: 15px;
        }
        
        h1::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 3px;
            background: var(--secondary);
        }
        
        h2 {
            font-size: 2em;
            color: var(--primary);
            margin: 40px 0 20px;
        }
        
        h3 {
            font-size: 1.5em;
            color: var(--dark);
            margin: 30px 0 15px;
        }
        
        p {
            margin-bottom: 15px;
            text-align: justify;
        }
        
        .highlight-box {
            background: var(--light);
            border-left: 4px solid var(--secondary);
            padding: 20px;
            margin: 30px 0;
            border-radius: 0 10px 10px 0;
        }
        
        .key-metric {
            background: white;
            border: 1px solid #e0e0e0;
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
        }
        
        .key-metric:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }
        
        .metric-value {
            font-size: 2.5em;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 5px;
        }
        
        .metric-label {
            color: #666;
            font-size: 0.9em;
        }
        
        .metrics-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }
        
        /* Tables */
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 30px 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        
        th {
            background: var(--gradient);
            color: white;
            padding: 15px;
            text-align: left;
            font-weight: 600;
        }
        
        td {
            padding: 15px;
            border-bottom: 1px solid #e0e0e0;
        }
        
        tr:hover {
            background: var(--light);
        }
        
        /* Revenue Chart */
        .revenue-visual {
            margin: 40px 0;
            padding: 30px;
            background: var(--light);
            border-radius: 15px;
        }
        
        .revenue-bars {
            display: flex;
            justify-content: space-around;
            align-items: flex-end;
            height: 300px;
            margin-top: 20px;
        }
        
        .revenue-bar {
            width: 20%;
            background: var(--gradient);
            border-radius: 10px 10px 0 0;
            position: relative;
            display: flex;
            align-items: flex-end;
            justify-content: center;
            color: white;
            font-weight: 600;
            padding-bottom: 10px;
        }
        
        .revenue-label {
            position: absolute;
            bottom: -30px;
            font-size: 0.9em;
            color: #666;
            text-align: center;
            width: 100%;
        }
        
        /* Timeline */
        .timeline {
            margin: 40px 0;
            position: relative;
            padding-left: 40px;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            left: 10px;
            top: 0;
            bottom: 0;
            width: 2px;
            background: var(--secondary);
        }
        
        .timeline-item {
            position: relative;
            margin-bottom: 30px;
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            left: -35px;
            top: 5px;
            width: 12px;
            height: 12px;
            background: var(--secondary);
            border-radius: 50%;
            border: 3px solid white;
            box-shadow: 0 0 0 3px var(--light);
        }
        
        .timeline-item h4 {
            color: var(--primary);
            margin-bottom: 5px;
        }
        
        /* Investment Terms */
        .investment-terms {
            background: var(--gradient);
            color: white;
            padding: 50px;
            border-radius: 20px;
            margin: 40px 0;
            position: relative;
            overflow: hidden;
        }
        
        .investment-terms::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 60%);
            animation: rotate 25s linear infinite reverse;
        }
        
        .investment-terms h2 {
            color: white;
            text-align: center;
            margin-bottom: 40px;
            font-size: 2.5em;
        }
        
        .terms-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            position: relative;
            z-index: 1;
        }
        
        .term-item {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            padding: 25px;
            border-radius: 15px;
            text-align: center;
        }
        
        .term-item h3 {
            color: white;
            margin-bottom: 10px;
        }
        
        .term-value {
            font-size: 2em;
            font-weight: 700;
        }
        
        /* Executive Summary Box */
        .executive-summary {
            background: linear-gradient(135deg, var(--light) 0%, white 100%);
            border-radius: 20px;
            padding: 40px;
            margin: 40px 0;
            box-shadow: 0 5px 30px rgba(0,0,0,0.1);
        }
        
        /* Print Styles */
        @media print {
            .page {
                page-break-after: always;
            }
            
            @keyframes rotate {
                to { transform: none; }
            }
        }
    </style>
</head>
<body>
    <!-- Cover Page -->
    <div class="cover-page">
        <div class="cover-content">
            <div class="logo-placeholder">PEP</div>
            <h1>Pacific Energy Partners</h1>
            <h2>Energy that Empowers the Pacific</h2>
            <div class="document-type">Investment Information Memorandum</div>
            <div class="cover-date">Series A Funding Round • September 2026</div>
        </div>
    </div>
    
    <!-- Executive Summary Page -->
    <div class="page">
        <div class="page-header">CONFIDENTIAL</div>
        
        <h1>Executive Summary</h1>
        
        <div class="executive-summary">
            <p style="font-size: 1.2em; line-height: 1.8;">
                Pacific Energy Partners is revolutionizing energy access across the Pacific region by combining 
                <strong>community impact with commercial success</strong>. We deliver affordable, sustainable energy 
                solutions while generating attractive returns for investors through a proven multi-stream business model.
            </p>
        </div>
        
        <div class="metrics-grid">
            <div class="key-metric">
                <div class="metric-value">$10B</div>
                <div class="metric-label">Total Addressable Market</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">25%</div>
                <div class="metric-label">Target IRR (5 Years)</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">11%</div>
                <div class="metric-label">EBITDA Margin (Year 3)</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">4-5×</div>
                <div class="metric-label">Exit Multiple (Year 5)</div>
            </div>
        </div>
        
        <h2>Investment Highlights</h2>
        <div class="highlight-box">
            <ul style="list-style: none; padding: 0;">
                <li style="margin: 10px 0;">✓ <strong>Diversified Revenue Model:</strong> Four complementary revenue streams reducing risk</li>
                <li style="margin: 10px 0;">✓ <strong>Social Impact:</strong> 20% discount for 55+ demographic creates brand loyalty</li>
                <li style="margin: 10px 0;">✓ <strong>Scalable Platform:</strong> Technology-enabled growth across Pacific markets</li>
                <li style="margin: 10px 0;">✓ <strong>Strategic Partnerships:</strong> Government and community collaborations</li>
                <li style="margin: 10px 0;">✓ <strong>Renewable Focus:</strong> 100% commitment to sustainable energy sources</li>
            </ul>
        </div>
        
        <div class="page-footer">
            <span>Pacific Energy Partners</span>
            <span>Page 1</span>
        </div>
    </div>
    
    <!-- Mission & Market Opportunity -->
    <div class="page">
        <div class="page-header">CONFIDENTIAL</div>
        
        <h1>Our Mission</h1>
        <p style="font-size: 1.2em; font-style: italic; color: var(--primary); margin-bottom: 30px;">
            "To democratize access to affordable and sustainable energy across Pacific communities, 
            creating lasting value for all stakeholders."
        </p>
        
        <h2>The Market Opportunity</h2>
        
        <h3>Critical Market Challenges</h3>
        <table>
            <tr>
                <th>Challenge</th>
                <th>Impact</th>
                <th>Our Solution</th>
            </tr>
            <tr>
                <td>Rising Energy Costs</td>
                <td>55+ population struggling with affordability</td>
                <td>20% subsidized pricing program</td>
            </tr>
            <tr>
                <td>Infrastructure Pressure</td>
                <td>Community organizations facing operational stress</td>
                <td>Bulk buying & solar partnerships</td>
            </tr>
            <tr>
                <td>Housing Affordability</td>
                <td>Energy costs impacting all demographics</td>
                <td>Scalable government partnerships</td>
            </tr>
            <tr>
                <td>Climate Imperatives</td>
                <td>Urgent renewable transition needed</td>
                <td>100% renewable energy focus</td>
            </tr>
            <tr>
                <td>Market Inefficiencies</td>
                <td>Limited community-oriented solutions</td>
                <td>Integrated partnership model</td>
            </tr>
        </table>
        
        <h3>Market Segmentation</h3>
        <div class="metrics-grid">
            <div class="key-metric">
                <div class="metric-value">~25%</div>
                <div class="metric-label">NZ Population 55+</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">70k+</div>
                <div class="metric-label">Social Housing Properties</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">15k+</div>
                <div class="metric-label">Sports Clubs & Charities</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">2.1M</div>
                <div class="metric-label">Total Households</div>
            </div>
        </div>
        
        <div class="page-footer">
            <span>Pacific Energy Partners</span>
            <span>Page 2</span>
        </div>
    </div>
    
    <!-- Business Model -->
    <div class="page">
        <div class="page-header">CONFIDENTIAL</div>
        
        <h1>Business Model</h1>
        <p style="font-size: 1.1em; margin-bottom: 30px;">
            Our innovative multi-stream revenue model combines commercial viability with social impact, 
            creating a sustainable flywheel effect that benefits all stakeholders.
        </p>
        
        <h2>Revenue Architecture (Year 3 Target)</h2>
        <div class="revenue-visual">
            <div class="revenue-bars">
                <div class="revenue-bar" style="height: 80%;">
                    40%
                    <span class="revenue-label">Direct Consumer<br/>Revenue</span>
                </div>
                <div class="revenue-bar" style="height: 60%; background: linear-gradient(135deg, #00a651 0%, #0066cc 100%);">
                    30%
                    <span class="revenue-label">Government<br/>Contracts</span>
                </div>
                <div class="revenue-bar" style="height: 40%;">
                    20%
                    <span class="revenue-label">Community<br/>Partnerships</span>
                </div>
                <div class="revenue-bar" style="height: 20%; background: linear-gradient(135deg, #ffd700 0%, #00a651 100%);">
                    10%
                    <span class="revenue-label">Solar<br/>Export</span>
                </div>
            </div>
        </div>
        
        <h2>The Flywheel Effect</h2>
        <div class="highlight-box">
            <h3 style="color: var(--primary); margin-top: 0;">Self-Reinforcing Growth Model</h3>
            <p><strong>1. Scale Achievement:</strong> Growing customer base reduces wholesale costs</p>
            <p><strong>2. Competitive Pricing:</strong> Lower costs enable market-leading prices</p>
            <p><strong>3. Asset Development:</strong> Cash flows fund solar infrastructure</p>
            <p><strong>4. Cost Reduction:</strong> Asset ownership further reduces energy costs</p>
            <p><strong>5. Community Impact:</strong> Surplus funds 55+ subsidies, building brand loyalty</p>
            <p style="margin-bottom: 0;"><strong>6. Market Expansion:</strong> Strong brand drives customer acquisition</p>
        </div>
        
        <h3>Growth Milestones</h3>
        <table>
            <tr>
                <th>Metric</th>
                <th>Year 1</th>
                <th>Year 2</th>
                <th>Year 3</th>
            </tr>
            <tr>
                <td>Retail Customers</td>
                <td>5,000</td>
                <td>15,000</td>
                <td>25,000</td>
            </tr>
            <tr>
                <td>Government Properties</td>
                <td>5,000</td>
                <td>12,000</td>
                <td>20,000</td>
            </tr>
            <tr>
                <td>Community Partners</td>
                <td>200</td>
                <td>600</td>
                <td>1,000</td>
            </tr>
            <tr>
                <td>55+ Households</td>
                <td>10,000</td>
                <td>35,000</td>
                <td>60,000</td>
            </tr>
            <tr>
                <td>Solar Capacity (MWh)</td>
                <td>60</td>
                <td>180</td>
                <td>400</td>
            </tr>
        </table>
        
        <div class="page-footer">
            <span>Pacific Energy Partners</span>
            <span>Page 3</span>
        </div>
    </div>
    
    <!-- Financial Projections -->
    <div class="page">
        <div class="page-header">CONFIDENTIAL</div>
        
        <h1>Financial Projections</h1>
        
        <div class="metrics-grid">
            <div class="key-metric">
                <div class="metric-value">NZ$28.7M</div>
                <div class="metric-label">Year 3 Revenue</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">Month 24</div>
                <div class="metric-label">Break-even Point</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">Month 30</div>
                <div class="metric-label">Positive Cash Flow</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">11%</div>
                <div class="metric-label">EBITDA Margin (Y3)</div>
            </div>
        </div>
        
        <h2>Revenue Projections</h2>
        <table>
            <tr>
                <th>Revenue Stream</th>
                <th>Year 1</th>
                <th>Year 2</th>
                <th>Year 3</th>
                <th>CAGR</th>
            </tr>
            <tr>
                <td>Direct Consumer</td>
                <td>NZ$1.7M</td>
                <td>NZ$5.0M</td>
                <td>NZ$11.5M</td>
                <td>90%</td>
            </tr>
            <tr>
                <td>Government Contracts</td>
                <td>NZ$1.3M</td>
                <td>NZ$3.8M</td>
                <td>NZ$8.6M</td>
                <td>87%</td>
            </tr>
            <tr>
                <td>Community Partnerships</td>
                <td>NZ$0.8M</td>
                <td>NZ$2.5M</td>
                <td>NZ$5.7M</td>
                <td>92%</td>
            </tr>
            <tr>
                <td>Solar Export</td>
                <td>NZ$0.4M</td>
                <td>NZ$1.2M</td>
                <td>NZ$2.9M</td>
                <td>95%</td>
            </tr>
            <tr style="font-weight: 700; background: var(--light);">
                <td>Total Revenue</td>
                <td>NZ$4.2M</td>
                <td>NZ$12.5M</td>
                <td>NZ$28.7M</td>
                <td>90%</td>
            </tr>
        </table>
        
        <h2>Profitability Bridge</h2>
        <div class="highlight-box">
            <p><strong>Gross Margin Evolution:</strong></p>
            <ul style="margin-left: 20px;">
                <li>Year 1: 17-22% (market entry pricing)</li>
                <li>Year 2: 22-25% (scale efficiencies)</li>
                <li>Year 3: 25%+ (asset ownership benefits)</li>
            </ul>
            <p style="margin-top: 15px;"><strong>EBITDA Impact:</strong> 11% margin achieved in Year 3 AFTER funding 
            the 55+ subsidy program (vs. ~14% without subsidy), demonstrating sustainable impact model.</p>
        </div>
        
        <h3>Use of Funds</h3>
        <div class="metrics-grid">
            <div class="key-metric">
                <div class="metric-value">40%</div>
                <div class="metric-label">Solar Infrastructure</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">25%</div>
                <div class="metric-label">Technology Platform</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">20%</div>
                <div class="metric-label">Market Expansion</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">15%</div>
                <div class="metric-label">Working Capital</div>
            </div>
        </div>
        
        <div class="page-footer">
            <span>Pacific Energy Partners</span>
            <span>Page 4</span>
        </div>
    </div>
    
    <!-- Implementation & Risk -->
    <div class="page">
        <div class="page-header">CONFIDENTIAL</div>
        
        <h1>Implementation Strategy</h1>
        
        <div class="timeline">
            <div class="timeline-item">
                <h4>Phase 1: Foundation (Oct 2026 - Mar 2027)</h4>
                <p>Core infrastructure development, initial partnerships, 55+ pilot launch in Auckland region</p>
            </div>
            <div class="timeline-item">
                <h4>Phase 2: Expansion (Apr 2027 - Sep 2027)</h4>
                <p>Scale retail services, broaden community partnerships, extend solar network to 5 key regions</p>
            </div>
            <div class="timeline-item">
                <h4>Phase 3: Growth (Oct 2027 onwards)</h4>
                <p>National rollout, advanced technology integration, service diversification, international expansion planning</p>
            </div>
        </div>
        
        <h2>Risk Management</h2>
        <table>
            <tr>
                <th>Risk Category</th>
                <th>Potential Impact</th>
                <th>Mitigation Strategy</th>
            </tr>
            <tr>
                <td>Regulatory Changes</td>
                <td>Policy shifts affecting subsidies</td>
                <td>Active engagement with policymakers, diversified revenue model</td>
            </tr>
            <tr>
                <td>Market Competition</td>
                <td>Pressure on margins</td>
                <td>Unique value proposition, community bonds, strategic partnerships</td>
            </tr>
            <tr>
                <td>Wholesale Price Volatility</td>
                <td>Cost fluctuations</td>
                <td>65% hedged with long-term renewable PPAs</td>
            </tr>
            <tr>
                <td>Customer Churn</td>
                <td>Revenue impact</td>
                <td>Loyalty programs, fixed-rate options, community engagement</td>
            </tr>
            <tr>
                <td>Technology Risk</td>
                <td>Platform reliability</td>
                <td>Robust partnerships, proven systems, redundancy planning</td>
            </tr>
            <tr>
                <td>Funding Challenges</td>
                <td>Growth constraints</td>
                <td>Diversified revenue streams, strong unit economics</td>
            </tr>
        </table>
        
        <h2>Competitive Advantages</h2>
        <div class="highlight-box">
            <h3 style="color: var(--primary); margin-top: 0;">Sustainable Moats</h3>
            <ul style="list-style: none; padding: 0;">
                <li style="margin: 8px 0;">🛡️ <strong>Community Trust:</strong> Deep relationships with 55+ demographic</li>
                <li style="margin: 8px 0;">🤝 <strong>Strategic Partnerships:</strong> Government and community collaborations</li>
                <li style="margin: 8px 0;">☀️ <strong>Asset Ownership:</strong> Solar infrastructure providing cost advantages</li>
                <li style="margin: 8px 0;">💡 <strong>Technology Platform:</strong> Scalable systems enabling efficient growth</li>
                <li style="margin: 8px 0;">🌿 <strong>Brand Values:</strong> Authentic commitment to sustainability and community</li>
            </ul>
        </div>
        
        <div class="page-footer">
            <span>Pacific Energy Partners</span>
            <span>Page 5</span>
        </div>
    </div>
    
    <!-- Investment Terms -->
    <div class="page">
        <div class="page-header">CONFIDENTIAL</div>
        
        <h1>Investment Opportunity</h1>
        
        <div class="investment-terms">
            <h2>Series A Funding Round - September 2026</h2>
            <div class="terms-grid">
                <div class="term-item">
                    <h3>Total Raise</h3>
                    <div class="term-value">NZ$10M</div>
                </div>
                <div class="term-item">
                    <h3>Minimum Investment</h3>
                    <div class="term-value">NZ$500k</div>
                </div>
                <div class="term-item">
                    <h3>Preferred Return</h3>
                    <div class="term-value">8%</div>
                    <p style="font-size: 0.9em; margin-top: 5px;">Cumulative dividend</p>
                </div>
                <div class="term-item">
                    <h3>Target IRR</h3>
                    <div class="term-value">25%</div>
                    <p style="font-size: 0.9em; margin-top: 5px;">Over 5 years</p>
                </div>
                <div class="term-item">
                    <h3>Exit Multiple</h3>
                    <div class="term-value">4-5×</div>
                    <p style="font-size: 0.9em; margin-top: 5px;">By Year 5</p>
                </div>
                <div class="term-item">
                    <h3>Board Seats</h3>
                    <div class="term-value">Available</div>
                    <p style="font-size: 0.9em; margin-top: 5px;">For investments ≥ NZ$2M</p>
                </div>
            </div>
        </div>
        
        <h2>Investment Highlights</h2>
        <div class="metrics-grid">
            <div class="key-metric">
                <div class="metric-value">✓</div>
                <div class="metric-label">Proven Business Model</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">✓</div>
                <div class="metric-label">Multiple Revenue Streams</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">✓</div>
                <div class="metric-label">Strong Social Impact</div>
            </div>
            <div class="key-metric">
                <div class="metric-value">✓</div>
                <div class="metric-label">Experienced Team</div>
            </div>
        </div>
        
        <h2>Next Steps</h2>
        <div class="highlight-box">
            <p><strong>To express interest in this opportunity:</strong></p>
            <ol style="margin-left: 20px;">
                <li>Contact our investment team at <strong>investors@pacificenergypartners.com</strong></li>
                <li>Request detailed financial models and due diligence materials</li>
                <li>Schedule management presentations and site visits</li>
                <li>Review legal documentation and investment terms</li>
            </ol>
        </div>
        
        <div style="text-align: center; margin-top: 60px;">
            <h3 style="color: var(--primary); font-size: 1.8em; margin-bottom: 20px;">
                "He waka eke noa – we are all in this together"
            </h3>
            <p style="font-size: 1.2em; color: #666;">
                Join us in transforming the Pacific's energy future while generating strong returns
            </p>
        </div>
        
        <div class="page-footer">
            <span>Pacific Energy Partners</span>
            <span>Page 6</span>
        </div>
    </div>
    
    <!-- Back Cover -->
    <div class="cover-page" style="justify-content: flex-end; padding-bottom: 80px;">
        <div style="text-align: center; z-index: 1;">
            <div class="logo-placeholder" style="width: 100px; height: 100px; font-size: 1.5em; margin-bottom: 20px;">PEP</div>
            <h2 style="font-size: 1.5em; margin-bottom: 10px;">Pacific Energy Partners</h2>
            <p style="opacity: 0.8;">Energy that Empowers the Pacific</p>
            <p style="margin-top: 40px; opacity: 0.6;">
                investors@pacificenergypartners.com<br>
                www.pacificenergypartners.com
            </p>
        </div>
    </div>
</body>
</html>
