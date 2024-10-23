# Simple-Alarm-Clock
import time
import datetime
import winsound  # Only works on Windows

def set_alarm(alarm_time):
    while True:
        current_time = datetime.datetime.now().strftime("%H:%M:%S")
        if current_time == alarm_time:
            print("Time to wake up!")
            for i in range(5):  # Beep 5 times
                winsound.Beep(1000, 1000)  # Frequency 1000 Hz, Duration 1000 ms (1 second)
            break
        time.sleep(1)

def main():
    alarm_time = input("Enter the time for the alarm in HH:MM:SS format: ")
    print(f"Alarm is set for {alarm_time}")
    set_alarm(alarm_time)

if __name__ == "__main__":
    main()
