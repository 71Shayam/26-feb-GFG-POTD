 void solve(string s, string output, int i, vector<string>&v){
	        if(i==s.length()){
	            if(output.length()>0){
	                v.push_back(output) ;
	            }
	             return ;
		    }
		    solve(s, output, i+1, v) ;
		    output.push_back(s[i]) ;
		    solve(s,output, i+1, v) ;
	    }
		vector<string> AllPossibleStrings(string s){
		    // Code here
		    string output="" ;
		    vector<string>v ;
		    int i=0 ;
		    solve(s,output,i,v) ;
		    sort(v.begin(), v.end()) ;
		    return v ;
		}
