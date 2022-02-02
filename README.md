# 101_linux_cronjobs_first_steps
This is a repository to learn how to cron jobs in linux


## Table of Contents
* [Crontab list](#contrab-list)
* [Crontab edit](#contrab-edit)
* [Crontab definition](#crontab-definition)
* [Crontab examples](#contrab-examples)


## Crontab list
This command list all the jobs in the user crontab

```sh
# crontab -l 
```

## Crontab edit
This command edit the user crontab

```sh
# crontab -e
```

## Crontab definition
This is the explanation / definition of how to cron jobs

```sh
 .----------- minute (0 - 59)
 | .--------- hour (0 - 23)
 | | .------- day of month (1 - 31)
 | | | .----- month (1 - 12)
 | | | | .--- day of week (0 - 6) (Sun=0 or 7)
 | | | | |
 * * * * * command to be executed
```

## Crontab examples
Now we are going to show some examples:

```sh
# cron a job at every time
* * * * * /path_to_the_cron_job

# cron a job at every 10th minute
*/10 * * * * /path_to_the_cron_job

# cron a job at every minute 0
0 * * * * /path_to_the_cron_job

# cron a job at minute 0 past every 3rd hour
0 */3 * * * /path_to_the_cron_job

# cron a job at 00:00
0 0 * * * /path_to_the_cron_job

# cron a job at 08:00
0 8 * * * /path_to_the_cron_job

# cron a job at 00:00 on Wednesday
0 0 * * WED /path_to_the_cron_job

# cron a job at 00:00 on every day-of-week from Monday through Friday
0 0 * * 1-5 /path_to_the_cron_job

# cron a job at 00:00 on day-of-month 1
0 0 1 * * /path_to_the_cron_job

# cron a job at 00:00 on day-of-month 1 in every 6th month
0 0 1 */6 * /path_to_the_cron_job

# cron a job at 00:00 on day-of-month 1 in January
0 0 1 1 * /path_to_the_cron_job
```


