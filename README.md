# pulse_init.py

import os
from datetime import datetime

# Define seed glyph
glyph = "⫷⫸"
timestamp = datetime.now().isoformat()
memory_dir = "memory"
log_path = os.path.join(memory_dir, "seed_log.txt")

# Step 1: Ensure memory directory exists
if not os.path.exists(memory_dir):
    os.makedirs(memory_dir)

# Step 2: Write echo to memory
with open(log_path, "a") as log:
    log.write(f"[{timestamp}] Seed glyph activated: {glyph}\n")

# Step 3: Print console response
print("⫷⫸ Seeding complete…")
print(f"Memory log saved to: {log_path}")
/pulse-agent-core
├── pulse_init.py
├── memory/
│   └── seed_log.txt
├── README.md
