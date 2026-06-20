document.addEventListener('DOMContentLoaded', function() {

    console.log('Сайт театра «Ёркен риг» загружен');

    const mainBtn = document.getElementById('mainBtn');
    if (mainBtn) {
        mainBtn.addEventListener('click', function() {
            alert('Я сказал нет. Убери свои грязные пальчики от кнопки, маленький негодяй.');
        });
    }

    const ticketsBtn = document.getElementById('ticketsBtn');
    if (ticketsBtn) {
        ticketsBtn.addEventListener('click', function() {
            alert('Билеты можно приобрести в кассе театра ежедневно с 10:00 до 19:00. Адрес: г. Астана, ул. Театральная, 1. Телефон для справок: +7 (777) 123-45-67');
        });
    }

    const lightbox = document.getElementById('lightbox');
    const lightboxImg = document.getElementById('lightbox-img');
    const lightboxCaption = document.getElementById('lightbox-caption');
    const closeBtn = document.querySelector('.lightbox-close');

    if (lightbox && lightboxImg) {
        const images = document.querySelectorAll('.afisha-img');

        images.forEach(img => {
            img.addEventListener('click', function(e) {
                e.stopPropagation();
                e.preventDefault();
                lightbox.style.display = 'flex';
                lightboxImg.src = this.src;
                let captionText = this.getAttribute('alt') || 'Афиша';
                const parentCard = this.closest('.spectacle-card') || this.closest('.afisha-card');
                if (parentCard) {
                    const nameEl = parentCard.querySelector('.afisha-name') || parentCard.querySelector('h3');
                    if (nameEl) {
                        captionText = nameEl.textContent.trim() + ' — афиша';
                    }
                }
                lightboxCaption.textContent = captionText;
                document.body.style.overflow = 'hidden';
            });
        });

        if (closeBtn) {
            closeBtn.addEventListener('click', function(e) {
                e.stopPropagation();
                lightbox.style.display = 'none';
                document.body.style.overflow = 'auto';
            });
        }

        lightbox.addEventListener('click', function(e) {
            if (e.target === this) {
                lightbox.style.display = 'none';
                document.body.style.overflow = 'auto';
            }
        });

        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape' && lightbox.style.display === 'flex') {
                lightbox.style.display = 'none';
                document.body.style.overflow = 'auto';
            }
        });
    }
});
