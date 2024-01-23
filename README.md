# sunet-licenses

Licenses for use by SUNET projects.

## default.template
The default license used by SUNET projets: It is based on BSD-2-Clause-Views.

### Creation
Baseline file created like so:
```
curl -s https://raw.githubusercontent.com/spdx/license-list-data/main/text/BSD-2-Clause-Views.txt | sed -e 's/<owner>/SUNET/' -e 's/THE COPYRIGHT HOLDERS AND CONTRIBUTORS/SUNET/' -e 's/THE COPYRIGHT HOLDER/SUNET/' -e 's/the copyright holders or contributors/SUNET/' | fmt -w 80 > default.template
```

The baseline file has then been modified by hand to add the following:
* Hanging indent for the numbered list contents that is commonly seen.
* A dot between the owner name and `All rights reserved.` This is present in existing versions for the SUNET license, a ticket has been opened upstream for this: https://github.com/spdx/license-list-XML/issues/2336
### Usage
To fetch the license to your project do this:
```
curl -s https://raw.githubusercontent.com/SUNET/sunet-licenses/main/default.template | sed "s/<year>/$(date +%Y)/" > LICENSE
```
