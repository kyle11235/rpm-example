- rpm

        - guide
        
                https://www.jfrog.com/confluence/display/JFROG/RPM+Repositories

        - config

                - yum
                /etc/yum.conf
                /etc/yum.repos.d
                yum repolist

                - public -> reposync -> yum server (createrepo, yum repo baseurl=file) -> ftp/nginx/nfs -> yum client (yum repo baseurl=http://server ip)
                http://createrepo.baseurl.org/

        - test
        
                vi /etc/yum.repos.d/artifactory.repo (check artifactory.repo)
                yum install test

                curl -uadmin:xxx -XPUT http://182.92.214.141:8081/artifactory/kyle-rpm-dev-local/test -T /var/cache/yum/x86_64/7/docker-ce-stable/
