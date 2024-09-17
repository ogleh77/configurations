__Persistant volume__

- Persistant volume
- Persistant claim
- storage class

__NOTE__ Madama aaad ogayn nodeka uu podkagu ka restart garaysmi doono waaxa fiican inaad persistance volume kaagu yaalo meel all nodes kan share it sidoo klae waa inuu ahaado meel lagu kalsonan karo xtaa hdii clusterka dhamantii oo dhan crush groobo

Cloud storage kastaa wuxuuu leyhy persisatnce volume u gaara saaso ay tahay Stroage class name 
__hostpath__ wuxuu shegayaa 



```yml
apiVersion: v1
kind: PersistentVolume
metadata:
  name: postgres-pv
  labels:
    type: local
spec:
  storageClassName: hostpath
  capacity:
    storage: 1Gi
  accessModes:
    - ReadWriteOnce
  hostPath:
    path: "/mnt/data"

```