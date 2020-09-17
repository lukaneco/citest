# citest
Test for CI

python3 -m pip install -r .\requirements.txt
python3 .\server.py
python3 -m py.test mitest.py



travis login --org
travis encrypt-file deploy_rsa --add
git add deploy_rsa.enc .travis.yml
ssh-copy-id -i deploy_rsa.pub ezequieljsosa@34.75.155.110 ## ssh-copy-id -i deploy_rsa.pub lucasain2010@34.82.12.150
rm deploy_rsa deploy_rsa.pub
git commit -m "Add private key"
git push
