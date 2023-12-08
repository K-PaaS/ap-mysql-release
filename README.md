## Related Repositories

<table>
  <tr>
    <td colspan=2 align=center>플랫폼</td>
    <td colspan=2 align=center><a href="https://github.com/K-PaaS/cp-deployment">컨테이너 플랫폼</a></td>
    <td colspan=2 align=center><a href="https://github.com/K-PaaS/sidecar-deployment">사이드카</a></td>
    <td colspan=2 align=center><a href="https://github.com/K-PaaS/ap-deployment">어플리케이션 플랫폼</a></td>
  </tr>
  <tr>
    <td colspan=2 align=center>포털</td>
    <td colspan=2 align=center><a href="https://github.com/K-PaaS/cp-portal-release">CP 포털</a></td>
    <td colspan=2 align=center>-</td>
    <td colspan=2 align=center><a href="https://github.com/K-PaaS/portal-deployment">AP 포털</a></td>
  </tr>
  <tr align=center>
    <td colspan=2 rowspan=9>Component<br>/ 서비스</td>
    <td colspan=2><a href="https://github.com/K-PaaS/cp-portal-common-api">Common API</a></td>
    <td colspan=2>-</td>
    <td colspan=2><a href="https://github.com/K-PaaS/ap-mongodb-shard-release">MongoDB</a></td>
  </tr>
  <tr align=center>
    <td colspan=2><a href="https://github.com/K-PaaS/cp-metrics-api">Metric API</a></td>
    <td colspan=2>  </td>
    <td colspan=2><a href="https://github.com/K-PaaS/ap-mysql-release">🚩 MySQL</a></td>
  </tr>
  <tr align=center>
    <td colspan=2><a href="https://github.com/K-PaaS/cp-portal-api">Portal API</a></td>
    <td colspan=2>  </td>
    <td colspan=2><a href="https://github.com/K-PaaS/ap-pipeline-release">Pipeline</a></td>
  </tr>
  <tr align=center>
    <td colspan=2><a href="https://github.com/K-PaaS/cp-portal-ui">Portal UI</a></td>
    <td colspan=2>  </td>
    <td colspan=2><a href="https://github.com/K-PaaS/ap-rabbitmq-release">RabbintMQ</a></td>
  </tr>
  <tr align=center>
    <td colspan=2><a href="https://github.com/K-PaaS/cp-portal-service-broker">Service Broker</a></td>
    <td colspan=2>  </td>
    <td colspan=2><a href="https://github.com/K-PaaS/ap-on-demand-redis-release">Redis</a></td>
  </tr>
  <tr align=center>
    <td colspan=2><a href="https://github.com/K-PaaS/cp-metrics-api">Terraman API</a></td>
    <td colspan=2>  </td>
    <td colspan=2><a href="https://github.com/K-PaaS/ap-source-control-release">SoureceControl</a></td>
  </tr>
</table>
<i>🚩 You are here.</i>

## Notice
#### 릴리즈의 경로가 https://nextcloud.paas-ta.org/ 에서 https://nextcloud.k-paas.org/ 로 변경되었습니다  




  

  


## ap-mysql-release
### Application Platform Mysql Release Configuration
  - mysql : N machine(s)   
  - ap-mysql-broker : 1 machine
  - proxy : 1 machine   

### Create Application Platform Mysql Release
  - Download the latest Application Platform Mysql Release
    ```   
    $ git clone https://github.com/K-PaaS/ap-mysql-release.git
    $ cd ap-mysql-release
  - Download & Copy "source files" into the src directory   
    ```   
    ## download source files   
    $ wget -O src.zip https://nextcloud.k-paas.org/index.php/s/QX8xRCajBX2LzGk/download

    ## unzip download source files   
    $ unzip src.zip   

    ## final src directory (2-depth)  
    src
      ├── ap-mysql-broker
      │   └── ap-mysql-broker.jar
      └── openjdk
          └── openjdk-1.8.0_45.tar.gz

      
    ```   
  - Create Application Platform Mysql Release
    ```   
    ## <VERSION> :: release version (e.g. 2.1.2)   
    ## <RELEASE_TARBALL_PATH> :: release file path (e.g. /home/ubuntu/workspace/ap-mysql-release-<VERSION>.tgz)
    $ bosh -e <bosh_name> create-release --name=ap-mysql --version=<VERSION> --tarball=<RELEASE_TARBALL_PATH> --force
    ```   
### Deployment   
- https://github.com/K-PaaS/service-deployment

## Contributors ✨

<a href="https://github.com/K-PaaS/ap-mysql-release/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=K-PaaS/ap-mysql-release" />
</a>
