# A simple class based PyGame template
```python3
#!/usr/bin/python3
# By Joseph Pitts

import sys 
import random
import pygame
from pygame.locals import *


class Colours:
    BLACK = (0, 0, 0)
    WHITE = (255, 255, 255)
    AQUA = (0, 255, 255)
    GREY = (128, 128, 128)
    NAVY = (0, 0, 128)
    SILVER = (192, 192 ,192)
    GREEN = (0, 128, 0)
    OLIVE = (128, 128, 0)
    TEAL = (0, 128, 128)
    BLUE = (0, 0, 255)
    LIME = (0, 255, 0)
    PURPLE = (128, 0, 128)
    FUCHSIA = (255, 0, 255)
    MAROON = (128, 0, 0)
    RED = (255, 0, 0)
    YELLOW = (255, 255, 0)

    @staticmethod
    def RANDOM():
        return (random.randrange(0, 255), random.randrange(0, 255), random.randrange(0, 255))

        

class PyGame(object):
    def __init__(self, width = 640, height = 480): 
        pygame.init()
        
        self.fps = 60
        self.fpsClock = pygame.time.Clock()
        
        self.width, self.height = width, height
        self.screen = pygame.display.set_mode((self.width, self.height))

    def game_loop(self):
        self.screen.fill(Colours.BLACK)
        for event in pygame.event.get():
            if event.type == QUIT:
                pygame.quit()
                sys.exit()

        pygame.display.flip()
        fpsClock.tick(fps)

    def run(self):
        while True:
            self.game_loop()
```
