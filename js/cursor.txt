const cursor = document.querySelector('.cursor');

window.addEventListener('mousemove', e => {

    cursor.style.left = e.clientX + 'px';
    cursor.style.top = e.clientY + 'px';

});

const links = document.querySelectorAll('a, button, .card, .project-card');

links.forEach(link => {

    link.addEventListener('mouseenter', () => {

        cursor.style.transform =
            'translate(-50%, -50%) scale(2)';

        cursor.style.background =
            'rgba(0,240,255,0.2)';

        cursor.style.border =
            '1px solid #00f0ff';

    });

    link.addEventListener('mouseleave', () => {

        cursor.style.transform =
            'translate(-50%, -50%) scale(1)';

        cursor.style.background = 'transparent';

    });

});

document.addEventListener('mousedown', () => {

    cursor.style.transform =
        'translate(-50%, -50%) scale(0.8)';

});

document.addEventListener('mouseup', () => {

    cursor.style.transform =
        'translate(-50%, -50%) scale(1)';

});