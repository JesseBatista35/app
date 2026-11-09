Paulo, desculpa, aquela REQ foi uma referência que passaram numa reunião e não confirmei se ainda estava acessível. Vou pegar com o Evandro um modelo atual (a do VIP que está sendo aberta para o SIGSJ) e te repasso.

Sobre o VIP: dá para apontar o DNS direto para o IP da VM, mas aí a URL fica só em HTTP. O Apache da VM da esteira atende na porta 80 sem certificado; o HTTPS é feito no VIP, onde o certificado é instalado. Além disso, a VM é criada pelo Terraform, então, se ela for recriada, o IP muda e o DNS precisa ser refeito; com o VIP isso não acontece.

Se para vocês HTTP sem certificado atende, o DNS direto resolve. Se precisar de HTTPS, o caminho é o VIP. Vou confirmar com o Evandro se, para esse caso, ele aceita o DNS direto ou se o padrão é sempre VIP.
