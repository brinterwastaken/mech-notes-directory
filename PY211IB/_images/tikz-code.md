# spring-block.svg

```latex
\usepackage{tikz}
\usetikzlibrary{decorations.pathmorphing}

\begin{document}

\begin{tikzpicture}[scale=1.5]
  % Ground line with hatching
  \draw[line width=1.5pt] (-0.5,0) -- (4,0);
  \foreach \i in {0,0.2,0.4,0.6,...,3.8} {
    \draw (\i,-0.15) -- (\i-0.12,0);
  }

  % Rigid support/wall (hatched rectangle)
  \draw[line width=1.5pt] (0.2,0) -- (0.2,1.5);
  \foreach \i in {0.15,0.40,0.65,0.90,1.15} {
    \draw (0,\i) -- (0.2,\i+0.2);
  }

  % Spring (coil decoration)
  \draw[decorate,decoration={coil,aspect=0.6,segment length=0.28cm,amplitude=0.28cm},line width=1pt] (0.2,0.5) -- (2.3,0.5);

  % Block (rectangle)
  \draw[line width=1.5pt] (2.3,0) rectangle (3.3,1);

  % Label for spring constant
  \node at (1.3,1) {$k$};

  % Label for mass
  \node at (2.8,0.5) {$m$};

\end{tikzpicture}

\end{document}
```

# spring-parallel.svg

```latex
\usepackage{tikz}
\usetikzlibrary{decorations.pathmorphing}

\begin{document}

\begin{tikzpicture}[scale=1.5]
  % Ground line with hatching
  \draw[line width=1.5pt] (-0.5,0) -- (4,0);
  \foreach \i in {0,0.2,0.4,0.6,...,3.8} {
    \draw (\i,-0.15) -- (\i-0.12,0);
  }
  
  % Rigid support/wall (hatched rectangle)
  \draw[line width=1.5pt] (0.2,0) -- (0.2,1.5);
  \foreach \i in {0.15,0.40,0.65,0.90,1.15} {
    \draw (0,\i) -- (0.2,\i+0.2);
  }
  
  % First spring (upper, coil decoration)
  \draw[decorate,decoration={coil,aspect=0.6,segment length=0.28cm,amplitude=0.2cm},line width=1pt] (0.2,0.9) -- (2.3,0.9);
  
  % Second spring (lower, coil decoration)
  \draw[decorate,decoration={coil,aspect=0.6,segment length=0.28cm,amplitude=0.2cm},line width=1pt] (0.2,0.3) -- (2.3,0.3);
  
  % Block (rectangle)
  \draw[line width=1.5pt] (2.3,0) rectangle (3.4,1.1);
  
  % Label for first spring
  \node at (1.2,1.2) {$k_1$};
  
  % Label for second spring
  \node at (1.2,0.6) {$k_2$};
  
  % Label for mass
  \node at (2.85,0.55) {$m$};
  
\end{tikzpicture}

\end{document}
```

# spring-series.svg

```latex
\usepackage{tikz}
\usetikzlibrary{decorations.pathmorphing}

\begin{document}

\begin{tikzpicture}[scale=1.5]
  % Ground line with hatching
  \draw[line width=1.5pt] (-0.5,0) -- (4.5,0);
  \foreach \i in {0,0.2,0.4,0.6,...,4.3} {
    \draw (\i,-0.15) -- (\i-0.12,0);
  }
  
  % Rigid support/wall (hatched rectangle)
  \draw[line width=1.5pt] (0.2,0) -- (0.2,1.5);
  \foreach \i in {0.15,0.40,0.65,0.90,1.15} {
    \draw (0,\i) -- (0.2,\i+0.2);
  }
  
  % First spring (coil decoration)
  \draw[decorate,decoration={coil,aspect=0.6,segment length=0.25cm,amplitude=0.25cm},line width=1pt] (0.2,0.5) -- (1.4,0.5);
  
  % Second spring (coil decoration)
  \draw[decorate,decoration={coil,aspect=0.6,segment length=0.25cm,amplitude=0.25cm},line width=1pt] (1.6,0.5) -- (2.8,0.5);
  
  % Vertical line between springs
  \draw[line width=1pt] (1.4,0.5) -- (1.6,0.5);
  
  % Block (rectangle)
  \draw[line width=1.5pt] (2.8,0) rectangle (3.8,1);
  
  % Label for first spring
  \node at (0.85,1) {$k_1$};
  
  % Label for second spring
  \node at (2.15,1) {$k_2$};
  
  % Label for mass
  \node at (3.3,0.5) {$m$};
  
\end{tikzpicture}

\end{document}
```

# torsional-pendulum.svg

```latex
\usepackage{tikz}
\usetikzlibrary{arrows.meta}

\begin{document}

\begin{tikzpicture}[scale=1.5]
  
  % Isometric 3D rigid support block
  % Front face
  \draw[line width=1.5pt] (0,3) -- (1,3);
  
  % Hatching on front face
  \foreach \i in {0,0.2,0.4,0.6,0.8} {
    \draw (\i,3) -- (\i+0.2,3.2);
  }
  
  % Suspension wire (from center of top)
  \draw[line width=1pt] (0.5,3) -- (0.5,1.5);
  
  % Disc (ellipse in isometric view)
  \draw[line width=1.5pt] (0.5,1.5) ellipse (0.45 and 0.25);
  
  % Center line of disc (for reference)
  \draw[line width=0.5pt, dashed] (0.5,1.5) -- (0.95,1.5);

  \draw[line width=0.5pt] (0.5,1.5) -- (0.85,1.65);

  
  % Curved arrow indicating twist (arc)
  \draw[-{Stealth[length=5pt]}, line width=1.2pt] (1.1, 1.5) arc (0:45:0.5 and 0.3);
  
  % Theta label
  \node at (1.2,1.7) {$\theta$};
  
\end{tikzpicture}

\end{document}
```

# damping-types.svg

```latex
\usepackage{tikz}
\usetikzlibrary{decorations.pathmorphing}

\begin{document}

\begin{tikzpicture}[scale=2]
  
  % Axes
  \draw[-] (-0.3,0) -- (5,0);
  \draw[-] (0,-1.2) -- (0,1.5);
  
  % Axis labels
  \node at (-0.15,1.5) {$A$};
  \node at (5,-0.15) {$t$};
  \node at (-0.15,-0.15) {$0$};
  
  % Overdamping (very dotted line) - slow exponential decay
  \draw[line width=1.2pt, dotted, densely dotted] plot[smooth, domain=0:5, samples=100] (\x, {exp(-0.7*\x)});
  
  % Critical damping (long dashes) - fastest non-oscillatory decay
  \draw[line width=1.2pt, dashed, dash pattern=on 8pt off 4pt] plot[smooth, domain=0:5, samples=100] (\x, {(1+\x)*exp(-2.4*\x)});
  
  % Underdamping (solid line) - oscillatory decay with sine wave
  \draw[line width=1.2pt, solid] plot[smooth, domain=0:5, samples=200] (\x, {exp(-0.8*\x)*sin(5*\x r)});
  
  % Legend
  \draw[line width=1.2pt, dotted, densely dotted] (3.0,1.35) -- (3.4,1.35);
  \node[right] at (3.4,1.35) {$1$ - Overdamping};
  
  \draw[line width=1.2pt, dashed, dash pattern=on 8pt off 4pt] (3.0,1.15) -- (3.4,1.15);
  \node[right] at (3.4,1.15) {$2$ - Critical damping};
  
  \draw[line width=1.2pt, solid] (3.0,0.95) -- (3.4,0.95);
  \node[right] at (3.4,0.95) {$3$ - Underdamping};
  
\end{tikzpicture}

\end{document}
```
