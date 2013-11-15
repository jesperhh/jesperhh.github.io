---
layout: post
title:  "Simple QObject snippets for Visual Studio (2012)"
date:   2013-11-15 22:15:00
categories: development
---

When using Qt with Visual Studio and CMake, I was unable to preserve the functionality of the Qt Visual Studio add-in (for some reason, it demands that the project was created with the add-in), and therefore had to create QObjects by hand instead of using the nifty wizard thingy. As a rudimentary alternative, I created two snippets for a QObject (one for the header, and one for the implementation).

The snippets generate the following code:

[Header file snippet]({{ site.url }}/files/qobject.snippet)
---
{% highlight c++ %}
#ifndef INCLUDE_GUARD
#define INCLUDE_GUARD

#include <QObject>

class ClassName : public QObject
{
    Q_OBJECT

    public:
        explicit ClassName(QObject *parent = 0);
        ~ClassName();

    signals:

    public slots:
    
};

#endif // INCLUDE_GUARD
{% endhighlight %}

[Implementation file snippet]({{ site.url }}/files/qobjectimpl.snippet)
---
{% highlight c++ %}
#include "ClassName.h"

ClassName::ClassName(QObject *parent) :
    QObject(parent)
{
}

ClassName::~ClassName()
{
}
{% endhighlight %}