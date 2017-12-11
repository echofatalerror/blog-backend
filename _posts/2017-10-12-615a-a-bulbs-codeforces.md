---
layout: post
current: post
cover:  assets/images/advanced.jpg
navigation: True
title: 615A - A. Bulbs [Codeforces]
date: 2017-10-12 07:00:00
tags: maratones c++
class: post-template
subclass: 'post'
author: krthr
categories: krthr
---

## Problema
Vasya wants to turn on Christmas lights consisting of m bulbs. Initially, all bulbs are turned off. There are n buttons, each of them is connected to some set of bulbs. Vasya can press any of these buttons. When the button is pressed, it turns on all the bulbs it’s connected to. Can Vasya light up all the bulbs?

If Vasya presses the button such that some bulbs connected to it are already turned on, they do not change their state, i.e. remain turned on.

### Input
The first line of the input contains integers n and m (1 ≤ n, m ≤ 100) — the number of buttons and the number of bulbs respectively.

Each of the next n lines contains xi (0 ≤ xi ≤ m) — the number of bulbs that are turned on by the i-th button, and then xi numbers yij (1 ≤ yij ≤ m) — the numbers of these bulbs.

### Output
If it’s possible to turn on all m bulbs print “YES”, otherwise print “NO”.

### Examples

<pre><code>
# input
3 4
2 1 4
3 1 3 1
1 2

# output
YES

---

# input
3 3
1 1
1 2
1 1

# output
NO
</code></pre>

## Solución

<pre><code class="c++">
/**
    Codeforces | 615A
    A. Bulbs
    @author krthr
*/

#include <bits/stdc++.h>
using namespace std;

int main() {
    int n, m, x, j;
    cin >> n >> m;
    bool b[m];

    for (int i = 0; i < m; i++) b[i] = false;

    for (int i = 0; i < n; i++) {
        cin >> x;
        while (x--) {
            cin >> j;
            b[j - 1] = true;
        }
    }

    for (bool t : b) {
        if (!t) {
            cout << "NO" << endl; return 0;
        }
    }

    cout << "YES" << endl;

    return 0;
}
</code></pre>


