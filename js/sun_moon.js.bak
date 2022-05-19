function checkNightMode() {
   '1' === localStorage.getItem('isDark') ? ($('body').addClass('DarkMode'), $('#changeMode-top').removeClass('fa-moon').addClass('fa-sun'), $('#modeicon').attr('xlink:href', '#icon-sun')) : '0' === localStorage.getItem('isDark') ? $('#modeicon').attr('xlink:href', '#icon-moon') : new Date().getHours() >= 20 || new Date().getHours() < 7 ? ($('body').addClass('DarkMode'), $('#changeMode-top').removeClass('fa-moon').addClass('fa-sun'), $('#modeicon').attr('xlink:href', '#icon-sun')) : matchMedia('(prefers-color-scheme: dark)').matches ? ($('body').addClass('DarkMode'), $('#changeMode-top').removeClass('fa-moon').addClass('fa-sun'), $('#modeicon').attr('xlink:href', '#icon-sun')) : $('#modeicon').attr('xlink:href', '#icon-moon')
 }
 function switchNightMode() {
   $('<div class="Cuteen_DarkSky"><div class="Cuteen_DarkPlanet"></div></div>').appendTo($('body')),
     setTimeout(function () {
       $('body').hasClass('DarkMode') ? ($('body').removeClass('DarkMode'), localStorage.setItem('isDark', '0'), $('#changeMode-top').removeClass('fa-sun').addClass('fa-moon'), $('#modeicon').attr('xlink:href', '#icon-moon')) : ($('body').addClass('DarkMode'), localStorage.setItem('isDark', '1'), $('#changeMode-top').removeClass('fa-moon').addClass('fa-sun'), $('#modeicon').attr('xlink:href', '#icon-sun')),
         setTimeout(function () {
           $('.Cuteen_DarkSky').fadeOut(1e3, function () {
             $(this).remove()
           })
         }, 2e3)
     })
     const nowMode = document.documentElement.getAttribute('data-theme') === 'dark' ? 'dark' : 'light'
     if (nowMode === 'light') {
       activateDarkMode()
       saveToLocal.set('theme', 'dark', 2)
       GLOBAL_CONFIG.Snackbar !== undefined && btf.snackbarShow(GLOBAL_CONFIG.Snackbar.day_to_night)
       $('#modeicon').attr('xlink:href', '#icon-moon')
     } else {
       activateLightMode()
       saveToLocal.set('theme', 'light', 2)
       GLOBAL_CONFIG.Snackbar !== undefined && btf.snackbarShow(GLOBAL_CONFIG.Snackbar.night_to_day)
       $('body').addClass('DarkMode'), $('#changeMode-top').removeClass('fa-moon').addClass('fa-sun'), $('#modeicon').attr('xlink:href', '#icon-sun')
     }
     // handle some cases
     typeof utterancesTheme === 'function' && utterancesTheme()
     typeof FB === 'object' && window.loadFBComment()
     window.DISQUS && document.getElementById('disqus_thread').children.length && setTimeout(() => window.disqusReset(), 200)
 }
 function switchNightModeTop() {
   $('body').hasClass('DarkMode') ? ($('body').removeClass('DarkMode'), localStorage.setItem('isDark', '0'), $('#changeMode-top').removeClass('fa-sun').addClass('fa-moon'), $('#modeicon').attr('xlink:href', '#icon-moon')) : ($('body').addClass('DarkMode'), localStorage.setItem('isDark', '1'), $('#changeMode-top').removeClass('fa-moon').addClass('fa-sun'), $('#modeicon').attr('xlink:href', '#icon-sun'))
 }