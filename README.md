# Brick Breaker

A modern take on the classic Arkanoid/Breakout arcade game built with pure JavaScript and HTML5 Canvas. Break all the bricks to win while avoiding letting the ball fall off the screen!

**Created by:** Michael Semera

## 🎮 Game Features

- **Classic Gameplay**: Control a paddle to bounce a ball and break colorful bricks
- **Physics Engine**: Realistic ball physics with velocity, collision detection, and angle-based bouncing
- **Progressive Difficulty**: Multiple brick rows with different point values
- **Power-ups**: Special abilities including multi-ball, wider paddle, and slower ball speed
- **Score System**: Track your high score across game sessions
- **Lives System**: Three lives to complete each level
- **Level Progression**: Beat one level to advance to the next with increased difficulty
- **Visual Effects**: Particle explosions, smooth animations, and gradient effects
- **Responsive Design**: Adapts to different screen sizes
- **Sound Ready**: Architecture prepared for sound effect integration

## 🛠️ Technology Stack

- **HTML5 Canvas**: For game rendering and graphics
- **Vanilla JavaScript**: Pure JavaScript with no external dependencies
- **CSS3**: Modern styling and responsive layout
- **LocalStorage API**: For persisting high scores

## 📁 Project Structure

```
brick-breaker/
├── index.html          # Main HTML file with canvas element
├── game.js             # Core game logic and engine
├── styles.css          # Styling and layout
└── README.md           # Project documentation
```

## 🎯 Game Mechanics

### Controls
- **Mouse Movement**: Move paddle left and right
- **Touch**: Mobile touch support for paddle control
- **Spacebar**: Launch ball / Pause game
- **R Key**: Restart game after game over

### Scoring System
- **Red Bricks**: 10 points
- **Orange Bricks**: 8 points
- **Yellow Bricks**: 6 points
- **Green Bricks**: 4 points
- **Blue Bricks**: 2 points

### Power-ups
- **Multi-ball**: Spawns additional balls for more brick-breaking action
- **Wide Paddle**: Increases paddle width temporarily
- **Slow Motion**: Reduces ball speed for easier control

### Collision Detection
The game implements pixel-perfect collision detection:
- **Ball-Paddle Collision**: Angle-based bouncing depending on hit position
- **Ball-Brick Collision**: Detects which side of the brick was hit for realistic physics
- **Ball-Wall Collision**: Bounces off side walls and top wall
- **Ball-Bottom Collision**: Loses a life when ball falls off screen

## 🚀 Installation & Setup

### Option 1: Run Locally

1. Clone or download the project files
2. Open `index.html` in a modern web browser
3. No build process or dependencies required!

### Option 2: Deploy to Web Server

1. Upload all files to your web hosting service
2. Access via your domain URL
3. Works on any static hosting platform (GitHub Pages, Netlify, Vercel, etc.)

## 💻 Code Architecture

### Main Components

#### Game Class
The core game engine managing all game state and logic:
```javascript
class Game {
  constructor(canvas)
  init()              // Initialize game state
  update()            // Update game logic (60 FPS)
  render()            // Render all game elements
  handleCollisions()  // Detect and handle all collisions
  createBricks()      // Generate brick layouts
  spawnPowerUp()      // Randomly spawn power-ups
}
```

#### GameObject Classes
- **Paddle**: Player-controlled paddle with smooth movement
- **Ball**: Physics-based ball with velocity and collision
- **Brick**: Individual brick with health and color
- **PowerUp**: Collectible items with various effects
- **Particle**: Visual effects for brick destruction

### Key Algorithms

#### Collision Detection
```javascript
// Ball-brick collision with side detection
checkBrickCollision(ball, brick) {
  // Calculate overlap from all four sides
  // Determine which side had the least overlap
  // Adjust ball velocity accordingly
}
```

#### Physics System
```javascript
// Ball velocity with angle-based paddle bouncing
updateBallPhysics() {
  // Apply velocity to position
  // Handle wall bounces
  // Calculate paddle hit angle
  // Apply spin and speed modifications
}
```

## 🎨 Design Highlights

- **Color Palette**: Vibrant gradient backgrounds with neon brick colors
- **Smooth Animations**: 60 FPS game loop with requestAnimationFrame
- **Particle Effects**: Explosion particles when bricks are destroyed
- **UI Elements**: Clean HUD showing score, lives, and level
- **Visual Feedback**: Paddle glow effects and ball trails

## 📊 Game States

1. **Start Screen**: Initial state with instructions
2. **Playing**: Active gameplay
3. **Paused**: Temporary pause state
4. **Level Complete**: Transition between levels
5. **Game Over**: End state with score display

## 🔧 Customization

### Adjusting Difficulty
Modify constants at the top of `game.js`:
```javascript
const BALL_SPEED = 5;           // Ball velocity
const PADDLE_SPEED = 8;         // Paddle movement speed
const BRICK_ROWS = 5;           // Number of brick rows
const BRICK_COLS = 10;          // Number of brick columns
```

### Adding New Power-ups
Extend the `POWER_UP_TYPES` object:
```javascript
POWER_UP_TYPES: {
  NEW_POWER: {
    color: '#color',
    effect: (game) => { /* your effect */ }
  }
}
```

## 📈 Performance Optimization

- Efficient collision detection using bounding boxes
- Particle pooling for reduced garbage collection
- Canvas layer optimization
- Throttled mouse/touch event handlers
- Minimal DOM manipulation

## 🐛 Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 🎓 Learning Outcomes

This project demonstrates proficiency in:

1. **Game Development**: Complete game loop architecture
2. **Canvas API**: Advanced 2D graphics rendering
3. **Physics Programming**: Velocity, acceleration, collision detection
4. **Object-Oriented Design**: Clean class structure and inheritance
5. **Event Handling**: Mouse, keyboard, and touch input
6. **Algorithm Design**: Efficient collision detection algorithms
7. **State Management**: Complex game state transitions
8. **Performance Optimization**: 60 FPS rendering techniques

## 🚀 Future Enhancements

- [ ] Sound effects and background music
- [ ] Multiple level layouts with unique patterns
- [ ] Boss levels with special challenge bricks
- [ ] Leaderboard with online high scores
- [ ] Additional power-up types
- [ ] Brick types with special properties (exploding, moving, etc.)
- [ ] Achievement system
- [ ] Mobile app conversion with Cordova/Capacitor

## 📝 Version History

**v1.0.0** - Initial Release
- Core gameplay mechanics
- 5 levels of progressive difficulty
- Power-up system
- Score tracking and lives
- Particle effects
- Responsive design

## 📄 License

This project is created for portfolio purposes by Michael Semera. Feel free to use as a reference for learning game development concepts.

## 🙏 Acknowledgments

- Inspired by the classic Atari Breakout and Taito Arkanoid
- Built to demonstrate modern JavaScript game development techniques
- Created as a portfolio piece showcasing clean code and game design principles

## 👤 Author

**Michael Semera**

- 💼 LinkedIn: [Michael Semera](https://www.linkedin.com/in/michael-semera-586737295/)
- 🐙 GitHub: [@MichaelKS123](https://github.com/MichaelKS123)
- 📧 Email: michaelsemera15@gmail.com

This project showcases:
- JavaScript game development expertise
- Canvas API proficiency
- Physics simulation implementation
- Clean, maintainable code architecture
- User experience design
- Performance optimization techniques

---

**Play Now**: Open `index.html` in your browser and start breaking bricks!