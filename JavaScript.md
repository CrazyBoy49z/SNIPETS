-- Переотрисовка браузером анимаций --

function raf(fn){
	window.requestAnimationFrame(function(){
		window.requestAnimationFrame(function(){
			fn();
		})
	})
}
