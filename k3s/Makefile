default: vagrant provision

console:
	ansible-console --inventory inventory.yml

provision:
	ansible-playbook site.yml --inventory inventory.yml
	kubectl config set-context k3s-virtualbox

vagrant:
	vagrant up

destroy:
	vagrant destroy --force
	# rm -rf .vagrant*
	kubectl config delete-context k3s-virtualbox
	kubectl config delete-cluster k3s-virtualbox
	kubectl config delete-user k3s-virtualbox