import pygame

# Initialize Pygame
pygame.init()

# Set up the display
screen = pygame.display.set_mode((640, 480))

# Load images
rabbit_image = pygame.image.load("rabbit.png")
carrot_image = pygame.image.load("carrot.png")
sparrow_image = pygame.image.load("sparrow.png")
vulture_image = pygame.image.load("vulture.png")

# Set up the clock
clock = pygame.time.Clock()

# Set up the game state
game_state = "intro"

# Game loop
while True:
    # Handle events
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            quit()

    # Draw the screen
    screen.fill((255, 255, 255))

    if game_state == "intro":
        # Draw the rabbit and the text
        screen.blit(rabbit_image, (100, 100))
        font = pygame.font.Font(None, 36)
        text = font.render("Hello, I am Hurex. Let me tell you my story.", True, (0, 0, 0))
        screen.blit(text, (200, 100))

        # Check for mouse click
        if pygame.mouse.get_pressed()[0]:
            game_state = "carrots"

    elif game_state == "carrots":
        # Draw the rabbit and the carrots
        screen.blit(rabbit_image, (100, 100))
        screen.blit(carrot_image, (300, 200))
        screen.blit(carrot_image, (400, 250))

        # Check for mouse click
        if pygame.mouse.get_pressed()[0]:
            game_state = "sparrow"

    elif game_state == "sparrow":
        # Draw the rabbit, the sparrow, and the text
        screen.blit(rabbit_image, (100, 100))
        screen.blit(sparrow_image, (300, 200))
        font = pygame.font.Font(None, 36)
        text = font.render("Hello, friend Hurex!", True, (0, 0, 0))
        screen.blit(text, (200, 100))

        # Check for mouse click
        if pygame.mouse.get_pressed()[0]:
            game_state = "vulture"

    elif game_state == "vulture":
        # Draw the rabbit, the vulture, and the text
        screen.blit(rabbit_image, (100, 100))
        screen.blit(vulture_image, (300, 200))
        font = pygame.font.Font(None, 36)
        text = font.render("Oh no! The vulture took my friend!", True, (0, 0, 0))
        screen.blit(text, (200, 100))

        # Check for mouse click
        if pygame.mouse.get_pressed()[0]:
            game_state = "equations"

    elif game_state == "equations":
        # Draw the rabbit and the text
        screen.blit(rabbit_image, (100, 100))
        font = pygame.font.Font(None, 36)
        text = font.render("We need to solve equations to defeat the king of Brickmat Land!", True, (0, 0, 0))
        screen.blit(text, (200, 100))

        # Check for mouse click
        if pygame.mouse.get_pressed()[0]:
            game_state = "intro"

    # Update the screen
    pygame.display.update()

    # Set the frame rate
    clock.tick(60
<!---
aahanakhan/aahanakhan is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
