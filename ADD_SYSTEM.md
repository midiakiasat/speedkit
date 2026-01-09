# Procedure: Add New System to speedkit.eu

## Prerequisites
- System name in uppercase (e.g., "SYSTEMNAME")
- System directory name in lowercase (e.g., "systemname")
- System execution definition (one sentence)
- System boundaries (what it does NOT do)
- Entry point URL
- Output/proof description
- Termination conditions
- Access rules
- Archive guarantee statement
- Authoritative specification URL

## Steps

### 1. Create System Directory
```bash
mkdir <systemname>
```

### 2. Create System Page
Create `<systemname>/index.html` with this exact structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title><SYSTEMNAME></title>
    <link rel="stylesheet" href="../styles.css">
</head>
<body>
    <main>
        <nav><a href="../index.html">speedkit.eu</a></nav>
        
        <h1><SYSTEMNAME></h1>
        
        <section>
            <p><SYSTEMNAME> executes [execution definition].</p>
        </section>
        
        <section>
            <h2>What this system does NOT do</h2>
            <ul>
                <li>Does not execute support operations</li>
                <li>Does not execute feature modifications</li>
                <li>Does not execute third-party integrations</li>
                <li>Does not store data after execution terminates</li>
            </ul>
        </section>
        
        <section>
            <h2>Entry point</h2>
            <p>[canonical execution endpoint URL - must be real, not subdomain promise]</p>
        </section>
        
        <section>
            <h2>Output / proof produced</h2>
            <p>[output description with evidence]</p>
        </section>
        
        <section>
            <h2>Termination condition</h2>
            <p>[termination conditions]</p>
        </section>
        
        <section>
            <h2>Pricing or access rule</h2>
            <p>Execution is publicly accessible. Input validation occurs before execution begins.</p>
            <p>OR (if license-gated):</p>
            <p>Execution requires possession of a valid execution token. Tokens are validated at invocation time.</p>
            <p>NEVER use "authentication" - it implies identity. Use capability, not identity.</p>
        </section>
        
        <section>
            <h2>Exit / archive guarantee</h2>
            <p>After termination, system outputs remain accessible. System code does not execute after termination. Execution artifacts are produced at termination. Long-term retention is defined by the authoritative specification.</p>
        </section>
        
        <section>
            <h2>Authoritative specification</h2>
            <p><a href="[specification URL]">[specification URL]</a></p>
        </section>
    </main>
</body>
</html>
```

### 3. Update Root Index
In `index.html`, add one line to the Systems list:

**Before:**
```html
            <ul>
                <li><a href="verifrax/index.html">VERIFRAX</a></li>
                <li><a href="mk10-pro/index.html">MK10-PRO</a></li>
                <li><a href="vatfix/index.html">VATFIX</a></li>
            </ul>
```

**After:**
```html
            <ul>
                <li><a href="verifrax/index.html">VERIFRAX</a></li>
                <li><a href="mk10-pro/index.html">MK10-PRO</a></li>
                <li><a href="vatfix/index.html">VATFIX</a></li>
                <li><a href="<systemname>/index.html"><SYSTEMNAME></a></li>
            </ul>
```

### 4. Update robots.txt
Add one Disallow line:

**Before:**
```
User-agent: *
Allow: /
Disallow: /verifrax/
Disallow: /mk10-pro/
Disallow: /vatfix/
```

**After:**
```
User-agent: *
Allow: /
Disallow: /verifrax/
Disallow: /mk10-pro/
Disallow: /vatfix/
Disallow: /<systemname>/
```

### 5. Deploy
- Commit changes
- Push to repository
- Cloudflare Pages will auto-deploy
- No downtime (static files are atomic)

## Rules
- Do NOT modify existing system pages
- Do NOT modify styles.css
- Do NOT modify _headers
- Do NOT change existing index.html content except adding the new list item
- Do NOT change existing robots.txt content except adding the new Disallow line
- New system must follow exact template structure
- All content must describe execution, boundary, evidence, or termination
- No adjectives, no marketing language, no emotional language
- Entry point must be canonical execution endpoint (not subdomain promise)
- Never use "authentication" - use capability-based access language
- Archive guarantee must push retention responsibility to authoritative specification

## Verification
After deployment, verify:
- `https://speedkit.eu/<systemname>` loads correctly
- Link appears in root index
- robots.txt includes new Disallow rule
- All existing systems remain unchanged
