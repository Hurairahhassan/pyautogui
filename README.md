# pyautogui

import webbrowser
import pyautogui
import time

import webbrowser
import pyautogui
import time

"""
def click_gig(link, x, y):
   
    Opens a Fiverr gig link in a web browser, moves the cursor to the specified coordinates,
    right-clicks on the gig, presses down and enter keys, and waits for 2 seconds.

    Parameters:
    - link (str): The Fiverr gig link to open.
    - x (int): The x-coordinate of the cursor position.
    - y (int): The y-coordinate of the cursor position.
    """
    # Open the link in a web browser
    webbrowser.open(link)

    for _ in range(2):
        # Move the cursor to the specified coordinates
        pyautogui.moveTo(x=x, y=y, duration=1.5)

        # Right-click on the gig
        pyautogui.rightClick(x=x, y=y, duration=1.5)

        # Press the down key
        pyautogui.press("down")

        # Press the enter key
        pyautogui.press("enter")

        # Wait for 2 seconds
        time.sleep(2)

    # Rest of the code after the loop
    """"


# Example usage
links = [list of Fiverr gig links]

# Perform actions on each gig link
# Specify the cursor positions (x, y) for each gig
# Use list comprehension to iterate over the links and perform actions
[click_gig(links[0], x, y) for x, y in [(600, 401), (800, 401)]]
[click_gig(links[1], x, y) for x, y in [(600, 401)]]
[click_gig(links[2], x, y) for x, y in [(600, 401), (800, 401)]]
...
[click_gig(links[n], x, y) for x, y in [(x1, y1), (x2, y2), ...]]

# Move to the close button position
pyautogui.moveTo(x=1253, y=11, duration=2)
# Click on the close button
pyautogui.click(x=1253, y=11, duration=2)
