properties([parameters([string(defaultValue: 'awscli==1.18.147', description: '', name: 'awscliversion', trim: false)])])

string awsversionsr = '$(/usr/bin/pip freeze | grep awscli)'

node
{
        sh '''
	         
           if [[ $(/usr/bin/pip freeze | grep awscli)  = ${awscliversion} ]]; then

              echo "==Expected version standard-slv aws version  $(/usr/bin/pip freeze | grep awscli) and install version same==="

            else
        
                echo  "????????????? not expected standard-slv aws version $(/usr/bin/pip freeze | grep awscli) ?????????????"
            fi
          
       '''
}
