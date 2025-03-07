==========================================================
How to track your website traffic from your Odoo Dashboard
==========================================================

.. warning::
  It is not possible anymore for new Google Analytics accounts to integrate
  their **Google Analytics Dashboard** inside their **Odoo Dashboard**.
  Google deprecated **Universal Analytics** which won't be supported anymore in
  `July 2023 <https://support.google.com/analytics/answer/11583528>`_. They are
  replacing it with **Analytics 4**. New accounts are already using it.

  **Analytics 4** `doesn't allow <https://issuetracker.google.com/issues/233738709?pli=1>`_
  its dashboard to be integrated in external websites.

  You now have to check your Analytics data directly in the Google Platform as
  it won't be possible in Odoo anymore.

  Accounts created before `October 2020 <https://support.google.com/analytics/answer/11583832>`_
  should still be using **Universal Analytics** and be able to integrate their
  dashboard on external website until the official end of support `around mid
  2023 <https://developers.googleblog.com/2022/03/gis-jsweb-authz-migration.html>`_.

You can follow your traffic statistics straight from your Odoo Website
Dashboard thanks to Google Analytics.

- A preliminary step is creating a Google Analytics account and entering the
  tracking ID in your Website's settings (see :doc:`google_analytics`).

- Go to `Google APIs platform <https://console.developers.google.com>`__
  to generate Analytics API credentials. Log in with your Google account.

- Select Analytics API.

.. image:: google_analytics_dashboard/google_analytics_api.png
    :align: center

- Create a new project and give it a name (e.g. Odoo).
  This project is needed to store your API credentials.

.. image:: google_analytics_dashboard/google_analytics_create_project.png
    :align: center

- Enable the API.

.. image:: google_analytics_dashboard/google_analytics_enable.png
    :align: center

- Create credentials to use in Odoo.

.. image:: google_analytics_dashboard/google_analytics_create_credentials.png
    :align: center

- Select *Web browser (Javascript)*
  as calling source and *User data* as kind of data.

.. image:: google_analytics_dashboard/google_analytics_get_credentials.png
    :align: center

- Then you can create a Client ID.
  Enter the name of the application (e.g. Odoo) and the allowed pages on
  which you will be redirected. The *Authorized JavaScript origin* is your
  Odoo's instance URL. The *Authorized redirect URI* is your Odoo's instance
  URL followed by '/google_account/authentication'.

.. image:: google_analytics_dashboard/google_analytics_authorization.png
    :align: center


- Go through the Consent Screen step by entering a product name
  (e.g. Google Analytics in Odoo). Feel free to check the customizations options
  but this is not mandatory. The Consent Screen will only show up when you enter
  the Client ID in Odoo for the first time.

- Finally you are provided with your Client ID. Copy and paste it in Odoo.

.. image:: google_analytics_dashboard/google_analytics_client_id.png
    :align: center

- Open your Website Dashboard in Odoo and link your Analytics account to past
  your Client ID.

.. image:: google_analytics_dashboard/google_analytics_start.png
    :align: center

- As a last step, authorize Odoo to access Google API.

.. image:: google_analytics_dashboard/google_analytics_login.png
    :align: center
