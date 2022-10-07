g++ -o server  main.cpp timer/lst_timer.cpp http/http_conn.cpp log/log.cpp CGImysql/sql_connection_pool.cpp webserver.cpp config.cpp -g -lpthread -lmysqlclient
In file included from ./threadpool/threadpool.h:9,
                 from webserver.h:15,
                 from config.h:4,
                 from main.cpp:1:
./threadpool/../CGImysql/sql_connection_pool.h:6:10: fatal error: mysql/mysql.h: No such file or directory
    6 | #include <mysql/mysql.h>
      |          ^~~~~~~~~~~~~~~
compilation terminated.
In file included from timer/../http/http_conn.h:25,
                 from timer/lst_timer.cpp:2:
timer/../http/../CGImysql/sql_connection_pool.h:6:10: fatal error: mysql/mysql.h: No such file or directory
    6 | #include <mysql/mysql.h>
      |          ^~~~~~~~~~~~~~~
compilation terminated.
In file included from http/http_conn.h:25,
                 from http/http_conn.cpp:1:
http/../CGImysql/sql_connection_pool.h:6:10: fatal error: mysql/mysql.h: No such file or directory
    6 | #include <mysql/mysql.h>
      |          ^~~~~~~~~~~~~~~
compilation terminated.
In file included from log/log.cpp:5:
log/log.h: In static member function ‘static void* Log::flush_log_thread(void*)’:
log/log.h:26:5: warning: no return statement in function returning non-void [-Wreturn-type]
   26 |     }
      |     ^
In file included from log/log.cpp:5:
log/log.h: In member function ‘void* Log::async_write_log()’:
log/log.h:47:5: warning: no return statement in function returning non-void [-Wreturn-type]
   47 |     }
      |     ^
log/log.cpp: In member function ‘bool Log::init(const char*, int, int, int, int)’:
log/log.cpp:57:54: warning: ‘%s’ directive output may be truncated writing up to 127 bytes into a region of size between 92 and 247 [-Wformat-truncation=]
   57 |         snprintf(log_full_name, 255, "%s%d_%02d_%02d_%s", dir_name, my_tm.tm_year + 1900, my_tm.tm_mon + 1, my_tm.tm_mday, log_name);
      |                                                      ^~
log/log.cpp:57:17: note: ‘snprintf’ output between 9 and 291 bytes into a destination of size 255
   57 |         snprintf(log_full_name, 255, "%s%d_%02d_%02d_%s", dir_name, my_tm.tm_year + 1900, my_tm.tm_mon + 1, my_tm.tm_mday, log_name);
      |         ~~~~~~~~^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
log/log.cpp: In member function ‘void Log::write_log(int, const char*, ...)’:
log/log.cpp:119:41: warning: ‘%s’ directive output may be truncated writing up to 127 bytes into a region of size between 113 and 255 [-Wformat-truncation=]
  119 |             snprintf(new_log, 255, "%s%s%s.%lld", dir_name, tail, log_name, m_count / m_split_lines);
      |                                         ^~
log/log.cpp:119:21: note: ‘snprintf’ output between 3 and 291 bytes into a destination of size 255
  119 |             snprintf(new_log, 255, "%s%s%s.%lld", dir_name, tail, log_name, m_count / m_split_lines);
      |             ~~~~~~~~^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
log/log.cpp:113:41: warning: ‘%s’ directive output may be truncated writing up to 127 bytes into a region of size between 113 and 255 [-Wformat-truncation=]
  113 |             snprintf(new_log, 255, "%s%s%s", dir_name, tail, log_name);
      |                                         ^~
log/log.cpp:113:21: note: ‘snprintf’ output between 1 and 270 bytes into a destination of size 255
  113 |             snprintf(new_log, 255, "%s%s%s", dir_name, tail, log_name);
      |             ~~~~~~~~^~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
CGImysql/sql_connection_pool.cpp:1:10: fatal error: mysql/mysql.h: No such file or directory
    1 | #include <mysql/mysql.h>
      |          ^~~~~~~~~~~~~~~
compilation terminated.
In file included from ./threadpool/threadpool.h:9,
                 from webserver.h:15,
                 from webserver.cpp:1:
./threadpool/../CGImysql/sql_connection_pool.h:6:10: fatal error: mysql/mysql.h: No such file or directory
    6 | #include <mysql/mysql.h>
      |          ^~~~~~~~~~~~~~~
compilation terminated.
In file included from ./threadpool/threadpool.h:9,
                 from webserver.h:15,
                 from config.h:4,
                 from config.cpp:1:
./threadpool/../CGImysql/sql_connection_pool.h:6:10: fatal error: mysql/mysql.h: No such file or directory
    6 | #include <mysql/mysql.h>
      |          ^~~~~~~~~~~~~~~
compilation terminated.
make: *** [makefile:12: server] Error 1