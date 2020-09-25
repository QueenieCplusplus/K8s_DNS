# K8s_DNS

K8s DNS 架構圖




                      DNS(反查-> IP)
                       |
                 etcd (log) 
                    
                     |
                     |
                    _|____Master______                    
                   |                  |  ----- get (etcd) ------  ____ Node 1__      _____________
                   |  Core API (Auth) |  ----- list (etcd) -----  |  Kuberlet | ---- | k8s proxy | --- |  Kuberlet |
                   |__________________|                           -------------      -------------
                       |           |
                       |           |
                       |           |
                       |           
                       |       Resorces Controll (cotains Node Controller)
                       |
                       |
                       
                   Event Listener (by Scheduler)
                     

  
