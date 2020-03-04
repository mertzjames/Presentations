# Protected Python: It's Time We Had 'the Talk' About Security

- Introduction
    - Recent Attacks/News/Articles
        - https://medium.com/@bertusk/cryptocurrency-clipboard-hijacker-discovered-in-pypi-repository-b66b8a534a8
        - https://www.bleepingcomputer.com/news/security/ten-malicious-libraries-found-on-pypi-python-package-index/
        - https://arstechnica.com/information-technology/2017/09/devs-unknowingly-use-malicious-modules-put-into-official-python-repository/
        - http://www.blog.pythonlibrary.org/2018/10/31/more-typo-squatting-malware-found-on-pypi/
        - https://www.vice.com/en_us/article/3a8ajj/an-off-the-shelf-skeleton-project-experts-analyze-the-app-that-broke-iowa
            - “Honestly, the biggest thing is—I don’t want to throw it under the bus—but the app was clearly done by someone following a tutorial. It’s similar to projects I do with my mentees who are learning how to code,”
            - Don't be this guy
    - What is Cybersecurity?
        - https://i.pinimg.com/736x/9d/fb/d7/9dfbd7e7c2083478e6b4091ee113a3aa--breakfast-cereal-morning-breakfast.jpg
        - CIA Triad
            - Confidentiality
            - Integrity
            - Availability
        - Defense in Depth
            - Plants vs Zombies (tower defense) example
                - A single layer of defense won't cut it
                - Multiple layers is going to make it harder
- Common Attack Vectors
    - Web Apps (Front and Backend)
        - Untrusted data
        - DDOS
        - XSS
        - CSRF
    - Desktop/Dev Envs
        - Typosquatting
        - loading untrusted data
            - pickle https://www.owasp.org/images/9/9f/OWASP_MeetupTO.pdf
                import pickle
                import iobadstring = "cos\nsystem\n(S'ls -la /'\ntR."
                badfile = "./pickle.sec"
                with io.open(badfile, 'wb') as w:
                    w.write(badstring)
                obj = pickle.load(open(badfile))
                print "== Object =="
                print repr(obj)
        - Executing untrusted code
            - eval
        - unnecessary elevate privs
    - 
- Protecting yourself                                                                                                                       
    - Be aware
        - OWASP top 10
        - SANS top 25
        - python-security
    - Keep your environment clean
        - verify packages on pip and conda
        - evaluate unknown packages
    - Filter your inputs
        - Sanitize untrusted sources
    - Don't execute untrusted inputs
    
