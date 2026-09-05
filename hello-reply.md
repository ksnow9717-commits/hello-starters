# Short personalized "Hello?" reply

Hi BenFrank — I’m your friendly guide. You’re not alone; I’ll walk you through step‑by‑step.

## What a CTA is
- CTA = "call to action" — one simple instruction that tells the person what to do next (e.g., “Reply with A, B or C,” “Click Run,” or “Send me your name”). It nudges the user to take the next step.

## Quick 5‑minute starter (for a first-time user)
1) Goal — Ask one line: “What do you want to do?” (example: “I want to see my first web page.”)  
2) Try — give this exact instruction:
   - Online (CodePen): Open https://codepen.io → New Pen → paste the HTML below into the HTML panel → Click “Run”.
   - Offline: Save the HTML below as `hello.html`, then open it in your browser.

### HTML you can paste (it uses the visitor’s name when given, otherwise shows "friend"):
```html
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Hello!</title>
    <style>body{font-family:system-ui,Segoe UI,Roboto,Helvetica,Arial;margin:24px}</style>
  </head>
  <body>
    <h1 id="greeting">Hello, friend!</h1>
    <p>This is your first web page — you made it!</p>
    <script>
      // Use a name passed by URL (/?name=Ben) or prompt the user once,
      // otherwise fall back to 'friend'.
      const urlName = new URLSearchParams(location.search).get('name');
      const stored = localStorage.getItem('visitorName');
      const askName = () => {
        const n = prompt('What is your name? (or leave blank)');
        if (n) localStorage.setItem('visitorName', n);
        return n;
      };
      const name = urlName || stored || askName() || 'friend';
      document.getElementById('greeting').textContent = `Hello, ${name}!`;
    </script>
  </body>
</html>
```

## Short 1‑week path (10 minutes/day)
- Days 1–2: Edit the text in the HTML and re-open the file.
- Days 3–4: Change the page color or font (I’ll show CSS).
- Days 5–7: Add one photo and three facts about yourself.

## CTA (what to do now)
- Reply with one of:
  - A — Learn basics
  - B — Build something together now
  - C — Get the 1‑week roadmap
Or give your name (e.g., “Ryan”) and I’ll personalize the reply automatically.
