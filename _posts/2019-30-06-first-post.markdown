---
layout: post
title: The Grand Opening of the War Room
date: 2019-06-30 01:24:00
description: First post -- should feature everything we could need to remember
---

## Code
Here's some python code

We can write code pretty easily here. 

{% raw  %}
{% highlight c++ %}  <br/> code code code <br/> {% endhighlight %}
{% endraw %}

Produces something like this:

{% highlight python %}
def minimizer_func(params, samples):
    """ Params is the normal concatenation of h and Jij """
	loglikelihood = 0
	N = len(samples[0])
	dloglikelihood = np.zeros_like(params)

	for r in range(N):
		obs = calc_obs_r(r, samples)
		jr_vector, jr_ind = calc_jij_r(r, params, N)
		E = -obs.dot(jr_vector)
		loglikelihood += -np.log(1 + np.exp(2 * E)).sum()
		dloglikelihood[jr_ind] += ( -(1/(1+np.exp(2*E)) * np.exp(2*E))[:,None] * 2*obs ).sum(0)
		return(-loglikelihood, dloglikelihood)

{% endhighlight %}

Here are some quotes:

<blockquote>
    We do not grow absolutely, chronologically. We grow sometimes in one dimension, and not in another, unevenly. We grow partially. We are relative. We are mature in one realm, childish in another.
    —Anais Nin
</blockquote>

Here's a list of things:
#### list
<ul>
    <li>Make code region nicer (I'm thinking solarized, with rounded corners)</li>
    <li>Actually write up Jij</li>
    <li>get at least two more fast projects done so this thing doesn't look empty</li>
    <li>IPO</li>
</ul>

All the normal Markdown stuff should carry over.

Finally, here's some math and links.

$$
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
$$

Note that [KaTeX](https://khan.github.io/KaTeX/) is work in progress, so it does not support the full range of math expressions as, say, [MathJax](https://www.mathjax.org/). Yet, it is [blazing fast](http://www.intmath.com/cg5/katex-mathjax-comparison.php).
