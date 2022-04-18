---
title: Home
type: docs
---

# Home

-----------

## This Website

This website serves as a place to store my thoughts/opinions on various topics, provide a deeper look into some of my projects, provide helpful resources to my students (when I was a TA) and house anything else I might want on it. {{< cite "VizDoom" >}}

## About Me

* My name is Benjamin Beal, but I normally go by Noah (my middle name).
* UTCS BS Class of 22'
* I'm deeply interested in topics involving AI, DL/ML and many of my most up to date projects and though pieces involve them  {{< cite "VizDoom2" >}}

## Today In CS History

---

<div id="cdate" class="custom-date"></div>

<script>
    function getPX(canvas, numChars) {
        return 1/numChars * canvas.width;
    }
    function getFont(px) {
        return (px |0) + 'px roboto mono';
    }
    var dt = new Date();
    var month = dt.getMonth() + 1;
    var month_as_string = dt.toLocaleString('default', { month: 'long' });
    var day = dt.getDate();
    var canvas = document.createElement('canvas');
    var cdate = document.getElementById('cdate');
    var ctx = canvas.getContext('2d');
    var style = getComputedStyle(document.querySelector('.custom-date'));
    var value = ' ' + month_as_string + ' ' + day;
    canvas.width = style.width.slice(0, style.width.length - 2);
    canvas.height = style.height.slice(0, style.height.length - 2);
    var fontSize = getPX(canvas, value.length);
    var font = getFont(fontSize);
    ctx.font = font;
    ctx.fillText(value, -20, canvas.height/3.5, canvas.width);

    // determines if in small-screen/mobile mode
    if (getComputedStyle(document.getElementById('toc-control')).display != 'none') {
        cdate.appendChild(canvas);
    } else {
        let image = (canvas.toDataURL('image/png'));
        cdate.setAttribute('data-letter-crap', (image));
    }
</script>

---

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

<script>
    var toc = document.getElementById('contact');
    toc.style = "height: 0px;width: 0px;overflow:hidden";
</script>

| Contact |
|-|
| bnoahbeal@gmail.com                             |
| bebeal@utexas.edu                               |
| [LinkedIn](https://www.linkedin.com/in/bebeal/) |
| [Github](https://github.com/bebeal)             |  

{{<katex>}}
{{</katex>}}

{{< references >}}

{{< reference "VizDoom" "https://hugo-book-demo.netlify" >}}
{{< reference "VizDoom2" "https://hugo-book-demo.netlify" >}}

{{< /references >}}

