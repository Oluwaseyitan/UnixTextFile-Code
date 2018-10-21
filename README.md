# UnixTextFile-Code

#Download files from URL
 wget -i "http://129.120.58.147/INFO5502fall2018/class/Group1/2009/"
 
cat A_Hybrid_Approach_to_Undergraduate_LIS_Instruction_A_Case_Study_of_Organization_of_Online_Course_Information.txt|tr -c '[:alpha:]' '[\n*]' | sort | uniq -c | sort -n -r>Hybrid.txt

cat Hybrid.txt|tr -c "a-zA-Z" " " |tr "A-Z" "a-z"|tr " " "\n" >Hybrid.txt

tr -s '[:blank:]' '\n' <Hybrid.txt| fgrep -vwf stopwords.txt

cat Hybrid.txt|tr -c '[:alpha:]' '[\n*]' | sort | uniq -c | sort -n -r>Hybrid.txt
