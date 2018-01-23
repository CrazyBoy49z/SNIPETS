------------------
Переотрисовка браузером анимаций
------------------
	function raf(fn){
		window.requestAnimationFrame(function(){
			window.requestAnimationFrame(function(){
				fn();
			})
		})
	}
------------------
События для анимаций
------------------
	addEventListener('transitionend', handler) // Событие окончание транзишина для transition css 
	addEventListener('animationend', handler) // Событие окончание аниматион для keyframes css
	
	--------------jQuery---------------
	
	.on('transitionend', handler)
	.on('animationend', handler)
------------------
Убрать событие с элемента
------------------	
	.removeEventListener('событие', handler) //В данной функции аргументы будут те же самые, которые в самом событии
	
	--------------jQuery---------------
	
	.off('событие', handler)
