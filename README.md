<div id="timer"></div>


| <img align="center" src="https://github-readme-stats.vercel.app/api?username=xujiujiu&show_icons=true&include_all_commits=true&hide_border=true&rank_icon=github" alt="xujiujiu's github stats" /> | <img align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=xujiujiu&layout=compact&hide_border=true" /> |
| ------------- | ------------- |


<!---
xujiujiu/xujiujiu is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

<script>
    const targetDate = new Date(1994 + 55, 1, 6).getTime();

    // 更新计时器的函数
    function updateTimer() {
      const currentDate = new Date().getTime();
      const timeRemaining = targetDate - currentDate;

      // 计算小时、分钟和秒
      
      const days = Math.floor((timeRemaining / (1000 * 60 * 60 * 24));
      // const hours = Math.floor((timeRemaining % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      // const minutes = Math.floor((timeRemaining % (1000 * 60 * 60)) / (1000 * 60));
      // const seconds = Math.floor((timeRemaining % (1000 * 60)) / 1000);

      // 更新计时器容器的内容
      const timerElement = document.getElementById('timer');
      timerElement.innerHTML = `距离退休还剩 ${days} 天` //`${hours} 小时 ${minutes} 分钟 ${seconds} 秒`;

      // 如果目标日期已经过去，显示消息
      if (timeRemaining < 0) {
        timerElement.innerHTML = '已退休';
      }
    }

    // 每秒更新一次计时器
    setInterval(updateTimer, 1000);

    // 初始加载时更新计时器
    updateTimer();
</script>
