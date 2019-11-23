# Important things // NODE.JS

## Express JS

### Response Headers To Permit Access For External Servers
- Choose domains to permit access to: `res.setHeader('Access-Control-Allow-Origin', 'DOMAIN_NAME')`  
**DOMAIN_NAME**: URL or * For all domains
- Choose headers to accept besides the default browser's headers: `res.setHeader('Access-Control-Allow-Headers', 'HEADERS')`  
**HEADERS**: List of headers names
- Restrict methods to accept: `res.setHeader('Access-Control-Allow-Methodds', 'METHODS')`
**METHODS**: Names of methods to accept

**Example:**
```js
const app = express();

app.use((req, res, next) => {
    res.setHeader('Access-Control-Allow-Origin', '*');
    res.setHeader(
        'Access-Control-Allow-Headers',
        'Origin, X-Requested-With, Content-Type, Accept'
    );
    res.setHeader(
        'Access-Control-Allow-Methods',
        'GET, POST, PATCH, DELETE, OPTIONS'
    );
    next();
})
```