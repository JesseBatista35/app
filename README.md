   oc get pod -n sispi-des -l name=sispi-med-gestao-des --show-labels


      oc get pods -n sispi-des -L maistra.io/expose-route | grep -v Completed
