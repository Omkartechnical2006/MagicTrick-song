# 🎩 Magic Trick Website

> A mind-reading magic trick powered by Firebase Realtime Database

## ✨ What is This?

This is a web-based magic trick that creates the illusion of reading someone's mind. The magician appears to predict the exact song a volunteer is thinking of by using real-time synchronization between two devices.

## 🎪 The Trick

1. **Setup**: Borrow the volunteer's phone and open the performer view
2. **Hide**: Place the phone face-down with volume muted
3. **Ask**: Have the volunteer think of their favorite song
4. **Reveal**: When they say the song name, your accomplice (in the audience) sends the YouTube link
5. **Magic**: The phone automatically redirects to YouTube with the exact song!
6. **Finale**: Unmute the phone and show the "predicted" song playing

## 🚀 Quick Start

### Prerequisites

- A modern web browser
- Firebase account (already configured)
- Two devices (one for performer, one for accomplice)

### Setup Firebase Database Rules

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Open project: **magictrick-c9765**
3. Navigate to **Realtime Database** → **Rules**
4. Set rules to:

```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

5. Click **Publish**

### Running the Website

#### Option 1: Local File Access

**Performer View** (on volunteer's phone):
```
file:///c:/Users/omkar suman/Desktop/MagicTrick/index.html
```

**Accomplice View** (on your accomplice's phone):
```
file:///c:/Users/omkar suman/Desktop/MagicTrick/index.html?view=accomplice
```

#### Option 2: Host Online (Recommended)

Deploy to a hosting service for easier access:

- **[Netlify](https://www.netlify.com/)** - Drag & drop the folder
- **[Vercel](https://vercel.com/)** - Connect to Git repository
- **[Firebase Hosting](https://firebase.google.com/docs/hosting)** - `firebase deploy`

Then access via:
- Performer: `https://your-site.com/`
- Accomplice: `https://your-site.com/?view=accomplice`

## 📁 Project Structure

```
MagicTrick/
├── index.html          # Main application (dual views)
├── style.css           # Premium styling with glassmorphism
└── README.md           # This file
```

## 🛠️ Technology Stack

- **Frontend**: Pure HTML, CSS, JavaScript
- **Database**: Firebase Realtime Database
- **Styling**: Custom CSS with glassmorphism and gradient effects
- **Animations**: CSS keyframe animations

## 🎯 Features

### Performer View
- ✨ Beautiful purple gradient background
- 🎩 Floating magic hat animation
- 💫 Pulsing circle effect
- 🔄 Auto-redirect to YouTube on link receive
- 📱 Responsive design

### Accomplice View
- 🎯 Secret control panel interface
- 📝 YouTube URL input with validation
- 🚀 One-click send button
- ✅ Success/error feedback
- ⚠️ Hidden from audience warnings

### Technical Features
- 🔥 Real-time Firebase synchronization
- ✨ Instant URL propagation
- 🎨 Premium glassmorphism UI
- 📱 Mobile-first responsive design
- ⌨️ Keyboard support (Enter to send)
- 🔍 YouTube URL validation

## 🎬 How to Perform

### Pre-Performance
1. Test the setup with your accomplice
2. Ensure both devices have internet access
3. Have the accomplice view ready on your accomplice's phone

### During Performance
1. Borrow volunteer's phone
2. Open performer view (`index.html`)
3. Place phone face-down, mute volume
4. Ask volunteer to think of a song
5. When they reveal the song:
   - Accomplice quickly searches YouTube
   - Accomplice pastes link in accomplice view
   - Accomplice clicks "Send Link"
6. Pick up phone, unmute, show the magic!

## ⚙️ Configuration

The Firebase configuration is embedded in `index.html`:

```javascript
const firebaseConfig = {
  apiKey: "sdgfgsdfgsdfgsfgsfdgsdf",
  authDomain: "sfgsdfgsdfm",
  databaseURL: "https://magsdictricsgsdfgdfgsdk-c9765-default-rtdb.asia-southeast1.firebasedatabase.app",
  projectId: "magictrfdvfick-c9765",
  storageBucket: "magictsgdsfgrick-c9765.firebasestorage.app",
  messagingSenderId: "521er99363204",
  appId: "1:52199363245243204:adfadfasfweb:2933234d10aa4334ea68d1"
};
```

## 🔒 Security Note

> ⚠️ **Warning**: The current Firebase rules allow public read/write access. This is fine for a magic trick demo, but for production use, consider adding authentication or more restrictive rules.

## 🐛 Troubleshooting

### Link Not Auto-Redirecting
- Check Firebase Database rules are set correctly
- Verify both devices have internet connection
- Check browser console for errors
- Ensure Firebase Database URL is correct

### "Invalid URL" Error
- Make sure the URL is a valid YouTube link
- Accepted formats:
  - `https://youtube.com/watch?v=...`
  - `https://www.youtube.com/watch?v=...`
  - `https://youtu.be/...`

### Slow Synchronization
- Check internet speed on both devices
- Firebase should sync within 1-2 seconds typically
- Consider using WiFi instead of cellular data

## 💡 Tips for Best Performance

1. **Practice**: Rehearse with your accomplice multiple times
2. **Timing**: Perfect the misdirection while waiting for sync
3. **Connection**: Use strong WiFi for both devices
4. **Backup**: Have a backup song ready in case of technical issues
5. **Presentation**: Your showmanship sells the trick!

## 📝 License

This is a personal magic trick project. Feel free to use and modify for your own performances!

## 🙏 Credits

Built with Firebase Realtime Database for seamless real-time synchronization.

---

**Ready to blow some minds?** 🎩✨

For questions or issues, check the Firebase Console or browser developer tools for debugging.
