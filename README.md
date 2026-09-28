# smart-fuse-monitor
# Smart Fuse Monitoring System

MAX_CURRENT = 10
MAX_TEMPERATURE = 70

print("==============================")
print("       SMART FUSE MONITOR")
print("==============================")

current = float(input("Enter fuse current (A): "))
temperature = float(input("Enter fuse temperature (°C): "))

print("\nCurrent:", current, "A")
print("Temperature:", temperature, "°C")

fault = False

# Current monitoring
if current > MAX_CURRENT:
    print("\n⚠️ OVERCURRENT DETECTED")
    fault = True

# Temperature monitoring
if temperature > MAX_TEMPERATURE:
    print("⚠️ FUSE OVERHEATING DETECTED")
    fault = True

# Fuse status
if fault:
    print("\n🔴 FUSE ALERT")
    print("⚡ Fuse protection activated")
    print("🔌 Load should be disconnected")
else:
    print("\n🟢 FUSE STATUS: NORMAL")
    print("✅ Fuse is operating safely")
