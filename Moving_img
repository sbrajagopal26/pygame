import pygame

pygame.init()

display_width = 800
display_height = 600

black = (0,0,0)
white = (255,255,255)
red = (255,0,0)


gameDisplay = pygame.display.set_mode((display_width,display_height)) # dispaly size

pygame.display.set_caption('A bit Racey') # text

clock = pygame.time.Clock() # it refers to game time

carImg = pygame.image.load('crr.png')

def car(x,y):
    gameDisplay.blit(carImg,(x,y))

x = (display_width * 0.45)
y = (display_height * 0.6)

x_change = 0
#Game loop

crashed = False

while not crashed:

    for event in pygame.event.get():#gets event from the library
        if event.type == pygame.QUIT:
            crashed = True

        if event.type == pygame.KEYDOWN:
            if event.key == pygame.K_LEFT:
                x_change = -5
            if event.key == pygame.K_RIGHT:
                x_change = 5

        if event.type == pygame.KEYUP:
            if event.key == pygame.K_LEFT or event.key == pygame.K_RIGHT:
                x_change = 0

    x += x_change
            

        #print(event)
    gameDisplay.fill(white)
    car(x,y)
    pygame.display.update()#updates the window or can also use flip
    clock.tick(60)#frames per second

pygame.quit()
quit()
        
        
