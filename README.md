# Steps to create a python package

### Step 1 :

- Create a new repository in github
  - choose a license
  - include a readme
  - select .gitignore file for python
### Step 2 :

- #### 2.1
- Create a package directory
  
 ![image](https://github.com/user-attachments/assets/78d2d00d-2b89-4ab3-9a9c-1efdea1684dd)

- #### 2.2 
- Create a module inside the package directory. A module is a single ```.py``` file that contains Python code — it could be functions, classes, or variables
- #### 2.3
- Edit __init__.py
- #### 2.4
- Create setup file (setup.py)
  - Example 1 :
  ```  from setuptools import setup
  setup(
    name='calc-demo',
    version='1.0.0',
    url='https://github.com/Franc6s/demo-package-test',
    author='Francis Mangala',
    author_email='francis@viz-optima.us',
    description='Demo basic calculator',
    license='MIT',
    packages=['calculator']
    )
  ```
  - Example 2 :
    ```
    from setuptools import setup, find_packages

    setup(
    name='MyPackageName',
    version='1.0.0',
    url='https://github.com/mypackage.git',
    author='Author Name',
    author_email='author@gmail.com',
    description='Description of my package',
    packages=find_packages(),    
    install_requires=['numpy >= 1.11.1', 'matplotlib >= 1.5.1']
    )
    ```
  - Example 3 :
    ```
    from setuptools import setup

    setup(
    name = 'PackageName',
    version = '0.1.0',
    author = 'An Awesome Coder',
    author_email = 'aac@example.com',
    packages = ['package_name', 'package_name.test'],
    scripts = ['bin/script1','bin/script2'],
    url = 'http://pypi.python.org/pypi/PackageName/',
    license = 'LICENSE.txt',
    description = 'An awesome package that does something',
    long_description = open('README.txt').read(),
    install_requires = [
        "Django >= 1.1.1",
        "pytest",
    ]
    )
    ```
- Put the test file above the package directory, in the root of the project directory.
- Stage, commit, and push all the files you've created.
- #### Step 3 :
- Install your package with pip. ``` pip install . ``` (make sure to include the .)
