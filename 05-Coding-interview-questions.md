Input:  txt[] = "THIS IS A TEST TEXT"
        pat[] = "TEST"
Output: Pattern found at index 10

Input:  txt[] =  "AABAACAADAABAABA"
        pat[] =  "AABA"
Output: Pattern found at index 0
        Pattern found at index 9
        Pattern found at index 12
        
        
  function search(txt, pat) 
    { 
        let M = pat.length(); 
        let N = txt.length(); 
  
        /* A loop to slide pat one by one */
        for (let i = 0; i <= N - M; i++) { 
  
            int j; 
  
            /* For current index i, check for pattern  
              match */
            for (let j = 0; j < M; j++) 
                if (txt.charAt(i + j) != pat.charAt(j)) 
                    break; 
  
            if (j == M) // if pat[0...M-1] = txt[i, i+1, ...i+M-1] 
                System.out.println("Pattern found at index " + i); 
        } 
    } 
  
    fucntion main() { 
        String txt = "AABAACAADAABAAABAA"; 
        String pat = "AABA"; 
        search(txt, pat); 
    }        
        
