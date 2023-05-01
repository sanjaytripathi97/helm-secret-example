# helm-secret-example

#helm plugin install https://github.com/zendesk/helm-secrets

#gpg --gen-key

provide passpharse as well if you want

copy the fingerprint from the above command 
helm secret will also provide us the SOPS


#sops -p <fingerprint> secrets.yaml

<delete all the data >

and put the below line 

password: secret1234

#helm secrets view secrets.yaml    (it will ask passpharse)

if you get the error then try below

GPG_TTY=$(tty)
export GPG_TTY

#helm secrets view secrets.yaml


#helm secrets install app ./app -n default -f ./secrets.yaml
#helm ls

