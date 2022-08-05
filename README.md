## Pip sürümünü yüklemiş olmalıyız.
**Windows**
```
py -m pip install --upgrade pip
```



### Bu işlemleri tamamladıktan sonra pip   kontrolü ve yapı oluşturumuna geçiyoruz.

```
py -m pip install --upgrade build
```

py -m build
```
### Twine ile pypi sitesinde yaptığımız modülün setup linkini ekletmiş oluyoruz bu kısımda kullanıcı adı ve şifre giriyoruz.
```
twine upload dist/*
```
pip install ust-alma  // linkini pypi https://pypi.org/project/ust-alma/ sitesinden elde ediyoruz. 
```
Bu kısımdan sonra pythonumuzun kurulu olduğu klasöre gidiyoruz ve gidişat yolu kısmına cmd yazıyoruz. Açılan pencereye resimde ki gibi aldığımız pip install ust-alma linkini yapıştırıyoruz ve indirimini görüyoruz. Bu kısımdan sonrasında python yazıp modülümüzü belirtiyoruz ve üst alma işlemini gerçekleştiriyoruz.

<img src="https://github.com/malikagan48/Pip/blob/main/PythonPipLibrary/images/Ads%C4%B1z.png?raw=true" width="auto">

Bu işlemden sonra da pipin nereye indirildiğini cmd satırında görebilirsiniz. Bu komutun yoluna baktığımızda ekteki gibi bir klasöre indirildiğini görüyoruz. 


<img src="https://github.com/malikagan48/Pip/blob/main/PythonPipLibrary/images/Ads%C4%B1z1.png?raw=true" width="auto">
