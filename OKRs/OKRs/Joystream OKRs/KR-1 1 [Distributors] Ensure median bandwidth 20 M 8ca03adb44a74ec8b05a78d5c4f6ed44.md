# KR-1.1 [Distributors] Ensure median bandwidth > 20 Mbps and median TTFB < 350 ms for all deployment locations (across multiple tests).

Assignee: Distributor WG
Parent item: [2024 Q1] O-1-1 Improve Joystream as a Video Platform (%5B2024%20Q1%5D%20O-1-1%20Improve%20Joystream%20as%20a%20Video%20Platf%2070ee7f8b6c2d401195de1f1348b1454a.md)
Progress: ◾️◾️◾️◾️◾️◾️◾️◾️◾️◾️ 100%
Status: Completed ⭐️
Last Updated: March 8, 2024
Last edited time: June 18, 2024 6:31 PM

(1) Deployment locations: N. Virginia, Sao Paolo, Madrid, Mumbai, Jakarta, Seoul.

(2) Cached assets only consider for testing

(3) Synthetic tests details

[https://joystream.notion.site/CDN-Performance-standard-79000919c67d4aba8fa90541cfee9f93](https://www.notion.so/CDN-Performance-standard-79000919c67d4aba8fa90541cfee9f93?pvs=21)

- Improve geographic node coverage by hiring workers for South America + Africa
- Improve benchmarking process by reviewing the code (not sure eg if the TTFB includes DNS resolution time + handshakes time ) and maybe deploy scripts for more locations for the ping tool
- Investigate Argus node selection by Orion and Atlas
- Investigate usage of CloudFlare workers for improved bandwidth
- Improve CPU usage of Argus node (this is to be attained by siding Argus with a bespoke squid and reducing state cleanup to once a week). This should lower latency for video requests
- Collect data from end-users of apps (Gleev) to see perceived performance

### **21 Feb 2024**

- Switch resources to SWG/DWG merge plan? Ignazio would spent much of time on Luxor release
- **Very important to do now:**
    - Collect data from end-users of Gleev
    - Improve CPU usage of Argus node
- **Immediate focus for next term:**
    - consolidation work
    
    Improve geographic node coverage by hiring workers for South America + Africa
    
    - Africa node - not really relevant now.
    
    Remaining 40% of progress:
    
    - Improve CPU usage of Argus node (depends on the Argus new release)
    
    - Collect data from end-users of apps (Gleev) to see perceived performance
    
    - Investigate usage of CloudFlare workers for improved bandwidth
    
    ### 7 March 2024
    
    Gleev has indexed logs for metrics, however there are errors in them, so a proper benchmark is not possible yet
    However as we have already established, via the ping tool, (which measures  those metrics only in specific locations) we might want to keep the rating (achivemente stars) at the same level.
    
    ### 8 March 2024
    
    - During midterm, per mrbovo (WG lead) we are on track, likely on 80%
    - re: Errors in log as per last update, there is a GH issue and it is being addressed as per mrbovo (WG lead)
    
    ### 30 Apr 2024
    
    KR fully achieved 
    
    Score 1.0
    
    Evidence is elastic search dashboard 
    
    Note: next time adjust target to make it more challenging