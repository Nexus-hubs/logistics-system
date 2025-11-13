# 3D Micro-Fulfillment Center

An interactive 3D visualization of a high-efficiency micro-fulfillment center rendered entirely in the browser. Experience a complete logistics system with autonomous robots, conveyor belts, package tracking, and spatial audio.

## Features

### 🏭 Warehouse Architecture
- Multi-level facility with ground floor and elevated mezzanine platform
- Industrial lighting with work zone spotlights
- Structural beams, railings, and glass panels
- Realistic floor grid and ceiling cable trays

### 🤖 Robotic Systems

**Inbound Scanning Tunnel**
- Transparent casing with visible sensor units
- Barcode scanning with sound effects
- Package identification and highlighting

**Conveyor Network**
- Multi-level conveyor system at different heights
- Merge and diverge points with mechanical diverters
- Smooth package flow with realistic physics

**Six-Axis Sorting Arms**
- Three robotic arms at the central sorting hub
- Smooth interpolated motions with visible joints
- Pick and place operations with sound feedback
- Idle calibration movements

**Autonomous Mobile Robots (AMRs)**
- Six mobile robots carrying totes
- Underglow lighting indicating direction
- Coordinated path planning to avoid collisions
- Utilization tracking and status display

**Vertical Lifts**
- Multi-level package transport
- Open frame design with moving platforms
- Mechanical sounds synchronized with movement

### 📦 Package Lifecycle

Each package follows a complete journey:
1. **Arrival** - Enters on inbound conveyor
2. **Scanning** - Passes through detection tunnel
3. **Identification** - System assigns route and priority
4. **Sorting** - Robotic arm picks and places to correct lane
5. **Transport** - Moves via conveyors and lifts
6. **Outbound** - Groups at dispatch zones
7. **Loading** - Virtual truck departure

### 🎮 Interactive Controls

**Camera System**
- Smooth orbit, pan, and zoom controls
- Mouse/touch drag to rotate view
- Right-click/two-finger drag to pan
- Scroll/pinch to zoom
- Preset viewpoints: Overview, Inbound, Sorter Hub, Mobile Robots, Outbound

**Control Panel**
- Start/Pause system operations
- Follow individual packages through the system
- Adjust traffic load (Light/Normal/Peak)
- Control sound volume
- Toggle diagnostics overlays
- Toggle info labels

**Real-Time Statistics**
- Packages per minute throughput
- Active package count
- Robot utilization percentage
- System status indicator

**Interactive Tooltips**
- Hover over packages to see ID, destination, priority, and status
- Hover over robots to see utilization and speed
- Real-time information updates

### 🔊 Spatial Audio

**Layered Soundscape**
- Base industrial ambience (HVAC, distant machinery)
- Localized conveyor rolling sounds
- Robotic arm motor whines and clicks
- Mobile robot movement hums
- Scanning beeps and confirmation tones
- Alert sounds for exceptions

**3D Audio Positioning**
- Sound intensity varies with camera distance
- Stereo positioning based on source location
- Dynamic mixing based on system state

### 📱 Mobile & Desktop Support

**Responsive Design**
- Optimized layouts for all screen sizes
- Touch controls for mobile devices
- Pinch-to-zoom gesture support
- Adaptive UI panel positioning
- Performance optimization for mobile GPUs

### 🎨 Visual Feedback

**Color Coding**
- Standard priority: Neutral brown tones
- Express priority: Cyan glow effect
- Bottlenecks/jams: Amber pulsing
- Active work zones: Blue-tinted lighting

**Dynamic Effects**
- Package highlighting during scanning
- Robot underglow animation
- Smooth camera transitions
- Particle effects for status changes

## Usage

### Getting Started

1. Open `micro-fulfillment-center.html` in any modern web browser
2. The system will load and initialize automatically
3. Click anywhere or press Start to begin operations (enables audio)

### Controls

**Mouse/Trackpad:**
- Left-click + drag: Rotate camera
- Right-click + drag: Pan camera
- Scroll wheel: Zoom in/out

**Touch (Mobile/Tablet):**
- One finger drag: Rotate camera
- Two finger drag: Pan camera
- Pinch: Zoom in/out

**Buttons:**
- **View Buttons** (right side): Jump to preset camera angles
- **Pause/Start**: Stop or resume all operations
- **Follow Package**: Track a package through its complete journey
- **Toggle Diagnostics**: Show/hide system visualization overlays
- **Toggle Labels**: Show/hide information tooltips

### Traffic Scenarios

Adjust the traffic load slider to see how the system scales:

- **Light**: Sparse package flow, calm ambience
- **Normal**: Regular operations with steady throughput
- **Peak**: High density, aggressive but coordinated robot movement

## Technical Details

### Technologies
- **Three.js r128**: 3D rendering engine
- **Web Audio API**: Spatial sound synthesis
- **Vanilla JavaScript**: No framework dependencies
- **CSS3**: Responsive UI styling

### Performance
- Optimized for 60 FPS on modern devices
- Shadow mapping with soft PCF shadows
- Level-of-detail considerations for mobile
- Efficient particle system
- Garbage collection friendly object pooling

### Browser Compatibility
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile Safari (iOS 14+)
- Chrome Mobile (Android 8+)

## System Architecture

### Package Flow Logic
```
Inbound → Scanner → Hub Lift → Sorting Hub → Robotic Arm →
Outbound Conveyor → Dock Lift → Dispatch Lane → Virtual Truck
```

### Robot Coordination
- Grid-based navigation
- Priority-based right-of-way
- Real-time collision avoidance
- Dynamic task assignment

### State Management
- Event-driven package lifecycle
- Centralized system state
- Real-time statistics tracking
- Persistent audio context

## Customization

The system can be extended with:
- Additional robot types
- Custom package priorities
- New warehouse layouts
- Different conveyor configurations
- Enhanced diagnostics overlays
- Performance analytics
- Integration with real logistics data

## Offline Capability

This visualization works completely offline after the initial load:
- Three.js loaded from CDN (cached by browser)
- All sounds generated synthetically in browser
- No external API calls
- No server dependencies

## File Structure

```
logistics-system/
├── micro-fulfillment-center.html   # Main application (self-contained)
└── README.md                        # This file
```

## License

This project is provided as-is for demonstration and educational purposes.

## Credits

Created as a demonstration of real-time 3D logistics visualization using modern web technologies.
