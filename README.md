# django-notes
- 视图
  ```
  class A():
    pass
  Class B():
    a = models.ForeignKey(A, on_delete=models.CASCADE)
  Class BView():
    # 由于B类a字段on_delele设置为CASCADE，视图a字段on_delete需要设置为DO_NOTHING，否则A类实例无法删除。
   a = models.ForeignKey(A, on_delete=models.DO_NOTHING)
  ```
- Queryset

如果一次性循环大量数据，可用iterator(), 避免占用大量内存

> django.core.exceptions.ImproperlyConfigured: Error loading MySQLdb module. Did you install mysqlclient?

```
pip install --force-reinstall --ignore-installed --no-binary :all: mysqlclient

pip install mysql-python
apt-get install python3-mysqldb libmysqlclient-dev python-dev
```

> 安装python外源包时，如mysqlclient，需安装python-dev
