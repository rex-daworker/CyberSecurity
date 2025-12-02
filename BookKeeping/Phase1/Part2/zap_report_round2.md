<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>ZAP by Checkmarx Scanning Report</title>
<link
	href="zap_report_round2_d/normalize/normalize.css" rel="stylesheet">
<link
	href="zap_report_round2_d/themes/original/main.css" rel="stylesheet">
<link
	href="zap_report_round2_d/themes/original/colors.css" rel="stylesheet">
</head>
<body>
	<header>
		<h1>ZAP by Checkmarx Scanning Report</h1>
		<p>
			<span>Generated with</span> <a href="https://zaproxy.org"><img
				src="zap_report_round2_d/zap32x32.png" alt="The ZAP logo" class="zap-logo">ZAP</a>
			<span>on Tue 2 Dec 2025, at 17:28:11</span>
		</p>
		<p>ZAP Version: 2.16.1</p>
		<p>
			ZAP by <a href="https://checkmarx.com/">Checkmarx</a>
		</p>
	</header>

	<main>

		<section id="contents" class="contents">
			<h2>Contents</h2>
			<nav>
				<ol>
					<li><a
						href="#about-this-report">About this report</a>
						<ol>
							
							<li><a
								href="#report-parameters">Report parameters</a></li>
						</ol></li>
					<data-th-block>
					<li><a
						href="#summaries">Summaries</a>
						<ol>
							<li><a
								href="#risk-confidence-counts">Alert counts by risk and confidence</a></li>
							<li><a
								href="#site-risk-counts">Alert counts by site and risk</a></li>
							<li><a
								href="#alert-type-counts">Alert counts by alert type</a></li>
						</ol></li>
					<li><a
						href="#alerts">Alerts</a>
						<ol>
							
							 
							
							
							
							
							
							
							
							
							<li><a
								href="#alerts--risk-2-confidence-1"><span>Risk</span>=<span
									class="risk-level">Medium</span>, <span>Confidence</span>=<span
									class="confidence-level">Low</span> <span>(1)</span></a></li>
							  
							 
							
							
							
							
							
							
							<li><a
								href="#alerts--risk-0-confidence-2"><span>Risk</span>=<span
									class="risk-level">Informational</span>, <span>Confidence</span>=<span
									class="confidence-level">Medium</span> <span>(1)</span></a></li>
							
							
							  
						</ol></li>
					<li><a
						href="#appendix">Appendix</a>
						<ol>
							<li><a
								href="#alert-types">Alert types</a></li>
						</ol></li>
					</data-th-block>
				</ol>
			</nav>
		</section>

		<section
			id="about-this-report" class="about-this-report">
			<h2>About this report</h2>

			

			<section
				id="report-parameters">
				<h3>Report parameters</h3>
				<div class="report-parameters--container">
					<h4>Contexts</h4>
					
					
					<p>No contexts were selected, so all contexts were included by default.</p>
					  

					<h4>Sites</h4>
					
					<p>The following sites were included:</p>
					<ul class="sites-list">
						<li><span class="site">http://localhost:8001</span></li>
					</ul>
					
					<p>(If no sites were selected, all sites were included by default.)</p>
					<p>An included site must also be within one of the included contexts for its data to be included in the report.</p>

					<h4>Risk levels</h4>
					<p>
						<span>Included</span>:
						 
						<span class="included-risk-codes"><span class="risk-level">High</span>, <span class="risk-level">Medium</span>, <span class="risk-level">Low</span>, <span class="risk-level">Informational</span></span>
					</p>
					<p>
						<span>Excluded</span>:
						 <span>None</span>
						
					</p>

					<h4>Confidence levels</h4>
					<p>
						<span>Included</span>:
						
						
						<span class="included-confidence-codes"><span class="confidence-level">User Confirmed</span>, <span class="confidence-level">High</span>, <span class="confidence-level">Medium</span>, <span class="confidence-level">Low</span></span>
					</p>
					<p>
						<span>Excluded</span>:
						
						
						<span class="included-confidence-codes"> <span class="confidence-level">User Confirmed</span>, <span class="confidence-level">High</span>, <span class="confidence-level">Medium</span>, <span class="confidence-level">Low</span>, <span class="confidence-level">False Positive</span></span>
					</p>
				</div>
			</section>
		</section>

		
		<section>
			
		</section>
		
		<section id="summaries" class="summaries">
			<h2>Summaries</h2>

			<section
				id="risk-confidence-counts">
				<h3>Alert counts by risk and confidence</h3>
				<table class="risk-confidence-counts-table">
					<caption>
						<p>This table shows the number of alerts for each level of risk and confidence included in the report.</p>
						<p>(The percentages in brackets represent the count as a percentage of the total number of alerts included in the report, rounded to one decimal place.)</p>
					</caption>
					<colgroup>
						<col>
						<col>
					</colgroup>
					<colgroup>
						<col
							style="width: 14.0%"><col
							style="width: 14.0%"><col
							style="width: 14.0%"><col
							style="width: 14.0%">
						<col style="width: 14.0%">
					</colgroup>
					<thead>
						<tr>
							<td colspan="2" rowspan="2"></td>
							<th scope="colgroup"
								colspan="5">Confidence</th>
						</tr>
						<tr>
							<th scope="col">User Confirmed</th>
							<th scope="col">High</th>
							<th scope="col">Medium</th>
							<th scope="col">Low</th>
							<th scope="col">Total</th>
						</tr>
					</thead>
					<tbody>
						<tr>
							<th scope="rowgroup"
								rowspan="5">Risk</th>
							<th scope="row">High</th>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>0</span><br> <span class="additional-info-percentages">(0.0%)</span></td>
						</tr>
						<tr>
							
							<th scope="row">Medium</th>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>1</span><br> <span
								class="additional-info-percentages">(50.0%)</span></td>
							<td><span>1</span><br> <span class="additional-info-percentages">(50.0%)</span></td>
						</tr>
						<tr>
							
							<th scope="row">Low</th>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>0</span><br> <span class="additional-info-percentages">(0.0%)</span></td>
						</tr>
						<tr>
							
							<th scope="row">Informational</th>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>1</span><br> <span
								class="additional-info-percentages">(50.0%)</span></td>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>1</span><br> <span class="additional-info-percentages">(50.0%)</span></td>
						</tr>
						<tr>
							<th scope="row">Total</th>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0.0%)</span></td>
							<td><span>1</span><br> <span
								class="additional-info-percentages">(50.0%)</span></td>
							<td><span>1</span><br> <span
								class="additional-info-percentages">(50.0%)</span></td>
							<td><span>2</span><br> <span
								class="additional-info-percentages">(100%)</span></td>
						</tr>
					</tbody>
				</table>
			</section>

			<section
				id="site-risk-counts">
				<h3>Alert counts by site and risk</h3>
				<table class="site-risk-counts-table">
					<caption>
						<p>This table shows, for each site for which one or more alerts were raised, the number of alerts raised at each risk level.</p>
						<p>Alerts with a confidence level of &quot;False Positive&quot; have been excluded from these counts.</p>
						<p>(The numbers in brackets are the number of alerts raised for the site at or above that risk level.)</p>
					</caption>
					<colgroup>
						<col>
						<col>
					</colgroup>
					<colgroup>
						<col
							style="width: 16.25%"><col
							style="width: 16.25%"><col
							style="width: 16.25%"><col
							style="width: 16.25%">
					</colgroup>
					<thead>
						<tr>
							<td colspan="2" rowspan="2"></td>
							<th scope="colgroup" colspan="4">Risk</th>
						</tr>
						<tr>
							<th scope="col">
								<span>High</span><br>  <span
									class="additional-info-percentages">(= High)</span>  
							</th>
							<th scope="col">
								<span>Medium</span><br>   <span
									class="additional-info-percentages">(&gt;= Medium)</span> 
							</th>
							<th scope="col">
								<span>Low</span><br>   <span
									class="additional-info-percentages">(&gt;= Low)</span> 
							</th>
							<th scope="col">
								<span>Informational</span><br>   <span
									class="additional-info-percentages">(&gt;= Informational)</span> 
							</th>
						</tr>
					</thead>
					<tbody>
						<tr>
							<th scope="rowgroup"
								rowspan="1">Site</th>
							<th scope="row">http://localhost:8001</th>
							
							<td><span>0</span><br> <span
								class="additional-info-percentages">(0)</span></td>
							<td><span>1</span><br> <span
								class="additional-info-percentages">(1)</span></td>
							<td><span>0</span><br> <span
								class="additional-info-percentages">(1)</span></td>
							<td><span>1</span><br> <span
								class="additional-info-percentages">(2)</span></td>
							
						</tr>
					</tbody>
				</table>
			</section>

			<section
				id="alert-type-counts">
				<h3>Alert counts by alert type</h3>
				<table class="alert-type-counts-table">
					<caption>
						<p>This table shows the number of alerts of each alert type, together with the alert type&#39;s risk level.</p>
						<p>(The percentages in brackets represent each count as a percentage, rounded to one decimal place, of the total number of alerts included in this report.)</p>
					</caption>
					<thead>
						<tr>
							<th scope="col">Alert type</th>
							<th scope="col">Risk</th>
							<th scope="col">Count</th>
						</tr>
					</thead>
					<tbody>
						<tr>
							<th scope="row"><a
								href="#alert-type-0">Absence of Anti-CSRF Tokens</a></th>
							<td class="risk-level">Medium</td>
							<td><span>1</span><br> <span
								class="additional-info-percentages">(50.0%)</span></td>
						</tr>
						<tr>
							<th scope="row"><a
								href="#alert-type-1">User Agent Fuzzer</a></th>
							<td class="risk-level">Informational</td>
							<td><span>12</span><br> <span
								class="additional-info-percentages">(600.0%)</span></td>
						</tr>
					</tbody>
					<tfoot>
						<tr>
							<th scope="row">Total</th>
							<td></td>
							<td>2</td>
						</tr>
					</tfoot>
				</table>
			</section>
		</section>

		<section id="alerts" class="alerts">
			<h2>Alerts</h2>
			<ol>
				
				 
				 
				
				
				
				
				
				
				<li id="alerts--risk-2-confidence-1">
					<h3>
						<span>Risk</span>=<span
							class="risk-level">Medium</span>, <span>Confidence</span>=<span
							class="confidence-level">Low</span> <span>(1)</span>
					</h3>
					<ol>
						
						<li class="alerts--site-li">
							<h4>
								<span class="site">http://localhost:8001</span> <span>(1)</span>
							</h4>
							<ol>
								
								<li>
									<h5>
										<a
											href="#alert-type-0">Absence of Anti-CSRF Tokens</a> <span>(1)</span>
									</h5>
									<ol>
										<li><details>
												<summary>
													<span class="request-method-n-url">GET http://localhost:8001/register</span>
												</summary>
												
<table class="alerts-table">
	<tr>
		<th scope="row">Alert tags</th>
		<td>
			<ul class="alert-tags-list">
				<li>
					<span><a href="https://owasp.org/Top10/A01_2021-Broken_Access_Control/">OWASP_2021_A01</a></span> 
				</li>
				<li>
					 <span>POLICY_QA_STD = </span>
				</li>
				<li>
					 <span>POLICY_PENTEST = </span>
				</li>
				<li>
					<span><a href="https://www.zaproxy.org/docs/desktop/addons/common-library/alerttags/#systemic">SYSTEMIC</a></span> 
				</li>
				<li>
					<span><a href="https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/06-Session_Management_Testing/05-Testing_for_Cross_Site_Request_Forgery">WSTG-v42-SESS-05</a></span> 
				</li>
				<li>
					<span><a href="https://owasp.org/www-project-top-ten/2017/A5_2017-Broken_Access_Control.html">OWASP_2017_A05</a></span> 
				</li>
				<li>
					<span><a href="https://cwe.mitre.org/data/definitions/352.html">CWE-352</a></span> 
				</li>
				<li>
					 <span>POLICY_DEV_STD = </span>
				</li>
			</ul>
		</td>
	</tr>
	<tr>
		<th scope="row">Alert description</th>
		<td> 
<p>No Anti-CSRF tokens were found in a HTML submission form.</p>

<p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p>

<p>CSRF attacks are effective in a number of situations, including:</p>

<p>    * The victim has an active session on the target site.</p>

<p>    * The victim is authenticated via HTTP auth on the target site.</p>

<p>    * The victim is on the same local network as the target site.</p>

<p>CSRF has primarily been used to perform an action against a target site using the victim&#39;s privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
 </td>
	</tr>
	<tr>
		<th scope="row">Other info</th>
		<td> 
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF, _token, _csrf_token, _csrfToken] was found in the following HTML form: [Form 1: &quot;birthdate&quot; &quot;password&quot; &quot;username&quot; ].</p>
 </td>
	</tr>
	<tr>
		<th scope="row">Request</th>
		<td><details open="open">
				<summary>Request line and header section (479 bytes)</summary>
				
				<pre><code>GET http://localhost:8001/register HTTP/1.1
host: localhost:8001
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:145.0) Gecko/20100101 Firefox/145.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Connection: keep-alive
Referer: http://localhost:8001/
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1
Priority: u=0, i

</code></pre>
				
				
			</details> <details class="request-body" open="open">
				<summary>Request body (0 bytes)</summary>
				
				<pre><code></code></pre>
				
				
			</details></td>
	</tr>
	<tr>
		<th scope="row">Response</th>
		<td><details open="open">
				<summary>Status line and header section (325 bytes)</summary>
				
				<pre><code>HTTP/1.1 200 OK
content-type: text/html
content-security-policy: default-src &#39;self&#39;; script-src &#39;self&#39;; style-src &#39;self&#39;; img-src &#39;self&#39;; frame-ancestors &#39;none&#39;; form-action &#39;self&#39;;
x-frame-options: DENY
x-content-type-options: nosniff
vary: Accept-Encoding
content-length: 3026
date: Tue, 02 Dec 2025 15:02:38 GMT

</code></pre>
				
				
			</details> <details class="response-body">
				<summary>Response body (3026 bytes)</summary>
				
				<pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang=&quot;en&quot;&gt;

&lt;head&gt;
    &lt;meta charset=&quot;UTF-8&quot;&gt;
    &lt;meta name=&quot;viewport&quot; content=&quot;width=device-width, initial-scale=1.0&quot;&gt;
    &lt;title&gt;User Registration&lt;/title&gt;
    &lt;link href=&quot;/static/tailwind.css&quot; rel=&quot;stylesheet&quot;&gt; &lt;!-- Link to Tailwind CSS --&gt;
&lt;/head&gt;

&lt;body class=&quot;flex flex-col min-h-screen bg-gray-100 text-gray-900&quot;&gt;
  &lt;main class=&quot;flex-grow&quot;&gt;
    &lt;div class=&quot;container mx-auto p-4&quot;&gt;
        &lt;div class=&quot;bg-white shadow-md rounded-lg p-6 mt-6 max-w-lg mx-auto&quot;&gt;
            &lt;h1 class=&quot;text-2xl font-bold mb-4 text-center&quot;&gt;Register&lt;/h1&gt;
            &lt;form action=&quot;/register&quot; method=&quot;POST&quot;&gt;
                &lt;div class=&quot;mb-4&quot;&gt;
                    &lt;label for=&quot;username&quot; class=&quot;block text-sm font-medium text-gray-700 font-bold&quot;&gt;Email&lt;/label&gt;
                    &lt;input type=&quot;email&quot; id=&quot;username&quot; name=&quot;username&quot; placeholder=&quot;Enter your email&quot; required class=&quot;mt-1 block w-full px-3 py-2 border rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm&quot;&gt;
                &lt;/div&gt;
                &lt;div class=&quot;mb-4&quot;&gt;
                    &lt;label for=&quot;password&quot; class=&quot;block text-sm font-medium text-gray-700 font-bold&quot;&gt;Password&lt;/label&gt;
                    &lt;input type=&quot;password&quot; id=&quot;password&quot; name=&quot;password&quot; placeholder=&quot;Create a password&quot; required class=&quot;mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm&quot;&gt;
                &lt;/div&gt;
                &lt;div class=&quot;mb-4&quot;&gt;
                    &lt;label for=&quot;birthdate&quot; class=&quot;block text-sm font-medium text-gray-700 font-bold&quot;&gt;Birthdate&lt;/label&gt;
                    &lt;input type=&quot;date&quot; id=&quot;birthdate&quot; name=&quot;birthdate&quot; required class=&quot;mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm&quot;&gt;
                &lt;/div&gt;
                &lt;div class=&quot;mb-4&quot;&gt;
                    &lt;label for=&quot;role&quot; class=&quot;block text-sm font-medium text-gray-700 font-bold&quot;&gt;Role&lt;/label&gt;
                    &lt;select id=&quot;role&quot; name=&quot;role&quot; required class=&quot;mt-1 block w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 sm:text-sm&quot;&gt;
                        &lt;option value=&quot;reserver&quot;&gt;Reserver&lt;/option&gt;
                        &lt;option value=&quot;administrator&quot;&gt;Administrator&lt;/option&gt;
                    &lt;/select&gt;
                &lt;/div&gt;
                &lt;div class=&quot;flex justify-between space-x-4&quot;&gt;
                    &lt;button type=&quot;submit&quot; class=&quot;inline-block bg-blue-500 text-white py-2 px-4 rounded hover:bg-blue-600 w-1/2&quot;&gt;Register&lt;/button&gt;
                    &lt;a href=&quot;/&quot; class=&quot;inline-block bg-gray-500 text-white py-2 px-4 rounded hover:bg-gray-600 w-1/2 text-center&quot;&gt;Cancel&lt;/a&gt;
                &lt;/div&gt;
            &lt;/form&gt;
        &lt;/div&gt;
    &lt;/div&gt;
  &lt;/main&gt;
  &lt;div id=&quot;footer-placeholder&quot;&gt;&lt;/div&gt;
  &lt;script src=&quot;/static/footer.js&quot;&gt;&lt;/script&gt;
&lt;/body&gt;

&lt;/html&gt;</code></pre>
				
				
			</details></td>
	</tr>
	
	
	<tr>
		<th scope="row">Evidence</th>
		<td><pre><code>&lt;form action=&quot;/register&quot; method=&quot;POST&quot;&gt;</code></pre></td>
	</tr>
	<tr>
		<th scope="row">Solution</th>
		<td> 
<p>Phase: Architecture and Design</p>

<p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p>

<p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p>

<p>Phase: Implementation</p>

<p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p>

<p>Phase: Architecture and Design</p>

<p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p>

<p>Note that this can be bypassed using XSS.</p>

<p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p>

<p>Note that this can be bypassed using XSS.</p>

<p>Use the ESAPI Session Management control.</p>

<p>This control includes a component for CSRF.</p>

<p>Do not use the GET method for any request that triggers a state change.</p>

<p>Phase: Implementation</p>

<p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
 </td>
	</tr>
</table>

											</details></li>
									</ol>
								</li>
								
							</ol>
						</li>
						
					</ol>
				</li>
				  
				 
				 
				
				
				
				
				<li id="alerts--risk-0-confidence-2">
					<h3>
						<span>Risk</span>=<span
							class="risk-level">Informational</span>, <span>Confidence</span>=<span
							class="confidence-level">Medium</span> <span>(1)</span>
					</h3>
					<ol>
						
						<li class="alerts--site-li">
							<h4>
								<span class="site">http://localhost:8001</span> <span>(1)</span>
							</h4>
							<ol>
								
								<li>
									<h5>
										<a
											href="#alert-type-1">User Agent Fuzzer</a> <span>(1)</span>
									</h5>
									<ol>
										<li><details>
												<summary>
													<span class="request-method-n-url">POST http://localhost:8001/register</span>
												</summary>
												
<table class="alerts-table">
	<tr>
		<th scope="row">Alert tags</th>
		<td>
			<ul class="alert-tags-list">
				<li>
					 <span>CUSTOM_PAYLOADS = </span>
				</li>
				<li>
					 <span>POLICY_PENTEST = </span>
				</li>
				<li>
					<span><a href="https://www.zaproxy.org/docs/desktop/addons/common-library/alerttags/#systemic">SYSTEMIC</a></span> 
				</li>
			</ul>
		</td>
	</tr>
	<tr>
		<th scope="row">Alert description</th>
		<td> 
<p>Check for differences in response based on fuzzed User Agent (eg. mobile sites, access as a Search Engine Crawler). Compares the response statuscode and the hashcode of the response body with the original response.</p>
 </td>
	</tr>
	
	<tr>
		<th scope="row">Request</th>
		<td><details open="open">
				<summary>Request line and header section (287 bytes)</summary>
				
				<pre><code>POST http://localhost:8001/register HTTP/1.1
host: localhost:8001
user-agent: Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)
pragma: no-cache
cache-control: no-cache
content-type: application/x-www-form-urlencoded
referer: http://localhost:8001/register
content-length: 83

</code></pre>
				
				
			</details> <details class="request-body" open="open">
				<summary>Request body (83 bytes)</summary>
				
				<pre><code>username=foo-bar%40example.com&amp;password=ZAP&amp;birthdate=2025-12-02&amp;role=administrator</code></pre>
				
				
			</details></td>
	</tr>
	<tr>
		<th scope="row">Response</th>
		<td><details open="open">
				<summary>Status line and header section (325 bytes)</summary>
				
				<pre><code>HTTP/1.1 200 OK
content-type: text/html
content-security-policy: default-src &#39;self&#39;; script-src &#39;self&#39;; style-src &#39;self&#39;; img-src &#39;self&#39;; frame-ancestors &#39;none&#39;; form-action &#39;self&#39;;
x-frame-options: DENY
x-content-type-options: nosniff
vary: Accept-Encoding
content-length: 1322
date: Tue, 02 Dec 2025 15:10:53 GMT

</code></pre>
				
				
			</details> <details class="response-body" open="open">
				<summary>Response body (1322 bytes)</summary>
				
				<pre><code>&lt;!DOCTYPE html&gt;
&lt;html lang=&quot;en&quot;&gt;

&lt;head&gt;
    &lt;meta charset=&quot;UTF-8&quot;&gt;
    &lt;meta name=&quot;viewport&quot; content=&quot;width=device-width, initial-scale=1.0&quot;&gt;
    &lt;title&gt;Staus&lt;/title&gt;
    &lt;link href=&quot;/static/tailwind.css&quot; rel=&quot;stylesheet&quot;&gt;
&lt;/head&gt;

&lt;body class=&quot;flex flex-col min-h-screen bg-gray-100 text-gray-900&quot;&gt;
    &lt;main class=&quot;flex-grow&quot;&gt;
        &lt;div class=&quot;container mx-auto p-4&quot;&gt;
            &lt;div class=&quot;bg-white shadow-md rounded-lg p-6 mt-6 max-w-lg mx-auto&quot;&gt;
                &lt;h1 class=&quot;text-2xl font-bold mb-4 text-center&quot;&gt;Status&lt;/h1&gt;

                &lt;!-- Status message box --&gt;
                &lt;div id=&quot;status-box&quot; class=&quot;hidden p-4 rounded-md mb-4&quot;&gt;
                    &lt;div id=&quot;status-title&quot; class=&quot;font-bold mb-1&quot;&gt;&lt;/div&gt;
                    &lt;p id=&quot;status-message&quot;&gt;&lt;/p&gt;
                &lt;/div&gt;

                &lt;div class=&quot;flex justify-between space-x-4&quot;&gt;
                    &lt;a href=&quot;/&quot;
                        class=&quot;block w-full bg-blue-500 text-white py-2 px-4 rounded text-center hover:bg-blue-600&quot;&gt;
                        Back to home
                    &lt;/a&gt;
                &lt;/div&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/main&gt;

    &lt;div id=&quot;footer-placeholder&quot;&gt;&lt;/div&gt;
    &lt;script src=&quot;/static/footer.js&quot;&gt;&lt;/script&gt;
    &lt;script src=&quot;/static/status.js&quot;&gt;&lt;/script&gt;
&lt;/body&gt;

&lt;/html&gt;</code></pre>
				
				
			</details></td>
	</tr>
	<tr>
		<th scope="row">Parameter</th>
		<td><pre><code>Header User-Agent</code></pre></td>
	</tr>
	<tr>
		<th scope="row">Attack</th>
		<td><pre><code>Mozilla/4.0 (compatible; MSIE 8.0; Windows NT 6.1)</code></pre></td>
	</tr>
	
	
</table>

											</details></li>
									</ol>
								</li>
								
							</ol>
						</li>
						
					</ol>
				</li>
				
				
				  
			</ol>
		</section>

		<section id="appendix" class="appendix">
			<h2>Appendix</h2>

			<section id="alert-types" class="alert-types">
				<h3>Alert types</h3>
				<p class="alert-types-intro">This section contains additional information on the types of alerts in the report.</p>
				<ol>
					<li
						id="alert-type-0">
						<h4>Absence of Anti-CSRF Tokens</h4>
						<table class="alert-types-table">
							<tr>
								<th scope="row">Source</th>
								<td>
									
									   <span>raised by a passive scanner</span> <span>(<a
										href="https://www.zaproxy.org/docs/alerts/10202/">Absence of Anti-CSRF Tokens</a>)
									</span>   
								</td>
							</tr>
							<tr>
								<th scope="row">CWE ID</th>
								<td><a
									href="https://cwe.mitre.org/data/definitions/352.html">352</a></td>
							</tr>
							<tr>
								<th scope="row">WASC ID</th>
								<td>9</td>
							</tr>
							<tr>
								<th scope="row">Reference</th>
								<td>
									<ol>
										<li><a
											href="https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html">https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html</a></li>
										<li><a
											href="https://cwe.mitre.org/data/definitions/352.html">https://cwe.mitre.org/data/definitions/352.html</a></li>
									</ol>
								</td>
							</tr>
						</table>
					</li>
					<li
						id="alert-type-1">
						<h4>User Agent Fuzzer</h4>
						<table class="alert-types-table">
							<tr>
								<th scope="row">Source</th>
								<td>
									
									   <span>raised by an active scanner</span> <span>(<a
										href="https://www.zaproxy.org/docs/alerts/10104/">User Agent Fuzzer</a>)
									</span>   
								</td>
							</tr>
							
							
							<tr>
								<th scope="row">Reference</th>
								<td>
									<ol>
										<li><a
											href="https://owasp.org/wstg">https://owasp.org/wstg</a></li>
									</ol>
								</td>
							</tr>
						</table>
					</li>
				</ol>
			</section>
		</section>
		 
	</main>
</body>
</html>



