# algor
// só como números naturais
function ehPrimo(n){
    if(n<2) return 'n'
    if(n == 2) return 's'
    let d = n-1
    while(d>=2){
        if(n%d==0) return 'n'
        d--
    }
    return 's'
}

// verifica com números inteiros
function ehPrimo2(n){
    if(isNaN(n)) return 'informe um número'
    if(n >= -1 && n <= 1) return 'não'
    let d=[1,-1,n,n*(-1)]
	let nt = n < 0 ? n*(-1): n
    let nm = nt
    while(nm > 1){
        let m = nt%nm
        if(m == 0){
            let res = false
            for(let i=0;i<d.length;i++){
                if(nm == d[i]){ 
                    res = true
                    break
                }
            }
            if(!res) return 'não'
        }	
     nm--
    }
    return 'sim'
}
