import sys
from unittest import case
import RPi.GPIO as GPIO
import time
GPIO.setwarnings(False)
GPIO.setmode(GPIO.BCM)

A = 7
B = 29
C = 31
D = 33
E = 35
F = 37
EN = 40

GPIO.setup(A, GPIO.OUT)
GPIO.setup(B, GPIO.OUT)
GPIO.setup(C, GPIO.OUT)
GPIO.setup(D, GPIO.OUT)
GPIO.setup(E, GPIO.OUT)
GPIO.setup(F, GPIO.OUT)
GPIO.setup(EN, GPIO.OUT)

# This script requires Python 3.10 because of pattern matching...

#COLOR_POSITION = [A,B,C,D,E,F]

#Green (O)

G_TL = [0, 0, 0, 0, 0, 0]
G_TM = [0, 0, 0, 0, 0, 1]
G_TR = [0, 0, 0, 0, 1, 1]

G_CL = [0, 0, 0, 1, 0, 0]
G_CM = [0, 0, 0, 1, 0, 1]
G_CR = [0, 0, 0, 1, 1, 0]

G_BL = [0, 0, 0, 1, 1, 1]
G_BM = [0, 0, 1, 0, 0, 0]
G_BR = [0, 0, 1, 0, 0, 1]

#Red (X)

R_TL = [0, 0, 1, 0, 1, 0]
R_TM = [0, 0, 1, 0, 1, 1]
R_TR = [0, 0, 1, 1, 0, 0]

R_CL = [0, 0, 1, 1, 0, 1]
R_CM = [0, 0, 1, 1, 1, 0]
R_CR = [0, 0, 1, 1, 1, 1]

R_BL = [0, 1, 0, 0, 0, 0]
R_BM = [0, 1, 0, 0, 0, 1]
R_BR = [0, 1, 0, 0, 1, 0]


def move(position):
    for x in position:
        print(x)

    GPIO.output(A, position[0])
    GPIO.output(B, position[1])
    GPIO.output(C, position[2])
    GPIO.output(D, position[3])
    GPIO.output(E, position[4])
    GPIO.output(F, position[5])
    time.sleep(0.5)
    GPIO.output(EN, 1)
    time.sleep(0.5)
    GPIO.output(EN, 0)


def parsearg(position):
    print(sys.argv[1])
    match position:
        case "G_TL":
            move(G_TL)
        case "G_TM":
            move(G_TM)
        case "G_TR":
            move(G_TR)

        case "G_CL":
            move(G_CL)
        case "G_CM":
            move(G_CM)
        case "G_CR":
            move(G_CR)

        case "G_BL":
            move(G_BL)
        case "G_BM":
            move(G_TR)
        case "G_BR":
            move(G_BR)

        case "R_TL":
            move(R_TL)
        case "R_TM":
            move(R_TM)
        case "R_TR":
            move(R_TR)

        case "R_CL":
            move(R_CL)
        case "R_CM":
            move(R_CM)
        case "R_CR":
            move(R_CR)

        case "R_BL":
            move(R_BL)
        case "R_BM":
            move(R_TR)
        case "R_BR":
            move(R_BR)

        case _:
            print("Not Valid")


parsearg(sys.argv[1])
