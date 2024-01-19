# sunet-licenses

Licenses for use by SUNET projects.

## default.template
The default license used by SUNET projets: It is based on BSD-2-Clause-Views.

### Creation
Baseline file created like so:
```
curl -s https://raw.githubusercontent.com/spdx/license-list-data/main/text/BSD-2-Clause-Views.txt | sed -e 's/<owner>/SUNET/' -e 's/THE COPYRIGHT HOLDERS AND CONTRIBUTORS/SUNET/' -e 's/THE COPYRIGHT HOLDER/SUNET/' -e 's/the copyright holders or contributors/SUNET/' | fmt -w 80 > default.template
```

Afterwards the file has been modified by hand to add the hanging indent for the
numbered list contents that is commonly seen.
### Usage
To fetch the license to your project do this:
```
curl -s https://raw.githubusercontent.com/SUNET/sunet-licenses/main/text/default.template | sed "s/<year>/$(date +%Y)/" > LICENSE
```
