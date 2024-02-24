import pygame
import sys

def play_music(music_file):
    pygame.init()
    pygame.mixer.music.load(music_file)
    pygame.mixer.music.play()

def pause_music():
    pygame.mixer.music.pause()

def resume_music():
    pygame.mixer.music.unpause()

def stop_music():
    pygame.mixer.music.stop()

def main():
    music_file = "path/to/your/audio/file.mp3"  # Replace with the path to your audio file

    while True:
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                pygame.quit()
                sys.exit()

            if event.type == pygame.KEYDOWN:
                if event.key == pygame.K_SPACE:
                    if pygame.mixer.music.get_busy():
                        pause_music()
                    else:
                        play_music(music_file)

                if event.key == pygame.K_p:
                    pause_music()

                if event.key == pygame.K_r:
                    resume_music()

                if event.key == pygame.K_s:
                    stop_music()

if __name__ == "__main__":
    main()
