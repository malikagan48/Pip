## Pip sürümünü yüklemiş olmalıyız.
**Windows**
```
py -m pip install --upgrade pip
```

## Daha sonrasında aşağıdaki yapıya benzer bir model oluşturun.
```
packaging_tutorial/
├── LICENSE
├── pyproject.toml
├── README.md
├── setup.cfg
├── src/
│   └── GetMode/
│       ├── __init__.py
│       └── Mode.py
└── tests/
touch LICENSE
touch pyproject.toml
touch setup.cfg
mkdir src/mypackage
touch src/mypackage/__init__.py
touch src/mypackage/main.py
mkdir tests
```

## pyproject.toml 

Bu dosya, pip ve build gibi araçlara projenizi nasıl oluşturacağınızı anlatır.

```
[build-system]
requires = [
    "setuptools>=42",
    "wheel"
]
build-backend = "setuptools.build_meta"
```
build-system.requires, paketinizi oluşturmak için gereken paketlerin bir listesini verir. Burada bir şey listelemek, onu kurulduktan sonra değil, yalnızca derleme sırasında kullanılabilir hale getirecektir.

build-system.build-backend, derlemeyi gerçekleştirmek için kullanılacak Python nesnesinin adıdır. Flit veya şiir gibi farklı bir yapı sistemi kullanacak olsaydınız, bunlar buraya gelirdi ve yapılandırma ayrıntıları aşağıda açıklanan setuptools yapılandırmasından tamamen farklı olurdu.

# Setup.cfg setup
setup.cfg kullanmak en iyi uygulamadır, ancak setup.py kullanarak dinamik bir kurulum dosyanız olabilir.

```
[metadata]
name = ust_alma
author = Mustafa ali Kağan Küçük
version =  0.0.1
author_email = mustafa.ali.kagan@gmail.com
description = My Own PIP
long_description = file: README.md
long_description_content_type = text/markdown
url = https://github.com/malikagan48/Pip
project_urls =
    Bug Tracker = https://github.com/malikagan48/Pip
classifiers =
    Programming Language :: Python :: 3
    License :: OSI Approved :: MIT License
    Operating System :: OS Independent

[options]
package_dir =
    = src
packages = find:
python_requires = >=3.6
install_requires=['scikit-learn'],

[options.packages.find]
where = src

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

<img src="https://github.com/malikagan48/Pip/PythonPipLibrary/images/Adsız.PNG" width="auto">

Bu işlemden sonra da pipin nereye indirildiğini cmd satırında görebilirsiniz. Bu komutun yoluna baktığımızda ekteki gibi bir klasöre indirildiğini görüyoruz. 

<img src="https://github.com/malikagan48/Pip/PythonPipLibrary/images/Adsız1.PNG" width="auto">
