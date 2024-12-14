import pygame
pygame.init()

WIDTH,HEIGHT = 400,600
BLUE = 0,0,255

screen = pygame.display.set_mode((WIDTH,HEIGHT))
pygame.display.set_caption('BOAT DODGER 3D (SHORT GAME)')

icon = pygame.image.load('icon.png')
pygame.display.set_icon(icon)

playerImg = pygame.image.load('boat.png')
playerX = 200
playerY = 500
playerX_change = 0
playerY_change = 0

enemyImg = pygame.image.load('enemy.png')
enemyX = 100
enemyY = 100

signImg = pygame.image.load('sign.png')
signX = 300
signY = 430

sign2Img = pygame.image.load('sign.png')
sign2X = 220
sign2Y = 130

sign3Img = pygame.image.load('sign.png')
sign3X = 120
sign3Y = 30

def player(x,y):
    screen.blit(playerImg, (x,y))

def sign(x,y):
    screen.blit(signImg, (x,y))

def sign2(x,y):
    screen.blit(sign2Img, (x,y))

def sign3(x,y):
    screen.blit(sign3Img, (x,y))

def enemy(x,y):
    screen.blit(enemyImg, (x,y))

running = True

while running:
    screen.fill((BLUE))
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
        if event.type == pygame.KEYDOWN:
            if event.key == pygame.K_a:
                playerX_change = -3
            if event.key == pygame.K_d:
                playerX_change = 3
            if event.key == pygame.K_w:
                playerY_change = -3
            if event.key == pygame.K_s:
                playerY_change = 3
        if event.type == pygame.KEYUP:
            if event.key == pygame.K_a or event.key == pygame.K_d:
                playerY_change = 0
            if event.key == pygame.K_w or event.key == pygame.K_s:
                playerY_change = 0

        player(playerX,playerY)
        sign2(sign2X,sign2Y)
        sign3(sign3X,sign3Y)
        enemyY += 0.9
        enemy(enemyX,enemyY)
        sign(signX,signY)
        playerX += playerX_change
        playerY += playerY_change
        pygame.display.update()
