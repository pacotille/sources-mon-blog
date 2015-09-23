---
title: Intersection Particule Triangle
author: PacoTille
tags: maths
---
# Cas d'un obstacle immobile

Torseur 


> Définition. Le vecteur position du point P(t) du solide (S)
>
>


Dérivation d'un vecteur par rapport au temps



$\{ \mathcal{V} (S/R) \}
= \left\{ \begin{array}{c}
     \overrightarrow{\Omega} (S/R) \\
     \overrightarrow{V} (B \in S/R)
\end{array} \right\} _{B/R}
= \left\{ \begin{array}{c}
     \overrightarrow{\Omega} (S/R) \\
     \overrightarrow{V} (A \in S/R) +\overrightarrow{BA} \wedge \overrightarrow{\Omega}(S/R)
\end{array} \right\} _{B/R}$



# Cas d'un obstacle mobile
sssssssssssssssssssssssssssssss
$\mathbf{P} (\textit{End} V)$
cing d'un nuage de glog

~~~ {.cpp}
class Delegate
{
    typedef void (*Type)(void* callee, int);
public:
    Delegate(void* callee, Type function)
        : fpCallee(callee)
        , fpCallbackFunction(function) {}

    template <class T, void (T::*TMethod)(int)>
    static Delegate from_function(T* callee)
    {
        Delegate d(callee, &methodCaller<T, TMethod>);
        return d;
    }

    void operator()(int x) const
    {
        return (*fpCallbackFunction)(fpCallee, x);
    }

private:

    void* fpCallee;
    Type fpCallbackFunction;

    template <class T, void (T::*TMethod)(int)>
    static void methodCaller(void* callee, int x)
    {
        T* p = static_cast<T*>(callee);
        return (p->*TMethod)(x);
    }
};
~~~
# Cas de l'obstacle mobile

$\sum_{i=1}^9 \frac{9!}{(9-i)!} = 986409$ 
$\{ \mathcal{V} (S/R) \}
= \left\{ \begin{array}{c}
     \overrightarrow{\Omega} (S/R) \\
     \overrightarrow{V} (B \in S/R)
\end{array} \right\} _{B/R}
= \left\{ \begin{array}{c}
     \overrightarrow{\Omega} (S/R) \\
     \overrightarrow{V} (A \in S/R) +\overrightarrow{BA} \wedge \overrightarrow{\Omega}(S/R)
\end{array} \right\} _{B/R}$

# Liens
-[www.geometrictools.com](http://www.geometrictools.com/Documentation/IntersectionMovingSphereTriangle.pdf)
-[www.realtimerendering.com](http://www.realtimerendering.com/intersections.html)
