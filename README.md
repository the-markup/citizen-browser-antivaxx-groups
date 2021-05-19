# Citizen Browser: Facebook recommendations for anti-vaccine groups
This repository contains data from the story ["Facebook Said It Would Stop Recommending Anti-Vaccine Groups. It Didn’t"](https://themarkup.org/citizen-browser/2021/05/20/facebook-said-it-would-stop-recommending-anti-vaccine-groups-it-didnt) from from our series, [Citizen Browser](https://themarkup.org/citizen-browser/).

Our methodology is described in "[How We Built a Facebook Inspector](https://themarkup.org/citizen-browser/2021/01/05/how-we-built-a-facebook-inspector)."

## Data
The `data/` directory contains files with data from the story.

1. `health_keywords.txt` contains a list of 12 health- or illness-related keywords that were used to identify an initial list of groups that were likely to be focused on health.
2. `negative_keywords.txt` contains a list of terms we used as a broad filter to remove groups that were not truly related to human physical or mental health.
3.  `recommended_health_groups.csv` contains the full list of groups recommended to Citizen Browser panelists that contained one or more of the health keywords and no negative keywords in the group name.
4. `anti-vaccine_content.csv` contains a list of groups and pages recommended to panelists that were dedicated mainly to the sharing of anti-vaccine misinformation.
5. `anti-mask_content.csv` contains a list of groups and pages recommended to panelists that were dedicated mainly to criticizing or discouraging the wearing of masks.

-----

Data in the `recommended_health_groups.csv` file is arranged as follows:
| column           | decription                                                                                |
|:-----------------|:------------------------------------------------------------------------------------------|
| group_name       | Name of the group at time of data collection                                              |
| first_sighted    | Earliest date in the investigation time period that the group was recommended to a panelist |
| last_sighted     | Latest date in the investigation time period that the group was recommended to a panelist |
| group_slug       | The unique identifier from the the group URL, i.e. facebook.com/groups/<group_slug>      |
| n_members        | The number of group members, recorded at the most recent date it was recommended       |

Data in `anti-vaccine_content.csv` and `anti-mask_content.csv` is arranged as follows:
| column           | decription                                                                                |
|:-----------------|:------------------------------------------------------------------------------------------|
| group_name       | Name of the group or page at time of data collection                                      |
| type             | Indicates whether the named entity is a group or page                                     |
| first_sighted    | Earliest date the entity was recommended to a panelist |
| last_sighted     | Latest date the entity was recommended to a panelist |
| url              | Direct URL to view the group or page. Note that many groups are private and membership must be requested.      |
| n_members        | The number of members (only applicable to groups, not pages)       |
-----
## Licensing
Copyright 2021, The Markup News Inc.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
