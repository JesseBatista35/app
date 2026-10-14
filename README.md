apiVersion: cert-manager.io/v1
kind: Certificate
metadata:
  annotations:
    kubectl.kubernetes.io/last-applied-configuration: >
      {"apiVersion":"cert-manager.io/v1","kind":"Certificate","metadata":{"annotations":{},"labels":{"app.kubernetes.io/instance":"sipgs-backend-bff-simulacao-des"},"name":"sipgs-backend-bff-simulacao-des-internal-srv0-cert","namespace":"istio-ingress"},"spec":{"dnsNames":["sipgs-backend-bff-simulacao.apl.des.private.aws"],"duration":"4320h","issuerRef":{"group":"awspca.cert-manager.io","kind":"AWSPCAClusterIssuer","name":"aws-privateca-cluster-issuer"},"renewBefore":"360h","secretName":"sipgs-backend-bff-simulacao-des-nprd","usages":["digital
      signature","key encipherment","server auth"]}}
  creationTimestamp: '2026-10-13T16:50:25Z'
  generation: 1
  labels:
    app.kubernetes.io/instance: sipgs-backend-bff-simulacao-des
  name: sipgs-backend-bff-simulacao-des-internal-srv0-cert
  namespace: istio-ingress
  resourceVersion: '60888920'
  uid: 6cfcac4d-28cf-4064-9469-3c8f762c4feb
spec:
  dnsNames:
    - sipgs-backend-bff-simulacao.apl.des.private.aws
  duration: 4320h
  issuerRef:
    group: awspca.cert-manager.io
    kind: AWSPCAClusterIssuer
    name: aws-privateca-cluster-issuer
  renewBefore: 360h
  secretName: sipgs-backend-bff-simulacao-des-nprd
  usages:
    - digital signature
    - key encipherment
    - server auth
status:
  conditions:
    - lastTransitionTime: '2026-10-13T16:50:25Z'
      message: Issuing certificate as Secret does not exist
      observedGeneration: 1
      reason: DoesNotExist
      status: 'False'
      type: Ready
    - lastTransitionTime: '2026-10-14T07:50:25Z'
      message: >-
        The certificate request has failed to complete and will be retried:
        failed to request certificate from PCA: operation error ACM PCA:
        DescribeCertificateAuthority, https response error StatusCode: 400,
        RequestID: 3732aceb-ae00-4c31-bab4-4738d8e5e40e, api error
        AccessDeniedException: User:
        arn:aws:sts::013644998398:assumed-role/aws-privateca-issuer-role-nprd/1791935425255176512
        is not authorized to perform: acm-pca:DescribeCertificateAuthority on
        resource:
        arn:aws:acm-pca:sa-east-1:143495498779:certificate-authority/bb63571e-8894-4f66-9ef8-f701059bcde0
        because no resource-based policy allows the
        acm-pca:DescribeCertificateAuthority action
      observedGeneration: 1
      reason: Failed
      status: 'False'
      type: Issuing
  failedIssuanceAttempts: 5
  lastFailureTime: '2026-10-14T07:50:25Z'
