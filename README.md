# Svelte Kit Scaffold

SvelteKitScaffold is a CLI that generates CRUDs that talks to APIs

## Usage

`svelte-kit-scaffold g [resource]`


## Example
`svelte-kit-scaffold g users name:string email:string`

Will generate:

### List / Index
* `routes/users/+page.svelte` listing all users in a table with the fields described above
* `routes/users/+page.js` fetch all users from an API endpoint

### Create
* `routes/new/+page.svelte` form to create users with the fields above
* `routes/new/+page.server.svelte` send json with the fields above