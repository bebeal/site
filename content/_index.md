---
title: Home
type: docs
---


# Home

-----------

## About Me

My name is Benjamin Beal, but I normally go by Noah (my middle name). I'm currently ...

An undergraduate Computer Science student at [The University of Texas](https://www.cs.utexas.edu/) at Austin.

A Teaching Assistant for [CS 314: Data Structures](https://www.cs.utexas.edu/~scottm/cs314/index.htm), taught by the legendary [Mike Scott](https://www.cs.utexas.edu/~scottm/)

The Curriculum Director for [CS Roadshow](http://www.cs.utexas.edu/roadshow/index.html)

Researching the problem of Drug Design using [Neural ODE's](https://arxiv.org/pdf/1806.07366.pdf), [Deep Reinforcement Learning](https://deepmind.com/blog/article/deep-reinforcement-learning), and [Variational Autoencoders](https://en.wikipedia.org/wiki/Autoencoder) as an Assistant Researcher of the [Computational Visualization Center](https://cvcweb.oden.utexas.edu/cvcwp/people/) led by the one and only [Dr. Chandrajit Bajaj](http://www.cs.utexas.edu/~bajaj/cvc/index.shtml)

## Today In CS History

<div>====================================================================================</div>

<div id='date' style='width: 100%;' data-lettercrap-aspect-ratio='0.4'></div>

<script>
    var dt = new Date();
    var month = dt.getMonth() + 1;
    var month_as_string = dt.toLocaleString('default', { month: 'long' });
    var day = dt.getDate();
    var canvas = document.createElement('canvas');
    var ctx = canvas.getContext('2d');
    canvas.width = 500;
    canvas.height = 115;
    ctx.font = "78px Roboto";
    ctx.fillText(month_as_string + ' ' + day, 80 - 8 * month_as_string.length, 85);
    document.getElementById('date').setAttribute('data-letter-crap', (canvas.toDataURL('image/png')));
</script>

<div>====================================================================================</div>

<div id='events'></div>

<script>

    function display_events(data){
        let list = document.createElement('ul');
        list.style.fontSize = '20px';
        for (var i = 0; i < data.length; i++) {
            if (data[i][1] == day && data[i][0] == month) {
                let li = document.createElement('li');

                let link = document.createElement('a');
                link.setAttribute('href', data[i][4]);
                link.appendChild(document.createTextNode(data[i][3]));
                li.appendChild(document.createTextNode(data[i][2] + ': '));
                li.appendChild(link);

                let elem = document.createElement('p');
                elem.style.marginTop = '0em';
                elem.innerHTML = data[i][5];
                let description = document.createTextNode(data[i][5]);
                if (data[i][6] != null) {
                    let source = document.createElement('a');
                    source.setAttribute('href', data[i][6]);
                    source.setAttribute('class', 'source');
                    source.appendChild(document.createElement('br'));
                    source.appendChild(document.createTextNode('source'));
                    elem.appendChild(source);
                }
                li.appendChild(elem);

                li.appendChild(document.createElement('br'));
                let container = document.querySelector("#events");
                list.appendChild(li);
                container.appendChild(list);
            }
        }
    }

    let event_file = '/~bebeal/events.csv';
    Papa.parse(event_file, {
        download: true,
        dynamicTyping: true,
        complete: function(results) {
            display_events(results.data);
        }
    });
</script>


## Contact

| |
|-|
| bnoahbeal@gmail.com                             |
| bebeal@utexas.edu                               |
| [LinkedIn](https://www.linkedin.com/in/bebeal/) |   
| [Github](https://github.com/bebeal)             |  