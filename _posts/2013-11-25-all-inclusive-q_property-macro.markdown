---
layout: post
title:  "All-inclusive Q_PROPERTY macro"
date:   2013-11-25 21:55:00
categories: development
---

When declaring properties in Qt, the Q_PROPERTY macro is used to define the property. However, this is only to make the Qt Meta-Object System aware of the property, you still have to manually define at least a getter, and optionally a setter, a member variable and a signal to notify when changed (and possible a reset function). To avoid this, I combined all this functionality in one macro ([Gist][]) (except the reset function, feel free to add this yourself).

{% highlight c++ %}
#define Q_PROPERTY_FULL(member, _type) \
  Q_PROPERTY(_type member READ member WRITE set##member NOTIFY member##Changed) \
  public: \
    void set##member##(_type _arg_##member) { if (m_##member != _arg_##member) {m_##member = _arg_##member; Q_EMIT member##Changed();  } } \
    _type member##() const { return m_##member; } \
  Q_SIGNALS: \
    void member##Changed(void); \
  private: \
    _type m_##member;
{% endhighlight %}

One thing to note is the use of `Q_SIGNALS` AND `Q_EMIT` instead of `signals` and `emit`, as I had some issues getting the MOC compiler to accept the macro when using the keywords.

[Gist]: https://gist.github.com/jesperhh/7648254