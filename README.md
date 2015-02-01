# madwifi-hopping
# Author: Paul Patras

This is a modified version of the popular madwifi driver authored by Sam Leffler.

Changes were introduced to enable packet transmissions with two distinct power levels, 
chosen randomly with equal probability (power hopping). The goal of this approach is to
cause packet capture deliberatively and alleviate collisions in crowded WLANs. A fix was also 
included to allow the WME parameters update for the best-effort access category.

The following files were modified:
- ath/if_ath.c
- net80211/ieee80211_proto.c
- net80211/ieee80211_node.c

Further details about this technique are given in the following research paper:
- P. Patras, H. Qi, D. Malone, "Mitigating Collisions through Power-Hopping to Improve 802.11 Performance", 
Elsevier Pervasive and Mobile Computing, vol. 11, pp.41–55, Apr. 2014.
