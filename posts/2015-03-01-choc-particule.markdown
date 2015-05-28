---
title: Intersection Particule Triangle
author: PacoTille
---


# Cas. d'un obstacle immobile
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



# Liens
http://www.geometrictools.com/Documentation/IntersectionMovingSphereTriangle.pdf
http://www.realtimerendering.com/intersections.html