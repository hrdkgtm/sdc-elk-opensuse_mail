# SDC & ELK Files for Opensuse Mail

This project contains the pipelines used in SDC and Elastic index mapping for Opensuse Mailing List Data. Created for ease of replication

## Getting Started

Cloning this repository to your local system 

```
$ git clone .,,
```

### Prerequisites

- A running ELK Cluster (Elasticsearch 6.x)
- Streamsets Data Collector (3.7.1)
- Scraped mail data in json format like:
    
    ```
    {"subject": "[Bug 1117086] Automatic cleanup of old kernels not working", "origin": "bugzilla_noreply@xxxxxxxxxx", "date": "Sat, 01 Dec 2018 00:47:41 +0000", "src_link": "https://lists.opensuse.org/opensuse-bugs/2018-12/msg00000.html", "reference_link": ["http://bugzilla.opensuse.org/show_bug.cgi?id=1117086", "http://bugzilla.opensuse.org/show_bug.cgi?id=1117086#c3"], "msg_body": "\n\n\nhttp://bugzilla.opensuse.org/show_bug.cgi?id=1117086\nhttp://bugzilla.opensuse.org/show_bug.cgi?id=1117086#c3\n\nbob wheater <bwheater@xxxxxxx> changed:\n\n           What    |Removed                     |Added\n----------------------------------------------------------------------------\n                 CC|                            |bnc-team-screening@xxxxxxxx\n                   |                            |ovo.novell.com\n   Target Milestone|---                         |Leap 15.0\n              Flags|                            |needinfo?(bnc-team-screenin\n                   |                            |g@xxxxxxxxxxxxxxxxxxxxxx)\n\n--- Comment #3 from bob wheater <bwheater@xxxxxxx> ---\nWhat is the status of this bug report?\n\n-- \nYou are receiving this mail because:\nYou are on the CC list for the bug.\n\n\n\n\n"}
    ```

### Importing Files to The Cluster

## Deployment

Deploying these files to a live system only require Import steps in the SDC and using the Dev Tools from kibana

### Importing pipelines to SDC

- Log in to the Streamsets Data Collector
- From the left menu select `Import Pipeline`
- Choose the appropriate pipeline from the cloned repository
- Modify it as necessary

### Creating the Index in Elastic Stack

This project contains 2 files for Elastic, `elastic-devtools.txt` and `elastic-curl.txt` which can be as easy as copying and pasting using the appropriate tool (Dev-Tools in kibana / cURL)

## Built With

* Streamsets Data Controller
* Elasticsearch 6.x

## Versioning
   
Versioning being used for tracking releases.

## Known issues
   
* All the known problems, bugs listed here. Add link to issues if any.

## License

This project is licensed under the XYZ License - see the LICENSE.md file for details
