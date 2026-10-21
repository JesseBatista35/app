oc get pods -n sigsj-des -l name=sigsj-alvara-des
oc describe pod sigsj-alvara-des-693-gnfhp -n sigsj-des        # Restart Count, Last State, Exit Code, probes falhando
oc logs sigsj-alvara-des-693-gnfhp -c sigsj-alvara-des -n sigsj-des --previous
oc get events -n sigsj-des --sort-by=.lastTimestamp | grep -i alvara
