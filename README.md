my website # landing-page
landing page for clearwater
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Clearwater — Clean water, clear future</title>

  <!-- Optional: Google font (remove if you prefer system fonts) -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Merriweather:wght@400;700&display=swap" rel="stylesheet">

  <style>
    /* -------------------------
       BRAND COLORS (from image)
       ------------------------- */
    :root{
      --dark: #12110d;          /* very dark */
      --olive: #8b8a6c;         /* headline strip */
      --beige: #dcdccf;         /* big left copy */
      --sea: #7fb7b0;           /* mission box */
      --accent-warm: #5e3521;   /* warm brown for small accents */
      --muted-white: rgba(255,255,255,0.95);
    }

    /* Reset / base */
    * { box-sizing: border-box; }
    html,body { height:100%; margin:0; font-family: 'Inter', system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial; color:var(--dark); line-height:1.45; }
    img { max-width:100%; display:block; }

    /* Page container with a subtle background image effect (replace or keep) */
    .page {
      min-height:100vh;
      padding:28px;
      background:
        radial-gradient(ellipse at center, rgba(0,0,0,0.25) 0%, rgba(0,0,0,0.65) 100%),
        url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="800" height="500"><rect width="100%" height="100%" fill="%23131b16"/></svg>');
      background-size:cover;
      background-attachment:fixed;
      display:flex;
      align-items:center;
      justify-content:center;
    }

    .card {
      width:100%;
      max-width:1100px;
      display:grid;
      gap:28px;
      grid-template-columns: 1fr 420px;
      align-items:start;
    }

    /* headline strip */
    .headline {
      grid-column: 1 / -1;
      background:var(--olive);
      color:var(--muted-white);
      padding:18px 26px;
      border-radius:6px;
      text-align:center;
      font-family:'Merriweather', serif;
      font-size:1.45rem;
      letter-spacing:0.2px;
    }

    /* Left column (text blocks stacked) */
    .left {
      display:flex;
      flex-direction:column;
      gap:22px;
    }

    .panel {
      padding:26px;
      border-radius:6px;
      box-shadow: 0 6px 18px rgba(0,0,0,0.25);
    }

    .panel.beige {
      background:var(--beige);
      color:var(--dark);
      font-size:1.05rem;
      line-height:1.6;
    }

    .panel.sea {
      background:var(--sea);
      color:var(--muted-white);
      font-size:0.98rem;
    }

    /* Right column with two framed images */
    .right {
      display:flex;
      flex-direction:column;
      gap:28px;
      justify-content:flex-start;
      align-items:stretch;
    }

    .photo-frame {
      background:linear-gradient(180deg, rgba(0,0,0,0.7), rgba(0,0,0,0.6));
      padding:14px;
      border-radius:6px;
      display:block;
      box-shadow:0 10px 30px rgba(0,0,0,0.5);
    }

    /* create the decorative black geometric crop like the Canva corner blocks */
    .photo-frame .photo {
      position:relative;
      overflow:hidden;
      border-radius:3px;
      border: 10px solid #000; /* heavy black border like Canva style */
      display:block;
    }

    .photo-frame .photo img {
      width:100%;
      height:100%;
      object-fit:cover;
      display:block;
    }

    /* CTA row (span full width) */
    .cta-row {
      grid-column: 1 / -1;
      margin-top:4px;
      display:flex;
      gap:12px;
      align-items:center;
      justify-content:space-between;
      flex-wrap:wrap;
    }

    .cta-left {
      display:flex;
      gap:12px;
      align-items:center;
    }

    .title-cta {
      color:var(--muted-white);
      font-weight:600;
      font-family:'Merriweather', serif;
      font-size:1.05rem;
      margin:0;
    }

    .buttons {
      display:flex;
      gap:12px;
      align-items:center;
    }

    .btn {
      padding:10px 18px;
      border-radius:6px;
      font-weight:600;
      text-decoration:none;
      display:inline-block;
      cursor:pointer;
      border:2px solid transparent;
    }

    .btn-primary {
      background:var(--accent-warm);
      color:var(--muted-white);
      border-color:rgba(0,0,0,0.12);
    }

    .btn-ghost {
      background:transparent;
      color:var(--muted-white);
      border:1.5px solid rgba(255,255,255,0.18);
    }

    /* small note under CTA */
    .note {
      color:rgba(255,255,255,0.8);
      font-size:0.92rem;
      margin-top:6px;
    }

    /* Responsive */
    @media (max-width:980px){
      .card { grid-template-columns: 1fr; padding-bottom:32px; }
      .right { order: -1; } /* show images above text on narrow screens */
      .headline { font-size:1.15rem; padding:14px; }
    }

    @media (max-width:480px){
      .panel { padding:18px; font-size:0.98rem; }
      .photo-frame { padding:8px; }
    }
  </style>
</head>
<body>

  <main class="page">
    <div class="card">

      <!-- Headline strip across the top -->
      <div class="headline">Clean water, clear future</div>

      <!-- Left column: copy blocks -->
      <div class="left">

        <!-- Big beige copy block that matches Canva left box -->
        <section class="panel beige" aria-label="Children deserve more">
          <h2 style="margin-top:0; font-family:'Merriweather', serif; font-weight:700;">Children deserve more than survival — they deserve opportunity.</h2>
          <p style="margin:12px 0 0;">
            Clearwater is committed to giving every child access to clean water and the resources they need to grow up healthy, safe, and hopeful for the future. We partner with communities to design solutions that last.
          </p>
        </section>

        <!-- Small sea-green mission box -->
        <section class="panel sea" aria-label="mission">
          <h3 style="margin-top:0; font-weight:700;">Our mission</h3>
          <p style="margin:8px 0 0;">
            At Clearwater our mission is to provide clean, safe, and consumable water to communities that need it. We do this by respecting ways of living and designing sustainable systems that create long-term opportunity.
          </p>
        </section>

      </div> <!-- /left -->

      <!-- Right column: stacked photos -->
      <aside class="right" aria-label="Imagery">

        <!-- Top photo framed -->
        <div class="photo-frame" aria-hidden="false">
          <div class="photo" style="height:330px;">
            <!-- Replace this src with your real hero photo -->
            <img src="https://via.placeholder.com/640x480.png?text=Child+with+water+%28replace%29" alt="Child holding a glass of water">
          </div>
        </div>

        <!-- Bottom photo framed -->
        <div class="photo-frame" aria-hidden="false">
          <div class="photo" style="height:260px;">
            <!-- Replace this src with your real pump/field photo -->
            <img src="https://via.placeholder.com/640x480.png?text=Community+Water+Pump+%28replace%29" alt="Community water pump">
          </div>
        </div>

      </aside>

      <!-- CTA row that spans full width -->
      <div class="cta-row">
        <div>
          <p class="title-cta">Help provide clean water today.</p>
          <p class="note">Your contribution helps build wells, maintain systems, and train local stewards so water stays safe and available.</p>
        </div>

        <div class="buttons" role="group" aria-label="Primary actions">
          <a class="btn btn-primary" href="#" onclick="alert('Replace with donate link')">Donate</a>
          <a class="btn btn-ghost" href="#" onclick="alert('Replace with learn-more anchor')">Learn More</a>
        </div>
      </div>

    </div> <!-- /card -->
  </main>

</body>
</html>
