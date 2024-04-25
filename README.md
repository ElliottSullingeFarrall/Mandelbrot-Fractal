# Mandelbrot Fractal

The [Mandelbrot Fractal](https://en.wikipedia.org/wiki/Mandelbrot_set) is a famous fractal in mathematics. We can write a simple program to produce this fractal

## The Map

Let $c \in \mathbb{Z}$ be arbitrary. We consider the function $f_c : \mathbb{Z} \to \mathbb{Z}$ given by
$$f_c(z) = z^2 + c$$
We use this map to construct a sequence of points $z_n \in \mathbb{C}$ via
$$z_{n+1} = f_c(z_n) \qquad\qquad z_0 = 0$$
We define the Mandelbrot Fractal to be the set of points $c \in \mathbb{C}$ such that this sequence does not diverge.

## The Code

Start by creating a function `func` that takes an argument $c$ and returns the function $z \mapsto z^2 + c$.

Next, create a function `is_bounded` that takes an argument $c$ and uses `func(c)` to iterate the point $z = 0$. Test to see if these iterations are diverging and return the appropriate boolean.

Finally, run `is_bounded` on a large number of points $c \in \mathbb{Z}$ and use `imshow` form `matplotlib` to display the results.
