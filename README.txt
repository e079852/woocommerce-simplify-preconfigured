This is an installation of WooCommerce with the Simplify plugin that has been preconfigured with a test product to run "out of the box." There are two versions of the installation: WooCommerceDocker-PROD will send transactions to the Production environment at www.simplify.com, while WooCommerceDocker-UAT will send transactions to the UAT environment at uat.simplify.com. The only configuration needed is to add the appropriate API keys. To do so follow the instruction below:

WooCommerce version 3.4.4
Simplify Commerce version 1.4.2

Username: simplify
Password: Password1

To bring up the docker image and configure the API keys:
(NB the following line should be in your hosts file: 127.0.0.1	localhost alphalaundryservices.store.uat.simplify.com)

1. Run docker-compose up
2. In a browser, go to the dashboard at http://localhost/wp-admin/
3. In the left-hand pane, click on Plugins/InstalledPlugins
4. In the list of installed plugsins click on Simplify Commerce Payment Gateway for WooCommerce/Settings
5. For Sandbox, click on the "Enable Sandbox Mode" checkbox and add your Sandbox Public and Private keys. For Live payments, ensure that "Enable Sandbox Mode" is not checked and add your Live Public and Private keys.
6. Click on the "Save Changes" button.
7. On the main Dashboard menu click on "Visit Store" (http://localhost/?post_type=product) to run transactions.

NB. In the UAT environment, the currency configured in your WooCommerce store must match the currency of the onboarded merchant at Simplify.com
