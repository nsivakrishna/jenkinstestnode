node
{
checkout scm
sh "ls -ltr"
	script{
	env.awscliversion = "awscli==1.18.147"
	}

stage("awscli-test")	
{
        sh '''
	    
           if [[ $(/usr/bin/pip freeze | grep awscli)  = ${env.awscliversion} ]]; then

              echo "==Expected version standard-slv aws version  $(/usr/bin/pip freeze | grep awscli) and install version same==="

            else
        
                echo  "????????????? not expected standard-slv aws version $(/usr/bin/pip freeze | grep awscli) ?????????????"
            fi
          
       '''
}
