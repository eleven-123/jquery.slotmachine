

JS常用属性、方法、事件详解:

1、初始化方法 var machine = $("#id").slotMachine({}); 返回当前旋转的对象。
     slotMachine()方法里面传递初始化的参数，如:     
          active：表示初始化的时候显示项的索引，从0开始 
          delay：切换两张图片的间隔时间（毫秒单位）
          auto：是否自动旋转，取值为true or false
          spins：当auto为true的时候，这是每次跳过图标的个数
          stophidden：是否出现开始和停止时候的动画 
          randomize:function(activeElementIndex){}此属性表示每次旋转后选中值的索引（从0开始）
          direction：动画的方向，取值（up||down）

2、常用方法：
     machine.shuffle( repeat, onStopCallback );表示开始旋转，repeat表示每次跳过的图片个数；onstopCallback表示旋转停止后的事件回调方法。
     machine.prev(); 返回前一个元素
     machine.next(); 返回后一个元素
     machine.stop(); 停止旋转
     machine.active; 得到选中的元素的索引
     machine.running; 检测是否正在旋转，true表示正在旋转
     machine.stopping; 检测是否已经停止
     machine.destroy(); 摧毁旋转节点
