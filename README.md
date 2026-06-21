# Password-Shield
Password shield - Password Strength Analyzer


A professional-grade password strength analysis tool built with vanilla JavaScript, Tailwind CSS, and advanced entropy calculations.

🎯 Purpose

PasswordShield teaches users about password security by analyzing their passwords in real-time and providing:


Strength scoring based on cryptographic entropy
Vulnerability detection (common patterns, weak characteristics)
Time-to-crack estimation (100 billion guesses/second baseline)
Actionable suggestions for improvement


Status: Built as part of IIT Kanpur B.Cyber Program application (June 2026)


✨ Features

🔍 Real-Time Analysis


Instant feedback as you type
Circular progress indicator
Linear strength bar with color coding
No server communication (all client-side)


📊 Advanced Metrics


Length Analysis: Character count and minimum recommendations
Entropy Calculation: Mathematical strength using Shannon entropy formula
Charset Detection: Identifies uppercase, lowercase, numbers, special characters
Time-to-Crack: Estimates cracking time with realistic assumptions


⚠️ Vulnerability Detection

Automatically identifies:


Insufficient length (< 8 characters)
Missing character types (uppercase, lowercase, numbers, symbols)
Repeated characters (aaa, bbb, etc.)
Common patterns (123456, password, qwerty, etc.)
Low entropy warnings


💡 Smart Suggestions


Context-aware recommendations
Specific guidance on which character types to add
Strategy tips for improving security
Congratulations when password is strong


🎨 Cyberpunk UI


Dark theme optimized for security professionals
Neon green/cyan glow effects
Real-time system console
Professional developer interface
Password visibility toggle (👁️ Show/Hide)



🚀 Quick Start

Option 1: Live Demo

Visit link: https://fluffy-kelpie-63480a.netlify.app/

Option 2: Run Locally


Download password-checker.html
Open in browser:


bash   # macOS
   open password-checker.html
   
   # Linux
   xdg-open password-checker.html
   
   # Windows
   start password-checker.html


Or use local server:


bash   python -m http.server 8000
   # Visit http://localhost:8000/password-checker.html


📖 How to Use


Enter a password in the input field
Real-time analysis shows:

Circular strength indicator (0-100%)
Linear progress bar with color coding
Password metrics (length, entropy, charset)
Time-to-crack estimation



Review vulnerabilities on the right panel
Apply suggestions to improve your password
Toggle visibility (👁️) to see/hide your password


Password Strength Levels


🔴 WEAK (0-39%): Not recommended
🟠 FAIR (40-59%): Acceptable but improvable
🟡 GOOD (60-79%): Recommended
🟢 EXCELLENT (80-100%): Highly secure



🔐 Technical Details

Entropy Calculation

Uses Shannon entropy formula:

Entropy = log₂(charset_size ^ password_length)

Example:


Password: "MyP@ssw0rd123" (13 chars)
Charset: lowercase (26) + uppercase (26) + numbers (10) + symbols (32) = 94 possible characters
Entropy = log₂(94^13) ≈ 86 bits


Time-to-Crack Estimation

Assumes attacker can make 100 billion guesses per second:

Time = 2^entropy / 100,000,000,000

For 86 bits: ~1,153 years to crack

Vulnerability Detection

Checks for:


Character type requirements (NIST guidelines)
Common patterns (top 100 weak passwords)
Repeated characters (test in teeeest)
Sequential patterns (detected via regex)
Low entropy thresholds



🛠️ Technical Stack


Frontend: Vanilla JavaScript (no frameworks)
Styling: Tailwind CSS (via CDN)
Cryptography: Shannon entropy calculation (educational)
Deployment: GitHub Pages / Netlify (static site)
Browser Support: Modern browsers (Chrome, Firefox, Safari, Edge)



🎓 Learning Outcomes

Using PasswordShield, you'll understand:


Password Entropy: Why randomness matters more than just length
Character Diversity: Why mixed character types strengthen passwords
Vulnerability Patterns: Common mistakes hackers exploit
Security Metrics: How to quantify password strength mathematically
Real-World Implications: Time/resources needed to crack passwords



🔐 Security & Privacy

✅ 100% Client-Side:


All analysis happens in your browser
Your password is never sent anywhere
No server logs or databases
No cookies or tracking


⚠️ Educational Use Only:


Not a cryptographic implementation library
Entropy calculation is for demonstration
Not suitable for protecting actual sensitive data



📊 Example Analysis

Strong Password: "Tr0p!cal$unset#2024"

Length: 19 characters
Charset: 94 possible characters
Entropy: 125.4 bits
Time to Crack: 4 trillion years
Strength: 98%

Weak Password: "password123"

Length: 11 characters
Charset: 36 possible characters
Entropy: 57.1 bits
Time to Crack: 23 seconds
Strength: 35%
Vulnerabilities:
  - Contains common word "password"
  - Numbers only at the end
  - Missing special characters


🚀 Deployment (Netlify / GitHub Pages)




📝 Version History


v1.0 (June 2026) — Initial release with entropy analysis, vulnerability detection, real-time feedback



📚 References


NIST Password Guidelines: https://pages.nist.gov/800-63-3/
Shannon Entropy: https://en.wikipedia.org/wiki/Entropy_(information_theory)
Password Security Best Practices: https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html



Built with ❤️ for cybersecurity learners

Questions? Issues? Improvements? This is an educational tool—feedback helps it get better!
