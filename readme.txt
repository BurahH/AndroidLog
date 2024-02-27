1 версия
2024-02-27 17:39:28.981 15577-15577 MainActivity            com.example.firstapp                 D  onCreate
2024-02-27 17:39:29.029 15577-15577 MainActivity            com.example.firstapp                 D  onStart
2024-02-27 17:39:29.031 15577-15577 MainActivity            com.example.firstapp                 D  onResume

Здесь происходит настройка, создание и дальнейшее отображение activity. Остановка проиходит на методе onResume, ведь activity отображается у нас на экране

2 версия

2024-02-27 17:45:13.689 21071-21071 MainActivity            pid-21071                            D  onCreate
2024-02-27 17:45:13.748 21071-21071 MainActivity            pid-21071                            D  onStart
2024-02-27 17:45:13.749 21071-21071 MainActivity            pid-21071                            D  onResume
2024-02-27 17:45:15.026   527-569   ActivityTaskManager     system_server                        I  Displayed com.example.firstapp/.MainActivity: +1s807ms
2024-02-27 17:45:20.228 21071-21071 MainActivity            com.example.firstapp                 D  onPause
2024-02-27 17:45:20.237 21071-21071 MainActivity            com.example.firstapp                 D  onStop
2024-02-27 17:45:20.254 21071-21071 MainActivity            com.example.firstapp                 D  onDestroy
2024-02-27 17:45:20.267   527-2246  InputManager-JNI        system_server                        W  Input channel object '4dd588c com.example.firstapp/com.example.firstapp.MainActivity (client)' was disposed without first being removed with the input manager!
2024-02-27 17:45:20.297 21071-21071 MainActivity            com.example.firstapp                 D  onCreate
2024-02-27 17:45:20.301 21071-21071 MainActivity            com.example.firstapp                 D  onStart
2024-02-27 17:45:20.302 21071-21071 MainActivity            com.example.firstapp                 D  onResume

Здесь сначала происходит то же что и в 1 версии, затем при повороте экрана изначальный activity удаляется и создается новый, с учетом поворота экрана 

3 версия

2024-02-27 17:45:57.795 21826-21826 MainActivity            pid-21826                            D  onCreate
2024-02-27 17:45:58.520 21826-21826 MainActivity            com.example.firstapp                 D  onDestroy

Из-за вызова finish() при настройке activity он не будет создан и выведен на экран
