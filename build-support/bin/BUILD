# Copyright 2019 Pants project contributors (see CONTRIBUTORS.md).
# Licensed under the Apache License, Version 2.0 (see LICENSE).

files(
  name = 'bash_scripts',
  sources = ['*.sh'],
)

# We include this entry, even though the scripts are already covered by individual `python_binary`
# targets, to ensure that tests are able to treat these files as loose source files, i.e. to avoid
# stripping the source root from the files.
files(
  name = 'python_scripts',
  sources = ['*.py'],
)

python_binary(
   name = 'bootstrap_and_deploy_ci_pants_pex',
   sources = ['bootstrap_and_deploy_ci_pants_pex.py'],
   dependencies = [
     ':common',
   ],
   tags = {'type_checked'},
 )

python_binary(
  name = 'check_banned_imports',
  sources = ['check_banned_imports.py'],
  dependencies = [
    ':common',
  ],
  tags = {'type_checked'},
)

python_binary(
  name = 'check_header',
  sources = ['check_header.py'],
  dependencies = [
    ':common',
  ],
  tags = {'type_checked'},
)

python_binary(
  name = 'check_pants_pex_abi',
  sources = ['check_pants_pex_abi.py'],
  dependencies = [
    ':common',
  ],
  tags = {'type_checked'},
)

python_binary(
  name = 'ci',
  sources = ['ci.py'],
  dependencies = [
    ':common',
  ],
  tags = {'type_checked'},
)

python_library(
  name = 'common',
  sources = ['common.py'],
  tags = {'type_checked'},
)

python_binary(
  name = 'deploy_to_s3',
  sources = ['deploy_to_s3.py'],
  dependencies = [
    ':common',
  ],
  tags = {'type_checked'},
)

python_binary(
  name = 'generate_travis_yml',
  sources = 'generate_travis_yml.py',
  dependencies = [
    '3rdparty/python:PyYAML',
  ],
  tags = {'type_checked'},
)

python_binary(
  name = 'get_rbe_token',
  sources = 'get_rbe_token.py',
  dependencies = [
    '3rdparty/python:ansicolors',
    '3rdparty/python:requests',
  ],
  tags = {'type_checked'},
)

python_binary(
  name = 'mypy',
  sources = ['mypy.py'],
  dependencies = [
    ':common',
  ],
  tags = {'type_checked'},
)

python_binary(
  name = 'shellcheck',
  sources = ['shellcheck.py'],
  dependencies = [
    ':common',
  ],
  tags = {'type_checked'},
)
