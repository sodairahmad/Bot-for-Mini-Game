# Bot-for-Mini-Game

#This is the bot which play a game for you

import pyautogui
import time
import keyboard

def click_accept_button():
    while True:  # Infinite loop
        accept_button_location = None

        print('Looking for button:')
        try:
            accept_button_location = pyautogui.locateOnScreen('image1.png', confidence=0.80)
            if accept_button_location is None:
                print("Button not found. Retrying...")
                time.sleep(0.00025)
            else:
                print("Button found. Pressing 'e' key.")
                keyboard.press('e')  # Press 'e' key
                print("Your match is accepted. Continuing...")
                time.sleep(0.002)
                # No return statement here to continue running indefinitely
        except Exception as e:
            print("Error:", e)
            time.sleep(0.00025)

if __name__ == "__main__":
    click_accept_button()
