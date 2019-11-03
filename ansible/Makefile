.PHONY: build check clean destroy provision up update

build: update up provision

check:
	vagrant validate

clean:
	rm provisioning.retry *.log

destroy:
	vagrant destroy -f

provision:
	vagrant ssh ansible \
		-c 'ansible-playbook /vagrant/provisioning.yml -i /vagrant/hosts'

up:
	vagrant up

update:
	vagrant box update
