# Server-side rendering with express-handlebars

Putting data into a template and send it to the client

Gives us the flexibility to create reusable templates - fb profile templates, bank account templates

Used with websites like wordpress, shopify and silverstripe

## Express-handlebars

Layout - skeleton of every page
Route template - for each kind of page(home, gallery, contact etc.)
Partials - repeatable contents (header, footer, repeated items - cart)

https://github.com/ericf/express-handlebars

## server-side rendering compared to static html

- Flexibility
Templates allow you to server a different set of data for each user
allow you to have similar but different html (home, gallery etc)
- Avoid repeating code
- Maintainability

const viewData = {
name: 'Joey',
}
res.render('home') -which template we want from the views folder
})

in .hbs
<p> my favorite otter is {{name}}</p>

each otters

# PM

Aria roles 

getByRole

const request = require('supertest')
const server = require('./server')

describe('GET /otters', () => {
test('heading contains otters', () => {
	return request(server)
		.get('/otters')
		.then((response) => {
		document.body.innerHTML = request.text
		const heading = getByRole(document, 'heading')
		console.log(document.body)
	   })
	})
})