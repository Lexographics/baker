# Baker

wget-and-use tool to bake your resource into your C/C++ code

## Usage
### Downloading
```sh
wget https://raw.githubusercontent.com/Lexographics/baker/main/baker.rb
```

### Running baker
```sh
  ruby baker.rb --help

  ruby baker.rb   --help, -h                prints usage
  ruby baker.rb   --version                 prints version information
  ruby baker.rb   --ext {extension}         extension for generated files (default: .h)
  ruby baker.rb   --namespace {namespace}   namespace for generated files (default: )
  ruby baker.rb   --dir {directory}         directory to lookup resources (default: ./)
  ruby baker.rb   --always-generate         if present, will not check file modification dates
  ruby baker.rb   --recursive               checks for resources in {dir} recursively
```
<br>

- After running baker.rb, C/C++ header files will be generated from the files in the {dir} 

<img src="res/code.png"/>

### Config Files
Config files can be used to save configuration instead of typing them to console.
To use config file, create a file in working directory named `baker_config.yml`
```yml
  # example baker_config.yml file
  extension: .h
  namespace: res
  dir: res
  always_generate: false
  recursive: true
```
Note: Command line arguments will override config file
