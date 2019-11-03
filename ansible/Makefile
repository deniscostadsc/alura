.PHONY: check clean up provision

check:
	vagrant validate

clean:
	vagrant destroy -f
	rm provisioning.retry *.log

up:
	vagrant box update
	vagrant up

provision:
	vagrant ssh ansible \
		-c 'ansible-playbook /vagrant/provisioning.yml -i /vagrant/hosts --private-key ~/.ssh/id_ed25519'
