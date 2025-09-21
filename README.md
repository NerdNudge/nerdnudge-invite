# Nerd Nudge Invite Page

This is the web page that handles invite links for the Nerd Nudge app.

## Setup Instructions

### 1. Create a GitHub Repository
1. Go to [GitHub](https://github.com) and create a new repository
2. Name it `nerdnudge-invite` (or any name you prefer)
3. Make it public

### 2. Upload the Files
1. Upload the `invite.html` file to the repository
2. Rename it to `index.html` (this is required for GitHub Pages)

### 3. Enable GitHub Pages
1. Go to your repository settings
2. Scroll down to "Pages" section
3. Under "Source", select "Deploy from a branch"
4. Select "main" branch and "/ (root)" folder
5. Click "Save"

### 4. Get Your URL
Your invite page will be available at:
```
https://YOUR_USERNAME.github.io/nerdnudge-invite/
```

### 5. Update the App
Update the `generateInviteLink` method in `DeepLinkHandler`:

```dart
static String generateInviteLink(String userId) {
  return 'https://YOUR_USERNAME.github.io/nerdnudge-invite/?user_id=$userId';
}
```

## How It Works

1. User clicks invite link: `https://YOUR_USERNAME.github.io/nerdnudge-invite/?user_id=John_Doe`
2. Web page loads and tries to open the app: `nerdnudge://invite?user_id=John_Doe`
3. If app opens: User sees invite dialog
4. If app doesn't open: Web page shows download buttons

## Customization

- Update the app store URLs in the JavaScript
- Modify the styling in the CSS
- Change the logo and branding

## Testing

Test the invite link by:
1. Deploying to GitHub Pages
2. Opening the URL in a browser
3. Testing on both iOS and Android devices
