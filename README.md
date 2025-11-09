# ZReference
A comprehensive Discord bot cog that allows you to **save, organize, and retrieve** important Discord messages in a searchable library system.
> 💡 **Built for the Zygnal Ecosystem — to download and use this extension, you must be part of the Zygnal Ecosystem.**  
> This extension (cog) is part of the **Zygnal Ecosystem** and is only available through its supported platforms.  
> You can use it with:  
> - The **[Discord Bot Framework](https://github.com/TheHolyOneZ/discord-bot-framework)** — ideal for developers who want full control and flexibility *(includes an integrated extension marketplace)*, or  
> - The **[ZygnalBot](https://zygnalbot.de)** — a prebuilt, plug-and-play Discord bot *(also includes an integrated extension marketplace)*.  
>
> Browse and install extensions at [zygnalbot.com/extension](https://zygnalbot.com/extension).  
> For help or community discussions, join us on Discord: [discord.gg/sgZnXca5ts](https://discord.gg/sgZnXca5ts)
# 🧭 ZReference - Discord Message Reference Library

A comprehensive Discord bot cog that allows you to **save, organize, and retrieve** important Discord messages in a searchable library system.

---

## 📘 Overview

ZReference transforms your Discord server into an organized **knowledge base** by allowing users to bookmark important messages with metadata, making it easy to find and reference them later.  

Perfect for keeping track of **rules**, **tutorials**, **announcements**, **bug reports**, or any valuable information shared in your server.

---

## ✨ Features

### 📚 Reference Library System
- **Save Discord Messages:** Bookmark any message with a direct link  
- **Rich Metadata:** Add titles, detailed notes, categories, and tags  
- **Message Previews:** Automatically captures message content  
- **Smart Organization:** Filter, search, and sort references  
- **View Statistics:** Track views, search activity, and popular tags  

### 🔍 Advanced Search & Filtering
- **Text Search:** Across titles, notes, tags, and message content  
- **Tag Filtering:** Filter references by specific tags  
- **Sorting Options:**
  - Most Recent
  - Oldest First
  - Alphabetical
  - Most Popular
- **Two View Modes:**
  - Detailed View
  - Compact View

### ⭐ Personal Features
- **Favorites System:** Mark favorites for quick access  
- **Personal Bookmarks:** Each user has their own favorites  
- **View History:** Tracks number of views per reference  

### 🎨 Customization
- **Custom Embed Colors**
- **Flexible Layout:** Items per page (1–10)  
- **Auto-Delete Messages:** Embeds auto-clean after 15 minutes  
- **Channel Control:** Restrict or allow specific channels  

### 🔒 Permission System
Three-tiered, role-based structure:
- **Add Permissions:** Control who can add new references  
- **Delete Permissions:** Control who can remove references  
- **Library Access:** Control who can view the library  
- **Self-Management:** Users can always edit/delete their own entries  
- **Admin Override:** Admins and owners have full access  

### 📊 Statistics & Logging
- **Usage Statistics:** Track views, searches, and references  
- **Tag Analytics:** View most popular tags  
- **Activity Logging:** Monitors all add/edit/delete actions  
- **Dedicated Log Channel:** Optional log for activities  
- **Recent Activity Feed:** Displays latest changes  

### 💾 Data Management
- **Auto-Backup System:** Keeps last 5 backups automatically  
- **Manual Backup:** Create backups on demand  
- **Export Data:** Download complete library as JSON  
- **Restore Backups:** Revert from previous saves  
- **Data Persistence:** Per-server JSON storage  

---

## ⚙️ Commands

### `/zreference`
Opens the **interactive reference library browser**.

**Features:**
- Paginated, interactive embeds  
- Navigation, search, and filter controls  
- Message previews and metadata  
- Tracks view counts automatically  

**Access:**  
- Users with “Can Use Library” role (if set)  
- Everyone (if public)  
- Admins always  

**In-Library Actions:**
- **Navigation:** ⏮️ ⬅️ ➡️ ⏭️  
- **Quick Actions:** Copy URL, Open Message, Toggle Favorite, View Stats  
- **Tag Filter & Sort:** By tag, order, popularity  
- **View Mode:** Switch between Detailed/Compact  
- **Search:** Keyword search  

---

### `/zrefadd`
Interactive form to **add new references**.

**Access:**  
- “Can Add” role or Administrator  

**Required:**  
- **Message URL** (must be from same server)  

**Optional:**  
- **Title/Summary** (≤ 200 chars)  
- **Notes** (≤ 1000 chars)  
- **Category** (≤ 50 chars)  
- **Tags** (comma-separated, ≤ 200 chars)  

**Steps:**  
1. Run `/zrefadd`  
2. Fill in details using modal forms  
3. Submit to instantly add the reference  

---

### `/zrefremove`
Manage and delete existing references.

**Access:**  
- Users can manage their own references  
- “Can Delete” role and Administrators can manage all  

**Actions:**  
- Browse through entries  
- Edit title, notes, tags, etc.  
- Delete with confirmation  

---

### `/zrefadmin`
Admin control panel (Admins/Owners only).

#### 🔐 Permissions Page
- Configure role-based access for:
  - Add References
  - Delete References
  - Use Library  

#### 📡 Channels Page
- Control bot usage by channel  
  - **Allowed Channels:** Whitelist mode  
  - **Excluded Channels:** Blacklist mode  
  - **Logging Channel:** For library actions  

#### ⚙️ Settings Page
- Customize appearance and behavior:
  - Embed Color (hex)
  - Items Per Page (1–10)
  - Auto-Backup toggle  

#### 📊 Statistics Page
- View analytics:
  - Total References
  - Total Views & Searches
  - Top Tags
  - Recent Activity  

#### 💾 Data Management
- Export all data (JSON)
- Restore from backup  

---

## 🧭 Interactive Elements

### 🧭 Navigation Buttons
| Button | Function |
|:------:|:----------|
| ⏮️ | First page |
| ◀️ | Previous page |
| ▶️ | Next page |
| ⏭️ | Last page |

### ⚡ Quick Actions
- 📋 **Copy Message URL**  
- 🔗 **Open Message**  
- ⭐ **Toggle Favorite**  
- 📊 **View Statistics**  

### 🧩 Filter & Sort Controls
- 🏷️ Tag Filter  
- 📊 Sort By  
- 👁️ View Mode  
- 🔍 Search  

### 📝 Add Reference Form Buttons
- 🔗 Set Message URL  
- 📝 Set Title  
- 📄 Set Notes  
- 📁 Set Category  
- 🏷️ Set Tags  
- ✅ Submit Reference  
- ❌ Cancel  

### ⚙️ Management Buttons
- ✏️ Edit  
- 🗑️ Delete (with confirmation)  

---

## 🚀 Setup Guide

### Installation
1. Place `ZReference.py` in your `cogs` directory  
2. Load the cog in your bot  
3. The bot auto-creates `/data/ZReference` directory  
4. Each server gets its own file:  
   `zreference_{guild_id}.json`

### Initial Configuration
1. Run `/zrefadmin` (Admin only)  
2. Set **permissions**  
3. (Optional) Configure **channel restrictions**  
4. Customize **embed color**, **pagination**, etc.  

---

## 🧰 Permission Setup Examples

| Mode | Can Use | Can Add | Can Delete |
|------|----------|----------|------------|
| **Public Library, Restricted Adding** | Public | Specific roles | Mods |
| **Fully Restricted Library** | Member roles | Trusted | Mods |
| **Open Contribution System** | Public | Everyone | Mods |

---

## 💡 Best Practices
- Start with one **category** for structure  
- Use consistent **tagging conventions** (e.g. `bug-report`, `feature-request`)  
- Enable **logging & auto-backups**  
- Review **usage statistics** regularly  

---

## 🧠 How It Works

### 🗂️ Data Storage
- Stored per-server in `data/ZReference/`  
- Auto-backups before each save (last 5 kept)  

### 🧾 Reference Structure
Each entry includes:
- **Message Info:** IDs, URLs, preview  
- **Metadata:** Title, notes, category, tags  
- **Tracking:** Added by, timestamp, view count  
- **Features:** Favorites, pinned, last edited  

### 🛡️ Permission Logic
- Users can always manage their own references  
- Admins & Owners bypass all restrictions  

### 🛰️ Channel Restrictions
- **Whitelist Mode:** Only allowed channels  
- **Blacklist Mode:** All except excluded  
- **Open Mode:** Default (everywhere)  

### 🧹 Auto-Cleanup
- All ephemeral messages auto-delete after 15 minutes  
- Trigger messages deleted immediately  

### 🧾 Activity Logging
If enabled:
- Logs who did what  
- Action type (Add/Edit/Delete)  
- Reference info + timestamps  
- Linked message URL  

### 📈 Statistics
Tracks:
- View counts  
- Searches  
- Popular tags  
- Recent 100 actions  

---

## 🧩 Use Cases

### 📋 Server Rules & Guidelines
Organize all rule messages for easy lookup.

### 🐛 Bug Reports
Track reported bugs, add notes, and tag statuses.

### 🎓 Tutorials & Guides
Save tutorials and FAQs for community members.

### 💡 Feature Requests
Store suggestions and sort by popularity.

### 📢 Important Announcements
Reference key announcements and context.

### 🎨 Community Creations
Showcase member art or projects.

### 📖 FAQ Builder
Save common questions and answers.

---

## 🧭 Tips & Tricks

### 🏷️ Effective Tagging
- Use lowercase
- Hyphens for multi-word tags
- Limit to 3–5 tags per entry

### 🔍 Search Strategies
- Searches all text fields
- Combine search + filters for precision
- Clear filters to reset results

### 🗃️ Organization Methods
- **By Department:** Admin, Mod, Community  
- **By Type:** Tutorial, Rule, Bug  
- **By Status:** Active, Resolved, Archived  
- **By Priority:** High, Medium, Low  

### 🧹 Maintenance
- Review stats periodically  
- Delete outdated entries  
- Export backups regularly  

---

## ⚙️ Technical Details

| Property | Value |
|-----------|--------|
| **Data Location** | `data/ZReference/` |
| **Format** | JSON |
| **Backups** | Last 5 kept |
| **Encoding** | UTF-8 |
| **Title Limit** | 200 chars |
| **Notes Limit** | 1000 chars |
| **Category Limit** | 50 chars |
| **Tags Limit** | 200 chars |
| **Activity Log** | Last 100 entries |

### 🧾 Message URL Format
https://discord.com/channels/{guild_id}/{channel_id}/{message_id}

- Must be from same server  
- Validated automatically  
- Prevents duplicates  

### 🎨 Embed Behavior
- Customizable color  
- Timestamp included  
- Auto-delete after 15 minutes  
- Ephemeral (visible only to user)  

---

## 🧩 Troubleshooting

| Issue | Possible Fix |
|-------|---------------|
| ❌ "Cannot be used in this channel" | Check allowed/excluded channels |
| 🔒 "You don't have permission" | Verify role permissions |
| ⚠️ "Invalid message URL" | Must be from same server & correct format |
| 🔁 "This message is already in the library" | Message already referenced |
| 💾 "Backups not creating" | Check auto-backup toggle and bot write access |

---

## 🔐 Privacy & Security

### Data Stored
- Message IDs & URLs  
- User IDs  
- Titles, notes, tags, categories  
- View counts, activity logs, favorites  

### Access Control
- Only within same server  
- Admins can export  
- Users see permitted entries only  
- Logs show who did what  

### Retention
- Persistent until deleted  
- 5 recent backups kept  
- Export available anytime  

---

## 🧑‍💻 Credits

**Created by:** TheHolyOneZ *(TheZ)*  
**Product:** ZReference  
**Platform:** Zygnalbot Extension  
**Version:** 1.0  
**Website:** https://zygnalbot.com/extension/
**License:** Inside the .py file at the very top
---

