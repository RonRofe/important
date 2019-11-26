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

## List Of Useful Packages

- **yargs:** Communication with the Terminal.
- **chalk:** Styling Terminal output.
- **nodemon:** Run files on document save.
- **mongodb:** Communicate with MongoDB databases.
- **mongoose:** Expended package of mongodb for communicating MongoDB with models.
- **express:** Running web server.
- **jsonwebtoken:** Generating JWT and use it.
- **validator:** Validating data format.
- **bcryptjs:** Encrypt and decrypt data.
- **multer:** Uploading files.
- **sharp:** Cut and modify images.
- **jest:** Test javascript codes.
- **supertest:** Test HTTP requests.
- **env-cmd:** Using local env file from env variables.
- **request:** Send HTTP requests from the server.
- **socket.io**: Using web-sockets for real-time event-based communication with the server.