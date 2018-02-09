------------------
Переотрисовка браузером анимаций
------------------
	function raf(fn){ //fn - функция, в которой анимации нужно перендерить
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

------------------
Делегирование событий
------------------
	var btnSendCallBack = $('button.btn-send');
	btnSendCallBack.on('click',function(event){
		var target = event.target;
		while(target != 'FORM'){
		    if(target.tagName == 'FORM'){
			console.log('нашли нужный элемент')
			return;
		    }
		    target = target.parentNode;
		}  
    	})
