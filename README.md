# dot-no

List of .no domains.

## Results

### 2024-12-10
* Source: Dump of `*.no` from https://merklemap.com from 2024-12-09. Thanks a lot to merklemap for this dataset, originally from CT logs.
* Stats: 523655 of at the time, 857162 domains: 61.09%.
* Commands:
  * merklemap data run through `nogrep.2024-12-09` in https://github.com/Kagee/mcn-tools-norid-cat-domains/ to find unique domains and category domains.
  * `massdns -r <file with *.nic.no resolvers> -t NS --norecurse "$INPUT_LIST" -w "$OUTFILE" -o J -c 3 -s 5`
  * `jq select(.status=="NOERROR") result_NS.2024-12-10-00-45.json | gzip > result_NS_NOERROR.2024-12-10-00-45.json.gz`
  * `jq -r '.name' result_NS_NOERROR.2024-12-10-00-45.json | sed 's/.$//' > result_NS_NOERROR.2024-12-10-00-45.txt`
  * 523655/857162*100
