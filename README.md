# Svelte Kit Scaffold

SvelteKitScaffold is a CLI that generates CRUDs that talks to APIs

## Usage

`svelte-kit-scaffold g [resource] [field:type] [field:type] ...`

## Example
`svelte-kit-scaffold g users name:string email:string`

Will generate:

### A table containing the resources
* `routes/users/+page.svelte` listing all users in a table with the fields described above
* `routes/users/+page.js` fetch all users from an API endpoint

### Delete
- as part of the list above will be a delete button that sends a DELETE request to the API and removes that row on the client side as well so there is no need for a refresh

### Create
* `routes/new/+page.svelte` form to create users with the fields above
* `routes/new/+page.server.svelte` send json with the fields above

### Edit
* `routes/users/[id]/+page.svelte` form to edit an user
* `routes/users[id]/+page.server.svelte` send UPDATE request to the API
