<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infant Development Plan</title>
    <style>
        :root {
            --primary: #4A90E2;
            --secondary: #50E3C2;
            --accent: #F5A623;
            --bg: #F9F9F9;
            --text: #333;
            --card-bg: #ffffff;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            color: var(--text);
            margin: 0;
            padding: 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            margin-bottom: 30px;
        }

        h1 {
            color: var(--primary);
            margin-bottom: 5px;
        }

        p.subtitle {
            color: #666;
            font-size: 0.9rem;
        }

        /* Tabs */
        .tabs {
            display: flex;
            justify-content: space-around;
            background: #fff;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            padding: 5px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }

        .tab-btn {
            background: none;
            border: none;
            padding: 10px 20px;
            font-size: 1rem;
            cursor: pointer;
            color: #777;
            border-radius: 8px;
            transition: all 0.3s ease;
            font-weight: 600;
        }

        .tab-btn.active {
            background-color: var(--primary);
            color: white;
            box-shadow: 0 2px 4px rgba(74, 144, 226, 0.3);
        }

        .tab-btn:hover:not(.active) {
            background-color: #f0f0f0;
        }

        /* Content Sections */
        .schedule-section {
            display: none;
            animation: fadeIn 0.5s;
        }

        .schedule-section.active {
            display: block;
        }

        /* Cards */
        .card {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.05);
            border-left: 5px solid var(--secondary);
        }

        .card h3 {
            margin-top: 0;
            color: var(--primary);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .time-block {
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #eee;
        }

        .time-block:last-child {
            border-bottom: none;
        }

        .time {
            font-weight: bold;
            color: var(--accent);
            display: block;
            margin-bottom: 4px;
        }

        .activity {
            font-weight: 600;
            color: #444;
        }

        .desc {
            font-size: 0.9rem;
            color: #666;
        }

        .focus-tag {
            display: inline-block;
            padding: 2px 8px;
            border-radius: 4px;
            font-size: 0.75rem;
            background: #eee;
            margin-left: 5px;
            color: #555;
        }

        /* Focus Areas */
        .focus-area {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 20px;
        }

        .focus-box {
            background: white;
            padding: 15px;
            border-radius: 8px;
            text-align: center;
            border: 1px solid #eee;
        }

        .focus-icon {
            font-size: 1.5rem;
            margin-bottom: 5px;
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @media (max-width: 600px) {
            .tab-btn {
                flex: 1 1 40%;
                margin: 2px;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>

<div class="container">
    <header>
        <h1>Baby Growth Tracker</h1>
        <p class="subtitle">Daily Routines for a Smart, Energetic & Good Citizen</p>
    </header>

    <div class="tabs">
        <button class="tab-btn active" onclick="openTab('phase1')">0-3 Months</button>
        <button class="tab-btn" onclick="openTab('phase2')">4-6 Months</button>
        <button class="tab-btn" onclick="openTab('phase3')">7-9 Months</button>
        <button class="tab-btn" onclick="openTab('phase4')">10-12 Months</button>
    </div>

    <div id="phase1" class="schedule-section active">
        <div class="focus-area">
            <div class="focus-box">
                <span class="focus-icon">🧠</span>
                <strong>High Contrast</strong>
                <p style="font-size:0.8rem">Black & white cards, face time.</p>
            </div>
            <div class="focus-box">
                <span class="focus-icon">⚡</span>
                <strong>Tummy Time</strong>
                <p style="font-size:0.8rem">1-2 mins, 3x daily.</p>
            </div>
            <div class="focus-box">
                <span class="focus-icon">🤝</span>
                <strong>Trust</strong>
                <p style="font-size:0.8rem">Respond to every cry.</p>
            </div>
        </div>

        <div class="card">
            <h3>Routine: Eat, Play, Sleep</h3>
            <div class="time-block">
                <span class="time">Morning (7:00 AM - 8:30 AM)</span>
                <div class="activity">Wake Up & Feed</div>
                <div class="desc">Open curtains immediately (circadian rhythm). Feed.</div>
                <div class="activity" style="margin-top:5px">Active Play</div>
                <div class="desc">Tummy time on chest or floor. Talk to baby face-to-face.</div>
            </div>
            <div class="time-block">
                <span class="time">Mid-Morning (8:30 AM - 10:00 AM)</span>
                <div class="activity">First Nap</div>
                <div class="desc">Swaddle, dark room, white noise.</div>
            </div>
            <div class="time-block">
                <span class="time">Afternoon Cycle (Repeats every 2-3 hrs)</span>
                <div class="activity">Sensory Play</div>
                <div class="desc">Wear baby in a carrier, go for a walk, narrator your life ("I am washing a dish").</div>
            </div>
            <div class="time-block">
                <span class="time">Evening (6:30 PM)</span>
                <div class="activity">Bedtime Routine</div>
                <div class="desc">Bath, massage (tactile stimulation), feed, lights out.</div>
            </div>
        </div>
    </div>

    <div id="phase2" class="schedule-section">
        <div class="focus-area">
            <div class="focus-box">
                <span class="focus-icon">🧠</span>
                <strong>Cause & Effect</strong>
                <p style="font-size:0.8rem">Rattles, crinkle paper.</p>
            </div>
            <div class="focus-box">
                <span class="focus-icon">⚡</span>
                <strong>Rolling</strong>
                <p style="font-size:0.8rem">Reach for toys on floor.</p>
            </div>
            <div class="focus-box">
                <span class="focus-icon">🤝</span>
                <strong>Emotion</strong>
                <p style="font-size:0.8rem">Mirror play & mimicry.</p>
            </div>
        </div>

        <div class="card">
            <h3>Routine: The Explorer</h3>
            <div class="time-block">
                <span class="time">Morning (7:00 AM)</span>
                <div class="activity">Wake & Milk</div>
                <div class="desc">Diaper change with "tickle games" to build connection.</div>
            </div>
            <div class="time-block">
                <span class="time">Playtime (Awake window 90 mins)</span>
                <div class="activity">Floor Gym</div>
                <div class="desc">Place toys just out of reach to encourage rolling. Mirror time.</div>
            </div>
            <div class="time-block">
                <span class="time">Mid-Day</span>
                <div class="activity">Sensory Integration</div>
                <div class="desc">Go outside. Touch leaves, grass, feel the wind (grounding).</div>
            </div>
            <div class="time-block">
                <span class="time">Evening (5:30 PM)</span>
                <div class="activity">Wind Down</div>
                <div class="desc">Read a simple board book. They learn the rhythm of your voice.</div>
            </div>
        </div>
    </div>

    <div id="phase3" class="schedule-section">
        <div class="focus-area">
            <div class="focus-box">
                <span class="focus-icon">🧠</span>
                <strong>Object Permanence</strong>
                <p style="font-size:0.8rem">Peek-a-boo, hiding toys.</p>
            </div>
            <div class="focus-box">
                <span class="focus-icon">⚡</span>
                <strong>Fine Motor</strong>
                <p style="font-size:0.8rem">Pincer grasp (finger food).</p>
            </div>
            <div class="focus-box">
                <span class="focus-icon">🤝</span>
                <strong>Social Eating</strong>
                <p style="font-size:0.8rem">Eat dinner as a family.</p>
            </div>
        </div>

        <div class="card">
            <h3>Routine: The Scientist</h3>
            <div class="time-block">
                <span class="time">Morning (7:00 AM)</span>
                <div class="activity">Solid Breakfast</div>
                <div class="desc">High chair time. Offer oatmeal or mashed fruit. Let them make a mess (physics learning).</div>
            </div>
            <div class="time-block">
                <span class="time">Mid-Morning</span>
                <div class="activity">Obstacle Course</div>
                <div class="desc">Pillows on the floor to crawl over. Builds core and confidence.</div>
            </div>
            <div class="time-block">
                <span class="time">Afternoon</span>
                <div class="activity">Sign Language</div>
                <div class="desc">Practice "More", "Milk", "All Done" during play and snacks.</div>
            </div>
            <div class="time-block">
                <span class="time">Evening</span>
                <div class="activity">Separation Practice</div>
                <div class="desc">Play "I'm leaving the room" and coming back. Builds security.</div>
            </div>
        </div>
    </div>

    <div id="phase4" class="schedule-section">
        <div class="focus-area">
            <div class="focus-box">
                <span class="focus-icon">🧠</span>
                <strong>Problem Solving</strong>
                <p style="font-size:0.8rem">Stacking cups, shape sorters.</p>
            </div>
            <div class="focus-box">
                <span class="focus-icon">⚡</span>
                <strong>Cruising</strong>
                <p style="font-size:0.8rem">Pulling up on furniture.</p>
            </div>
            <div class="focus-box">
                <span class="focus-icon">🤝</span>
                <strong>Citizenship</strong>
                <p style="font-size:0.8rem">"Clean up" time & gentle hands.</p>
            </div>
        </div>

        <div class="card">
            <h3>Routine: The Participant</h3>
            <div class="time-block">
                <span class="time">Morning</span>
                <div class="activity">Independent Play (15 mins)</div>
                <div class="desc">Let them play safely alone while you watch. Builds focus.</div>
            </div>
            <div class="time-block">
                <span class="time">Mid-Day</span>
                <div class="activity">Errands / Social</div>
                <div class="desc">Grocery store trip. Point at items and name them ("Red apple"). Socialize with cashiers.</div>
            </div>
            <div class="time-block">
                <span class="time">Afternoon</span>
                <div class="activity">Music & Movement</div>
                <div class="desc">Clap to music, bang on pots/pans.</div>
            </div>
            <div class="time-block">
                <span class="time">Evening</span>
                <div class="activity">Clean Up Ritual</div>
                <div class="desc">Help them put one toy in the bin. Sing a clean-up song.</div>
            </div>
        </div>
    </div>

</div>

<script>
    function openTab(phaseId) {
        // Hide all schedule sections
        const sections = document.querySelectorAll('.schedule-section');
        sections.forEach(section => {
            section.classList.remove('active');
        });

        // Deactivate all tab buttons
        const buttons = document.querySelectorAll('.tab-btn');
        buttons.forEach(btn => {
            btn.classList.remove('active');
        });

        // Show the selected section
        document.getElementById(phaseId).classList.add('active');
        
        // Activate the clicked button (find the button that called this function)
        const activeBtn = Array.from(buttons).find(btn => btn.getAttribute('onclick').includes(phaseId));
        if (activeBtn) activeBtn.classList.add('active');
    }
</script>

</body>
</html>
