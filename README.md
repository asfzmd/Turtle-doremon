# Turtle-doremon
import turtle as t

def draw_circle(color, x, y, radius):
    t.penup()
    t.fillcolor(color)
    t.goto(x, y)
    t.pendown()
    t.begin_fill()
    t.circle(radius)
    t.end_fill()

def draw_doraemon():
    t.bgcolor("#f7f7f7")
    t.speed(2)
    t.pensize(2)

    # Draw face
    draw_circle("#00a0de", 0, -20, 100)

    # Draw left eye
    draw_circle("white", -35, 35, 20)
    draw_circle("#3e7aef", -35, 35, 15)
    draw_circle("black", -25, 45, 5)

    # Draw right eye
    draw_circle("white", 35, 35, 20)
    draw_circle("#3e7aef", 35, 35, 15)
    draw_circle("black", 45, 45, 5)

    # Draw nose
    draw_circle("#e70013", 0, 10, 12)

    # Draw mouth
    t.penup()
    t.goto(-30, -20)
    t.pendown()
    t.right(60)
    t.circle(30, 120)

    # Draw whiskers
    def draw_whisker(x, y):
        t.penup()
        t.goto(x, y)
        t.pendown()
        t.forward(30)
        t.backward(60)
        t.forward(30)

    t.left(80)
    draw_whisker(-30, 20)
    t.right(160)
    draw_whisker(-30, 20)
    t.left(80)
    draw_whisker(-30, 0)
    t.right(160)
    draw_whisker(-30, 0)
    t.left(80)
    draw_whisker(-30, -20)
    t.right(160)
    draw_whisker(-30, -20)

    # Hide the turtle and display the result
    t.hideturtle()
    t.done()

if __name__ == "__main__":
    draw_doraemon()
