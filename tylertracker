<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tyler, The Creator - Unreleased Music Tracker</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #ff4081;
            --secondary: #3f51b5;
            --dark: #121212;
            --light: #f5f5f5;
            --gray: #424242;
        }

        body {
            background-color: var(--dark);
            color: var(--light);
            line-height: 1.6;
        }

        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            padding: 1.5rem;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
        }

        .logo {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .logo i {
            font-size: 2.5rem;
        }

        .logo h1 {
            font-size: 2rem;
            font-weight: 700;
        }

        .tagline {
            font-size: 1.1rem;
            opacity: 0.9;
            max-width: 600px;
            margin: 0 auto;
        }

        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1.5rem;
        }

        .intro {
            text-align: center;
            margin-bottom: 2rem;
            padding: 1.5rem;
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
        }

        .intro h2 {
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .intro p {
            max-width: 800px;
            margin: 0 auto;
        }

        .filter-container {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 2rem;
            flex-wrap: wrap;
        }

        .filter-btn {
            background-color: var(--gray);
            color: var(--light);
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .filter-btn:hover {
            background-color: var(--primary);
        }

        .filter-btn.active {
            background-color: var(--primary);
        }

        .music-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        .track-card {
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
        }

        .track-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }

        .track-image {
            height: 180px;
            width: 100%;
            object-fit: cover;
        }

        .track-info {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .track-title {
            font-size: 1.3rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }

        .track-meta {
            display: flex;
            justify-content: space-between;
            margin-bottom: 1rem;
            font-size: 0.9rem;
            color: #aaa;
        }

        .track-description {
            margin-bottom: 1.5rem;
            flex-grow: 1;
        }

        .audio-player {
            width: 100%;
            margin-top: auto;
        }

        .player-controls {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-top: 1rem;
        }

        .play-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .play-btn:hover {
            transform: scale(1.1);
        }

        .progress-container {
            flex-grow: 1;
            height: 6px;
            background-color: var(--gray);
            border-radius: 3px;
            cursor: pointer;
            position: relative;
        }

        .progress-bar {
            height: 100%;
            background-color: var(--primary);
            border-radius: 3px;
            width: 0%;
        }

        .time {
            font-size: 0.8rem;
            color: #aaa;
            min-width: 80px;
            text-align: right;
        }

        footer {
            background-color: rgba(0, 0, 0, 0.5);
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
        }

        .footer-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 1.5rem 0;
        }

        .social-links a {
            color: var(--light);
            font-size: 1.5rem;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: var(--primary);
        }

        .copyright {
            font-size: 0.9rem;
            color: #aaa;
        }

        @media (max-width: 768px) {
            .music-grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
            
            .logo h1 {
                font-size: 1.7rem;
            }
            
            .tagline {
                font-size: 1rem;
            }
        }

        @media (max-width: 480px) {
            .music-grid {
                grid-template-columns: 1fr;
            }
            
            .filter-container {
                flex-direction: column;
                align-items: center;
            }
            
            .filter-btn {
                width: 80%;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">
            <i class="fas fa-music"></i>
            <h1>Tyler, The Creator</h1>
        </div>
        <p class="tagline">Unreleased Music Tracker - Discover rare tracks, demos, and unreleased gems</p>
    </header>

    <div class="container">
        <section class="intro">
            <h2>Explore Tyler's Hidden Catalog</h2>
            <p>This collection features unreleased tracks, demos, and rare recordings from Tyler, The Creator's creative journey. From early Odd Future days to recent unreleased gems.</p>
        </section>

        <div class="filter-container">
            <button class="filter-btn active">All Tracks</button>
            <button class="filter-btn">Early Demos</button>
            <button class="filter-btn">Collaborations</button>
            <button class="filter-btn">Live Versions</button>
        </div>

        <div class="music-grid">
            <!-- Track 1 -->
            <div class="track-card">
                <img src="https://images.unsplash.com/photo-1571330735066-03aaa9429d89?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Track Cover" class="track-image">
                <div class="track-info">
                    <h3 class="track-title">Sarah</h3>
                    <div class="track-meta">
                        <span>2011 • Demo</span>
                        <span>3:24</span>
                    </div>
                    <p class="track-description">Unreleased track from the Goblin era, featuring raw production and introspective lyrics about a complicated relationship.</p>
                    <div class="audio-player">
                        <div class="player-controls">
                            <button class="play-btn">
                                <i class="fas fa-play"></i>
                            </button>
                            <div class="progress-container">
                                <div class="progress-bar"></div>
                            </div>
                            <div class="time">0:00 / 3:24</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Track 2 -->
            <div class="track-card">
                <img src="https://images.unsplash.com/photo-1493225457124-a3eb161ffa5f?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Track Cover" class="track-image">
                <div class="track-info">
                    <h3 class="track-title">Heaven To Me</h3>
                    <div class="track-meta">
                        <span>2017 • Unreleased</span>
                        <span>4:12</span>
                    </div>
                    <p class="track-description">Scrapped track from the Flower Boy sessions with soulful production and reflective lyrics about success and happiness.</p>
                    <div class="audio-player">
                        <div class="player-controls">
                            <button class="play-btn">
                                <i class="fas fa-play"></i>
                            </button>
                            <div class="progress-container">
                                <div class="progress-bar"></div>
                            </div>
                            <div class="time">0:00 / 4:12</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Track 3 -->
            <div class="track-card">
                <img src="https://images.unsplash.com/photo-1516280440614-37939bbacd81?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Track Cover" class="track-image">
                <div class="track-info">
                    <h3 class="track-title">OKAGA, CA (Early Version)</h3>
                    <div class="track-meta">
                        <span>2015 • Alternate</span>
                        <span>5:36</span>
                    </div>
                    <p class="track-description">Early version of the Cherry Bomb closing track with different instrumentation and extended outro section.</p>
                    <div class="audio-player">
                        <div class="player-controls">
                            <button class="play-btn">
                                <i class="fas fa-play"></i>
                            </button>
                            <div class="progress-container">
                                <div class="progress-bar"></div>
                            </div>
                            <div class="time">0:00 / 5:36</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Track 4 -->
            <div class="track-card">
                <img src="https://images.unsplash.com/photo-1470225620780-dba8ba36b745?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Track Cover" class="track-image">
                <div class="track-info">
                    <h3 class="track-title">Lemonhead (feat. Frank Ocean)</h3>
                    <div class="track-meta">
                        <span>2019 • Collab</span>
                        <span>2:54</span>
                    </div>
                    <p class="track-description">Unreleased collaboration with Frank Ocean from the IGOR era that didn't make the final album cut.</p>
                    <div class="audio-player">
                        <div class="player-controls">
                            <button class="play-btn">
                                <i class="fas fa-play"></i>
                            </button>
                            <div class="progress-container">
                                <div class="progress-bar"></div>
                            </div>
                            <div class="time">0:00 / 2:54</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Track 5 -->
            <div class="track-card">
                <img src="https://images.unsplash.com/photo-1511379938547-c1f69419868d?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Track Cover" class="track-image">
                <div class="track-info">
                    <h3 class="track-title">Sometimes...</h3>
                    <div class="track-meta">
                        <span>2010 • Early Demo</span>
                        <span>2:18</span>
                    </div>
                    <p class="track-description">One of Tyler's earliest recorded tracks with minimal production and stream-of-consciousness lyrics.</p>
                    <div class="audio-player">
                        <div class="player-controls">
                            <button class="play-btn">
                                <i class="fas fa-play"></i>
                            </button>
                            <div class="progress-container">
                                <div class="progress-bar"></div>
                            </div>
                            <div class="time">0:00 / 2:18</div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Track 6 -->
            <div class="track-card">
                <img src="https://images.unsplash.com/photo-1571974599782-87624638275f?ixlib=rb-4.0.3&auto=format&fit=crop&w=500&q=80" alt="Track Cover" class="track-image">
                <div class="track-info">
                    <h3 class="track-title">Group B</h3>
                    <div class="track-meta">
                        <span>2021 • Unreleased</span>
                        <span>3:42</span>
                    </div>
                    <p class="track-description">Track rumored to be from the CALL ME IF YOU GET LOST sessions with jazz-inspired production.</p>
                    <div class="audio-player">
                        <div class="player-controls">
                            <button class="play-btn">
                                <i class="fas fa-play"></i>
                            </button>
                            <div class="progress-container">
                                <div class="progress-bar"></div>
                            </div>
                            <div class="time">0:00 / 3:42</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <div class="footer-content">
            <p>This is a fan-made project for educational purposes. All music rights belong to Tyler, The Creator and respective copyright holders.</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
            <p class="copyright">© 2023 Tyler, The Creator Unreleased Music Tracker</p>
        </div>
    </footer>

    <script>
        // Audio player functionality
        document.addEventListener('DOMContentLoaded', function() {
            const playButtons = document.querySelectorAll('.play-btn');
            let currentlyPlaying = null;
            
            playButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const playerContainer = this.closest('.track-card');
                    const playIcon = this.querySelector('i');
                    
                    // If this player is already playing, pause it
                    if (playerContainer === currentlyPlaying) {
                        playIcon.classList.remove('fa-pause');
                        playIcon.classList.add('fa-play');
                        currentlyPlaying = null;
                        return;
                    }
                    
                    // Pause any currently playing track
                    if (currentlyPlaying) {
                        const currentPlayIcon = currentlyPlaying.querySelector('.play-btn i');
                        currentPlayIcon.classList.remove('fa-pause');
                        currentPlayIcon.classList.add('fa-play');
                    }
                    
                    // Play this track
                    playIcon.classList.remove('fa-play');
                    playIcon.classList.add('fa-pause');
                    currentlyPlaying = playerContainer;
                    
                    // Simulate audio progress
                    simulateAudioProgress(playerContainer);
                });
            });
            
            function simulateAudioProgress(playerContainer) {
                const progressBar = playerContainer.querySelector('.progress-bar');
                const timeDisplay = playerContainer.querySelector('.time');
                const duration = playerContainer.querySelector('.track-meta span:nth-child(2)').textContent;
                const [min, sec] = duration.split(':').map(Number);
                const totalSeconds = min * 60 + sec;
                
                let currentSeconds = 0;
                progressBar.style.width = '0%';
                timeDisplay.textContent = `0:00 / ${duration}`;
                
                const progressInterval = setInterval(() => {
                    if (playerContainer !== currentlyPlaying) {
                        clearInterval(progressInterval);
                        return;
                    }
                    
                    currentSeconds++;
                    const progressPercent = (currentSeconds / totalSeconds) * 100;
                    progressBar.style.width = `${progressPercent}%`;
                    
                    const currentMin = Math.floor(currentSeconds / 60);
                    const currentSec = currentSeconds % 60;
                    const formattedSec = currentSec < 10 ? `0${currentSec}` : currentSec;
                    
                    timeDisplay.textContent = `${currentMin}:${formattedSec} / ${duration}`;
                    
                    if (currentSeconds >= totalSeconds) {
                        clearInterval(progressInterval);
                        const playIcon = playerContainer.querySelector('.play-btn i');
                        playIcon.classList.remove('fa-pause');
                        playIcon.classList.add('fa-play');
                        progressBar.style.width = '0%';
                        timeDisplay.textContent = `0:00 / ${duration}`;
                        currentlyPlaying = null;
                    }
                }, 1000);
            }
            
            // Filter functionality
            const filterButtons = document.querySelectorAll('.filter-btn');
            
            filterButtons.forEach(button => {
                button.addEventListener('click', function() {
                    // Remove active class from all buttons
                    filterButtons.forEach(btn => btn.classList.remove('active'));
                    // Add active class to clicked button
                    this.classList.add('active');
                    
                    // In a real implementation, this would filter the tracks
                    // For this demo, we'll just show a message
                    const filterText = this.textContent;
                    alert(`Filtering by: ${filterText}. In a real implementation, this would filter the track list.`);
                });
            });
            
            // Progress bar click to seek
            const progressContainers = document.querySelectorAll('.progress-container');
            
            progressContainers.forEach(container => {
                container.addEventListener('click', function(e) {
                    const playerContainer = this.closest('.track-card');
                    if (playerContainer === currentlyPlaying) {
                        const rect = this.getBoundingClientRect();
                        const clickPosition = (e.clientX - rect.left) / rect.width;
                        const progressBar = this.querySelector('.progress-bar');
                        progressBar.style.width = `${clickPosition * 100}%`;
                        
                        // In a real implementation, this would seek the audio
                        console.log(`Seeking to ${Math.round(clickPosition * 100)}%`);
                    }
                });
            });
        });
    </script>
</body>
</html>
