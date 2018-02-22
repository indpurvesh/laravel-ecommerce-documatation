# Theme for Mage2 E commerce

- [Theme Createtion](#create-theme)
    - [Folder Structure](#themes-folder-structure)
    - [register.yaml] (#themes-register-file)
    - [assets](#themes-assets)
    - [views](#themes-views)
    - [lang](#theme-translation)

<a name="create-theme"></a>
### Create Theme
Theme development is one of the key component in enhancement of Mage2 E commerce frontend.


<a name="themes-folder-structure"></a>

### Folder Strucuture

- ./themes/
    - company-name (mage2)
        - theme-name (default)
            - assets
                - js
                - css 
                - fonts
                - images
                - sass
          - views
          - register.yaml
              

<a name="themes-register-yaml"></a>    
### Register Yaml File                  
 
Register.yaml file the key to register most related path and information about the theme. Things that needs to be careful here is your identifier neeeds to be unique.

    name: mage2-material
    asset_folder_name: assets
    lang_folder_name: lang
 
Once you have an theme register and files setup then you can go to admin=>system=>themes and Activate theme publish all the css/js/images into public/vendor/theme-identifier folder for you. 

### Theme Assets (Using and css/js) into layout files

Once you have theme activate and moved all your css/js/images into public folder then you can simply just it.

How to add Css into layout files.

    <link href="{{ asset('vendor/mage2-default/css/bootstrap.min.css') }}" rel="stylesheet">
    
How to add Javascript into layout files.

    <script src="{{ asset('/vendor/mage2-default/js/jquery-3.2.1.slim.min.js') }}"></script>
    
    
    
### How to use into Sass into webpack.mix.js files

    mix.sass('themes/mage2/default/assets/sass/app.scss', 'public/vendor/mage2-default/css/app.css');
    
    
    mix.scripts(['themes/mage2/default/js/jquery-3.2.1.min.js',
                'themes/mage2/default/js/popper.min.js',
                'themes/mage2/default/js/bootstrap.min.js], 
                
                    'public/vendor/mage2-default/js/app.js');
