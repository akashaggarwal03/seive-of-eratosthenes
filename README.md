# seive-of-eratosthenes
to calculate primes upto n

void SieveOfEratosthenes(int n) 
{ 
    
    memset(prime, true, sizeof(prime)); 
  
    for (int p=2; p*p<=n; p++) 
    { 
       
        if (prime[p] == true) 
        { 
            // Update all multiples of p 
            for (int i=p*2; i<=n; i += p) 
                prime[i] = false; 
        } 
    } 
   
    for (int p=2; p<=n; p++) 
       if (prime[p]) 
          cout << p << " "; 
} 
