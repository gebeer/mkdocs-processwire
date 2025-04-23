Provides an interface to the Pages class but specific to a given page class/type, with predefined parent and template.
----------------------------------------------------------------------------------------------------------------------

This class is primarily used by the core as an alternative to `$pages`, providing an API for other Page types like [`User`](/api/ref/user/), [`Role`](/api/ref/role/), [`Permission`](/api/ref/permission/), and `Language`. The [`$users`](/api/ref/users/), [`$roles`](/api/ref/roles/), [`$permissions`](/api/ref/permissions/) and [`$languages`](/api/ref/languages/) API variables are all instances of [`PagesType`](/api/ref/pages-type/). This class is typically not instantiated on its own and instead acts as a base class which is extended.

