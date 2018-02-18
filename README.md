from OpenGL.GL import *
from OpenGL.GLU import *
from OpenGL.GLUT import *
import numpy as np
from math import *


def draw():
    glClearColor(1, 1, 1, 1)   # clear background
    glClear(GL_COLOR_BUFFER_BIT)

    glBegin(GL_POLYGON)  # white border circle
    glColor(0, 0, 0)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.03 * cos(theta)
        y = 0.03 * sin(theta) + 0.8
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # white circle
    glColor(1, 1, 1)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.02 * cos(theta)
        y = 0.02 * sin(theta)+0.8
        glVertex2d(x, y)
    glEnd()
    glFlush()

    # Black line
    glBegin(GL_LINES)
    glColor(0, 0, 0)
    glVertex2d(0, 0.78)
    glVertex2d(0, 0.65)
    glEnd()
    glFlush()

    # Black lines
    glBegin(GL_LINES)
    glColor(0, 0, 0)
    glVertex2d(0, 0.74)
    glVertex2d(0.09, 0.78)
    glEnd()
    glFlush()

    # Black lines
    glBegin(GL_LINES)
    glColor(0, 0, 0)
    glVertex2d(0, 0.74)
    glVertex2d(-.09, 0.78)
    glEnd()
    glFlush()

    # Black lines
    glBegin(GL_LINES)
    glColor(0, 0, 0)
    glVertex2d(0, 0.72)
    glVertex2d(0.09, 0.76)
    glEnd()
    glFlush()

    # Black lines
    glBegin(GL_LINES)
    glColor(0, 0, 0)
    glVertex2d(0, 0.72)
    glVertex2d(-0.09, 0.76)
    glEnd()
    glFlush()

    # Black lines
    glBegin(GL_LINES)
    glColor(0, 0, 0)
    glVertex2d(0, 0.70)
    glVertex2d(0.09, 0.74)
    glEnd()
    glFlush()

    # Black lines
    glBegin(GL_LINES)
    glColor(0, 0, 0)
    glVertex2d(0, 0.70)
    glVertex2d(-0.09, 0.74)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # face
    glColor(0.75, 0.75, 0.75)
    glVertex2d(0.30, 0.64)
    glVertex2d(-0.30, 0.64)
    glVertex2d(-0.30, 0.36)
    glVertex2d(0.30, 0.36)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # right eye border
    glColor(0, 0, 0)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.019 * cos(theta) + 0.20
        y = 0.019 * sin(theta) + 0.53
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # left eye border
    glColor(0, 0, 0)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.019 * cos(theta) - 0.20
        y = 0.019 * sin(theta) + 0.53
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # right eye
    glColor(0, 0, 0)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.018 * cos(theta) + 0.20
        y = 0.018 * sin(theta) + 0.53
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # left eye
    glColor(0, 0, 0)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.018 * cos(theta) - 0.20
        y = 0.018 * sin(theta) + 0.53
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # right cheek border
    glColor(0.87, 0.45, 0.45)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.021 * cos(theta) + 0.20
        y = 0.021 * sin(theta) + 0.45
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # left cheek border
    glColor(0.87, 0.45, 0.45)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.021 * cos(theta) - 0.20
        y = 0.021 * sin(theta) + 0.45
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # right cheek
    glColor(0.87, 0.45, 0.45)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.02 * cos(theta) + 0.20
        y = 0.02 * sin(theta) + 0.45
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # left cheek
    glColor(0.87, 0.45, 0.45)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.02 * cos(theta) - 0.20
        y = 0.02 * sin(theta) + 0.45
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # right arm borders
    glColor(0.78, 0.78, 0.78)
    glVertex2d(0.26, 0.36)
    glVertex2d(0.36, 0.16)
    glVertex2d(0.26, -0.04)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # right arm
    glColor(1, 1, 1)
    glVertex2d(0.21, 0.31)
    glVertex2d(0.30, 0.16)
    glVertex2d(0.21, -0.01)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # left arm borders
    glColor(0.78, 0.78, 0.78)
    glVertex2d(-0.26, 0.36)
    glVertex2d(-0.36, 0.16)
    glVertex2d(-0.26, -0.04)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # left arm
    glColor(1, 1, 1)
    glVertex2d(-0.21, 0.31)
    glVertex2d(-0.30, 0.16)
    glVertex2d(-0.21, -0.01)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # right legs borders
    glColor(0, 0, 0)
    glVertex2d(0.176, -0.36)
    glVertex2d(0.076, -0.36)
    glVertex2d(0.076, -0.56)
    glVertex2d(0.176, -0.56)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # left legs borders
    glColor(0, 0, 0)
    glVertex2d(-0.076, -0.36)
    glVertex2d(-0.176, -0.36)
    glVertex2d(-0.176, -0.56)
    glVertex2d(-0.076, -0.56)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # right legs
    glColor(0.78, 0.78, 0.78)
    glVertex2d(0.175, -0.35)
    glVertex2d(0.075, -0.35)
    glVertex2d(0.075, -0.55)
    glVertex2d(0.175, -0.55)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # legs
    glColor(0.78, 0.78, 0.78)
    glVertex2d(-0.075, -0.35)
    glVertex2d(-0.175, -0.35)
    glVertex2d(-0.175, -0.55)
    glVertex2d(-0.075, -0.55)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # body borders
    glColor(0.9, 0.9, 0.9)
    glVertex2d(0.26, .36)
    glVertex2d(-0.26, .36)
    glVertex2d(-0.26, -.36)
    glVertex2d(0.26, -.36)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # body
    glColor(0.78, 0.78, 0.78)
    glVertex2d(0.25, 0.35)
    glVertex2d(-0.25, 0.35)
    glVertex2d(-0.25, -0.35)
    glVertex2d(0.25, -0.35)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # small body  borders
    glColor(8, 4, 7)
    glVertex2d(0.11, 0.16)
    glVertex2d(-0.11, 0.16)
    glVertex2d(-0.11, -0.16)
    glVertex2d(0.11, -0.16)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # small body
    glColor(0.78, 0.78, 0.78)
    glVertex2d(0.10, 0.15)
    glVertex2d(-0.10, 0.15)
    glVertex2d(-0.10, -0.15)
    glVertex2d(0.10, -0.15)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # yellow circle
    glColor(1, 1, 0)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.02 * cos(theta)
        y = 0.02 * sin(theta)
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # Red circle
    glColor(1, 0, 0)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.02 * cos(theta) + .04
        y = 0.02 * sin(theta) + .04
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # Red circle
    glColor(1, 0, 0)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.02 * cos(theta) - .04
        y = 0.02 * sin(theta) - .04
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # Red circle
    glColor(1, 0, 0)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.02 * cos(theta) + .04
        y = 0.02 * sin(theta) - .04
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # Red circle
    glColor(1, 0, 0)
    for theta in np.arange(0, 2 * pi, 0.01):
        x = 0.02 * cos(theta) - .04
        y = 0.02 * sin(theta) + .04
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # foot borders
    glColor(0, 0, 0)
    for angle in np.arange(0, 2 * pi, 0.01):
        x = 0.061 * cos(angle) + 0.125
        y = 0.061 * sin(angle) - 0.56
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # foot borders
    glColor(0, 0, 0)
    for angle in np.arange(0, 2 * pi, 0.01):
        x = 0.061 * sin(angle) - 0.125
        y = 0.061 * cos(angle) - 0.56
        glVertex2d(x, y)
    glEnd()
    glFlush()

    # foot
    glBegin(GL_POLYGON)
    glColor(0, 0, 0)
    for angle in np.arange(0, 2 * pi, 0.01):
        x = 0.06 * cos(angle) + 0.125
        y = 0.06 * sin(angle) - 0.56
        glVertex2d(x, y)
    glEnd()
    glFlush()

    # foot
    glBegin(GL_POLYGON)
    glColor(0, 0, 0)
    for angle in np.arange(0, 2 * pi, 0.01):
        x = 0.06 * cos(angle) - 0.125
        y = 0.06 * sin(angle) - 0.56
        glVertex2d(x, y)
    glEnd()
    glFlush()

    glBegin(GL_POLYGON)  # foot cutting
    glColor(1, 1, 1)
    glVertex2d(0.186, -0.56)
    glVertex2d(0.186, -0.66)
    glVertex2d(-0.186, -0.56)
    glVertex2d(-0.186, -0.66)
    glEnd()
    glFlush()


glutInit()
glutInitDisplayMode(GLUT_SINGLE | GLUT_RGB)
glutInitWindowSize(500, 500)
glutCreateWindow(b"first")
glutDisplayFunc(draw)
glutMainLoop()
