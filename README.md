# docker-compose
compose yml库
## 常用命令
```bash
# 默认使用docker-compose.yml构建镜像
docker-compose build
docker-compose build --no-cache # 不带缓存的构建

# 指定不同yml文件模板用于构建镜像
docker-compose build -f docker-compose1.yml

# 列出Compose文件构建的镜像
docker-compose images

# 启动所有编排容器服务
docker-compose up -d

# 查看正在运行中的容器
docker-compose ps

# 查看所有编排容器，包括已停止的容器
docker-compose ps -a

# 进入指定容器执行命令
docker-compose exec nginx bash
docker-compose exec web python manage.py migrate --noinput

# 查看web容器的实时日志
docker-compose logs -f web

# 停止所有up命令启动的容器
docker-compose down

# 停止所有up命令启动的容器,并移除数据卷
docker-compose down -v

# 重新启动停止服务的容器
docker-compose restart web

# 暂停web容器
docker-compose pause web

# 恢复web容器
docker-compose unpause web

# 删除web容器，删除前必需停止stop web容器服务
docker-compose rm web

# 查看各个服务容器内运行的进程
docker-compose top                     
```