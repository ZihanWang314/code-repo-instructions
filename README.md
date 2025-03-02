# code-repo-instructions

To write a code repo for a certain research idea, the codebase is usually organized in the below manner:
code-repo
  idea-name/ (source files like a python package)
    __init__.py
    .../
    utils/
      __init__.py
      ...
    
  config/ (config for experiments, including yaml / modeling configs)
    model/ (modeling configs, example below. Can be left empty if the idea is api-based)
      fancy_model/
        modeling_fancy_model.py
        configuration_fancy_model.py
        config.json
        tokenizer_config.json
        ...
    train.yaml (training yaml config)
  
  scripts/ (scripts used to setup environment and do experiments)
    prepare_data.py
    setup.sh # pip install etc. refer to https://github.com/ZihanWang314/RAGEN/blob/main/scripts/setup_ragen.sh

  data/ (save downloaded data, usually active in .gitignore so won't push it to github)
  checkpoints/ (save trained models. usually active in .gitignore)
  public/ (resources in the README.MD like figures, etc)

  README.MD
  main.py # the main script to run
  run.sh # the main bash command to run
  cmd.MD # put all running experiments, different variants compared to the "bash run.sh" or "bash main.py" that supports running different part of experiments in your paper
  setup.py # including package install, copyright information, etc
  .gitignore # please refer to https://github.com/ZihanWang314/RAGEN/blob/main/.gitignore
  requirements.txt
  

  


  data/


, data(left blank in .gitignore), scripts/download_dataset,py, scripts/setup.sh (including everything needed)
