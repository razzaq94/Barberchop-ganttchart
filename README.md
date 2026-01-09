# Barberchop Gantt Chart

A dynamic, interactive Gantt chart application for managing project tasks with automatic timeline shifting and conflict resolution. Perfect for tracking Backend and Mobile development tasks with visual timeline representation.

![GitHub Pages](https://img.shields.io/badge/GitHub-Pages-brightgreen)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## 🚀 Features

- **Interactive Gantt Chart**: Visual timeline representation with week-based view
- **Automatic Task Shifting**: When adding new tasks, overlapping tasks are automatically shifted to prevent conflicts
- **Team-Based Organization**: Separate task management for Backend and Mobile teams
- **Smart Conflict Resolution**: Automatically resolves overlaps within each team's timeline
- **Task Management**: Add, view, and delete tasks with ease
- **Real-time Statistics**: Track total tasks, project end date, and team-specific task counts
- **Automatic Local Storage**: All changes are automatically saved to your browser
- **☁️ Cloud Sync**: Sync data across all devices using GitHub API
- **Export/Import**: Backup and restore your data as JSON files
- **Responsive Design**: Modern, gradient-based UI with smooth animations
- **No Dependencies**: Pure HTML, CSS, and JavaScript - no frameworks required

## 📋 How to Use

### Adding a Task

1. Fill in the task details:
   - **Task Name**: Enter a descriptive name for your task
   - **Owner**: Select either "Backend" or "Mobile"
   - **Start Date**: Choose when the task should begin
   - **Duration**: Enter the number of days the task will take

2. Click **"Add Task"** to add it to the timeline

3. The system will automatically:
   - Shift any overlapping tasks of the same team
   - Update the timeline to show the new task
   - Recalculate all task positions to prevent conflicts

### Viewing Tasks

- Tasks are displayed in a Gantt chart format with weeks as the time unit
- Each task is color-coded by team:
  - **Purple gradient**: Backend tasks
  - **Pink gradient**: Mobile tasks
- Hover over tasks to see detailed information (dates and duration)

### Deleting Tasks

- Click the **×** button on any task bar to remove it
- The timeline will automatically recalculate after deletion

### Cloud Sync (GitHub)

Access your data from anywhere with automatic cloud synchronization:

1. **Setup Cloud Sync**:
   - Create a GitHub Personal Access Token at [github.com/settings/tokens](https://github.com/settings/tokens)
   - Select **repo** scope when creating the token
   - Enter your token, repository owner, and repository name in the Cloud Sync section
   - Click **Test Connection** to verify

2. **Automatic Sync**:
   - Once configured, all changes automatically sync to GitHub
   - Data is saved to `data.json` in your repository
   - Access your data from any device by loading from cloud

3. **Manual Sync**:
   - **Sync Now**: Manually push your current data to GitHub
   - **Load from Cloud**: Pull the latest data from GitHub
   - Useful when working on multiple devices

**Note**: Your GitHub token is stored locally in your browser and never sent to any third-party servers.

## 🛠️ Technology Stack

- **HTML5**: Structure and semantic markup
- **CSS3**: Styling with modern gradients and animations
- **Vanilla JavaScript**: No frameworks or dependencies

## 📦 Installation & Setup

### Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/razzaq94/Barberchop-ganttchart.git
   cd Barberchop-ganttchart
   ```

2. Open `index.html` in your web browser:
   ```bash
   # On Windows
   start index.html

   # On macOS
   open index.html

   # On Linux
   xdg-open index.html
   ```

That's it! No build process or dependencies required.

### Using a Local Server (Recommended)

For better development experience, use a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (with http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000` in your browser.

## 🌐 Deployment

### GitHub Pages

This project can be easily deployed to GitHub Pages with just a few clicks!

1. **Enable GitHub Pages**:
   - Go to your repository on GitHub: `https://github.com/razzaq94/Barberchop-ganttchart`
   - Click on **Settings** → **Pages** (in the left sidebar)
   - Under **Source**, select **Deploy from a branch**
   - Select branch: **main** (or **master** if that's your default branch)
   - Select folder: **/ (root)**
   - Click **Save**

2. **That's it!** Your site will be live in a few seconds at:
   - `https://razzaq94.github.io/Barberchop-ganttchart`

3. **Automatic Updates**:
   - Every time you push changes to the `main` branch, GitHub Pages will automatically update
   - Changes typically appear within 1-2 minutes

**Note**: The GitHub Actions workflow (`.github/workflows/deploy.yml`) is optional and can be used if you prefer deploying to a separate `gh-pages` branch. For simple static sites, deploying directly from the main branch is the easiest approach.

## 📁 Project Structure

```
Barberchop-ganttchart/
│
├── index.html              # Main application file (HTML, CSS, and JavaScript)
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Actions deployment workflow
└── README.md               # Project documentation
```

## 🎯 Key Functionality

### Automatic Timeline Shifting

When a new task is added:
- The system identifies tasks of the same team that would overlap
- Affected tasks are automatically shifted forward by the new task's duration
- The timeline recalculates to ensure no conflicts

### Conflict Resolution

The application uses a smart algorithm to:
- Separate tasks by team (Backend/Mobile)
- Sort tasks chronologically within each team
- Resolve overlaps by shifting tasks forward
- Maintain task durations while preventing conflicts

### Week-Based Display

- Tasks are displayed in weekly increments for better visualization
- Week labels show date ranges (e.g., "Jan 5-11")
- Task bars span across multiple weeks when needed

## 📊 Statistics Dashboard

The application provides real-time statistics:
- **Total Tasks**: Count of all tasks in the project
- **Project End Date**: The latest end date among all tasks
- **Backend Tasks**: Number of tasks assigned to the Backend team
- **Mobile Tasks**: Number of tasks assigned to the Mobile team

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📝 License

This project is open source and available for use and modification.

## 👨‍💻 Author

Created for the Barberchop project task management.

---

**Live Demo**: [View on GitHub Pages](https://razzaq94.github.io/Barberchop-ganttchart)
