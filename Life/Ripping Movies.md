
[[Passwords and such]]
## 🧩 Jellyfin Media Workflow: Rip, Rename, Sync

### 📀 1. Rip the Movie Using MakeMKV

- Launch MakeMKV and insert the disc
    
- Select the **main title** (usually the longest duration)
    
- Uncheck:
    - Menus
    - Short clips
    - Unwanted audio/subtitle tracks
        
- Set output folder to:
    Code
    ```
    /volume1/JellyfinVault/movies
    ```
- Start the rip
    
**Example output:**

Code
```
/volume1/JellyfinVault/movies/B1_t01.mkv
```

### 🧼 2. Rename the File for Jellyfin Metadata

- SSH into Synology or access via your server’s NFS mount
- Use `mv` to rename the file to match Jellyfin’s naming convention:
    Code
    
    ```
    mv /mnt/jellyfin/movies/B1_t01.mkv "/mnt/jellyfin/movies/Limitless (2011).mkv"
    ```
    
**Naming format:**

Code

```
Movie Title (Year).mkv
```

### 🔄 3. Trigger Jellyfin Library Scan

- Open Jellyfin dashboard
    
- Go to **Libraries → Movies → Scan Library Files**
    
- Confirm the movie appears with correct metadata
### 🧪 Optional: Verify Inside Container

bash

```
docker exec -it jellyfin ls /media/movies
```

You should see:

Code

```
Limitless (2011).mkv
```

### 🧰 Notes

- Use `/mnt/jellyfin/movies` on the server — it’s mounted via NFS from Synology
    
- Keep extras in `/mnt/jellyfin/extras` and mount as `/media/extras` in Jellyfin
    
- For bonus content, name files descriptively:
    
    Code
    
    ```
    Limitless (2011) - Behind the Scenes.mkv
    ```