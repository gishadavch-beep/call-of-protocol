# Call of Protocol

**[PHANERO]** protocol and seating web app. It organizes attendance and seating by hierarchy and runs as a free demo on GitHub Pages, with no installs, no backend and no hosting fees.

**Live demo:** https://YOUR-USERNAME.github.io/call-of-protocol/

## Screenshots

| Login | Seating map | Admin settings |
|---|---|---|
| ![Login](screenshots/login.png) | ![Seating map](screenshots/map.png) | ![Admin settings](screenshots/admin.png) |

## Features

- **Hierarchy-based seating:** Clergy, Leaders, VIPs and Members, in that order of priority.
- **Three services:** 1st, 2nd and 3rd service, each with its own capacity and its own seat allocation per level.
- **Adjustable capacity:** 100 to 1,000 seats per service, split across the hierarchy by percentage.
- **Live "seats left" counters** for every level.
- **Organizational seating map:** filled blocks are taken seats, hollow blocks are free. Hover a filled block to see the name.
- **Full-level protection:** registration is blocked when a level is full.
- **Attendance list:** search, export to CSV and print.
- **Logins:** 1 admin and 29 team user accounts (30 in total).

## Roles

| Action | Admin | User |
|---|---|---|
| Log in | Yes | Yes |
| View seats left, seating map and attendance list | Yes | Yes |
| Register attendees | Yes | Yes |
| Change service names, capacity and allocations | Yes | No |
| Remove attendees or clear a service | Yes | No |
| Manage accounts (names and passwords) | Yes | No |

Each registration records which account made it.

## For the protocol team: how to log in

1. Open the live demo link above on your phone or computer.
2. Enter the username and password the admin gave you.
3. Choose the service tab (1st, 2nd or 3rd).
4. To register someone, type their name, choose their hierarchy level and service, then tap **Register**.
5. When you are done, tap **Logout**.

If a level shows no seats left, tell the admin. Only the admin can change allocations.

## Logins

- Admin username: `admin`
- Team usernames: `user01` to `user29`

Default passwords are set in the `defaultAccounts()` function in `index.html`. **Change them before sharing the app.** The admin can edit display names and passwords in the Accounts panel after logging in.

## How to deploy on GitHub Pages

1. Create a public repository named `call-of-protocol`.
2. Add `index.html` and `README.md`.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, and click Save.
5. After a minute or two the app is live at `https://YOUR-USERNAME.github.io/call-of-protocol/`.

## Adding screenshots

1. In the repository, click **Add file → Upload files**.
2. Drag in your images, named `login.png`, `map.png` and `admin.png`, and make sure they go into a folder called `screenshots` (typing `screenshots/` before the file name on a new file creates the folder).
3. Commit. The images then appear in the Screenshots section above.

## Known limitations (demo version)

- **Data is stored per device.** Attendance and password changes are saved in the browser where they were made, so they are not shared between phones or computers.
- **Login is not real security.** There is no server, and the default credentials are visible in the page source. This is suitable for a demo only.

## Roadmap

- Connect a free backend (for example Firebase or Supabase) for shared live data and secure logins.
- Seat numbering and printable seating charts.
- Check-in and attendance reports per service.
- Custom roles and permissions.

## Tech

Plain HTML, CSS and JavaScript in a single file. No frameworks and no build step.
