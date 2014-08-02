### Ansible SMS notification example using plivo

Sample ansible project to send SMS notification using [Plivo](https://www.plivo.com). Plivo is a [newly proposed](https://github.com/ansible/ansible/pull/8408) notification module for Ansible 1.7.

#### Prerequisites:

1. Ansible: Install [this fork of ansible](https://github.com/rohit01/ansible), till the module is merged upstream.
2. Plivo API credentials: Login to your [Plivo](https://www.plivo.com) account and find it in the dashboard. If you dont have a Plivo account, register for a free trial.

#### The 3 Baby Steps:

1. Clone this repository & cd into the repository:

    `$ git clone git@github.com:rohit01/ansible-plivo-example.git`  
    `$ cd ansible-plivo-example/`

2. Update ansible variables in file: [roles/plivo_example/vars/main.yml](roles/plivo_example/vars/main.yml)

    * contact_number: Phone number of person to be notified
    * plivo_number: A valid phone number in your Plivo account. If you have custom sender-id enabled, this can be any phone number.
    * plivo_auth_id: Login to your plivo account and find - AUTH_ID
    * plivo_auth_token: Login to your plivo account and find - AUTH_TOKEN

3. Run the examples using the following command:

    `$ ansible-playbook -v -i ansible_hosts site.yml`

---

**Note:** [Plivo](https://www.plivo.com) services are not free. The examples will send few real SMS and you may be charged for the same.

