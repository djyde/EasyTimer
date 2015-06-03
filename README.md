# EasyTimer
An easy class help you create Android timer task in right way and feel more comfortable. 

Inspired by: http://android-developers.blogspot.com/2007/11/stitch-in-time.html

# Sample
![](http://ww3.sinaimg.cn/large/62580dd9gw1esqwi715p9g20f00qote0.gif)

# Usage

```java
EasyTimer timer = new EasyTimer();

// Or you can custom the interval, it is 1000 millisecond by default.

EasyTimer timer = new EasyTimer(2000);

timer.setOnTaskRunListener(new EasyTimer.OnTaskRunListener() {
    @Override
    public void onTaskRun(long past_time, String rendered_time) {
        // Change UI or do something with past_time and rendered_time.
        // It will NOT block the UI thread.
    }
});
```

**The thing you should note that is the `rendered_time` is the rendered past_time like `00:00:23`.**

Then you have to operate your timer:

```java
timer.start(); // To start the timer
```

```java
timer.stop(); // To stop the timer
```

# License
MIT License
