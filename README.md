# LeakSee

**Was your data leaked?** Check if your email or password has been exposed in a data breach, or browse 700+ known breaches — all for free, no account needed.

## Features

- **Email Breach Check** — Instantly verify if your email address appears in known data breaches
- **Password Strength Check** — Test if a password has been exposed in any breach using k-anonymity (your password never leaves your device)
- **Breach Database Browser** — Search and explore over 700 public breaches with detailed information about each incident
- **Privacy-First Design** — All checks use industry-standard security practices; your data is never stored

## How It Works

### Email Check
- Queries the **XposedOrNot** breach database in real-time
- Your email is sent directly to the API; never stored
- Shows which breaches exposed your email (if any)

### Password Check
- Uses **HaveIBeenPwned Passwords API** with k-anonymity
- Only the first 5 characters of your password's SHA-1 hash are transmitted
- The full password and complete hash remain on your device
- Safely checks against billions of compromised passwords

### Breach Browser
- Displays comprehensive data from the **HaveIBeenPwned breach database**
- Sort by number of accounts affected
- View breach details: dates, affected data types, verification status
- Search across 700+ known incidents

## Getting Started

### Installation

No build process required! This is a single-file HTML application.

1. **Clone or download** the repository
   ```bash
   git clone https://github.com/yourusername/LeakSee.git
   cd LeakSee
   ```

2. **Open in browser**
   - Simply open `index.html` in any modern web browser
   - No server or dependencies needed

### Usage

1. **Switch between tabs** at the top to select a check type
2. **Email Check**: Enter your email address and click "Check Email"
3. **Password Check**: Enter a password and click "Check Password"
4. **Browse Breaches**: Search by company name or scroll through the full database

## Security & Privacy

- ✅ **No backend server** — All processing happens in your browser
- ✅ **HTTPS only** — All external API calls use encryption
- ✅ **Password k-anonymity** — Only 5-character hash prefix sent, never the full hash
- ✅ **No data retention** — Your queries are never logged or stored
- ✅ **XSS protection** — HTML input is properly escaped to prevent injection attacks

## Technology Stack

- **HTML5** — Semantic markup structure
- **CSS3** — Modern styling with CSS custom properties (variables), responsive design
- **Vanilla JavaScript** — No frameworks or dependencies required
- **External APIs**:
  - [XposedOrNot API](https://xposedornot.com) — Email breach data
  - [HaveIBeenPwned Passwords API](https://haveibeenpwned.com/passwords) — Password breach data
  - [HaveIBeenPwned API v3](https://haveibeenpwned.com/api/v3) — Breach database

## Browser Compatibility

- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

Requires ES2017+ support (async/await, fetch API, Web Crypto API)

## Features in Detail

### Responsive Design
- Optimized for desktop, tablet, and mobile
- Touch-friendly interface
- Accessible color contrast (WCAG compliant)

### Error Handling
- Graceful fallbacks if APIs are unavailable
- Clear error messages for invalid input
- Network error recovery

### Performance
- Fast initial load (single HTML file, ~80KB)
- Lazy loading for breach logos
- Pagination (shows first 80 breaches, searchable)
- Smooth animations and transitions

## Known Limitations

- Email check depends on XposedOrNot API availability
- Password check limited to breaches indexed by HaveIBeenPwned
- Breach database updates depend on HIBP's data refresh schedule
- Search limited to first 80 results for performance

## Contributing

Contributions welcome! Please feel free to:
- Report bugs or security issues
- Suggest features or UI improvements
- Improve documentation
- Optimize performance

## License

MIT License — Feel free to use, modify, and distribute

## Acknowledgments

Data powered by:
- **[HaveIBeenPwned](https://haveibeenpwned.com)** by Troy Hunt — Comprehensive breach database
- **[XposedOrNot](https://xposedornot.com)** — Email breach lookups
- Icons by [Feather Icons](https://feathericons.com)
- Typography: Inter & Outfit fonts by Google Fonts

## Disclaimer

This tool is provided "as is" for informational purposes. While we strive for accuracy, LeakSee does not guarantee the completeness or real-time accuracy of breach data. Always practice strong password hygiene and enable two-factor authentication on important accounts.

---

**Questions or feedback?** Open an issue or contact the maintainers.

**Stay safe! 🔒**
