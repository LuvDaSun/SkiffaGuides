# SkiffaGuides
## **👩🏻‍💻 User Persona**

**Name**: Klara

**Role**: Product Manager

**Goal**: Help her team integrate **OpenID authentication** into the product’s **web login** using industry-standard APIs.

**Challenge**: She doesn’t write code daily but understands workflows and how tech supports business goals.

**Motivation**: She wants to speed up implementation, ensure interoperability with other systems, and provide clear documentation to developers. **(Explain why she wants to speed up implementation and give more context.)**

- The Whys?
    - Why does she want to speed up the implementation?
        - May slows down value delivery to users
        - Risks of falling behind competitors who already offer smooth, secure login experiences
        - Adds to engineering overhead and potential bugs (if code is rushed without standardization)
    - Why does clear documentation matter?
        - **Avoid**
            - New devs joined and got lost in undocumented APIs
            - A small login change took 3x longer because nobody knew what a certain endpoint did
            - Clients or partners asked, “Do you have docs for this API?” and got silence in return
        - With **OpenAPI + Skiffa**, she can:
            - Create a source of truth for the API
            - Auto-generate docs, saving manual writing
            - Provide a clear way for internal teams or external partners to **“try out”** the API before building
- Using standards like **OpenID** + tools like **OpenAPI & Skiffa** helps ensure:
    
    > Smooth communication across systems, now and in the future.
    > 

---

### Steps:

1. **Define the goal**
    1. Product needs a secure login.
2. **Work with Devs to outline APIs, write an OpenAPI Document.**
    1. Using YAML or JSON (OpenAPI format).
3. **Introduce Skiffa to the Team**
    1. How Skiffa can 
        - Take the API spec (OpenAPI)
        - Generate useful code: client libraries, server templates, and docs
        - Save hours of manual setup time
4. **Use Skiffa CLI ( I brainstormed with ChatGPT)**
    
    ```bash
    skiffa generate --input ./login-api.yaml --output ./generated
    ```
    
    - After installing (not sure if this is the rughg
        - Reads the OpenAPI file
        - Generates SDKs (code libraries) in different languages
        - Creates server-side stubs (API skeletons)
        - Builds documentation
5. **Customize the generated code**
    - Add real authentication logic (what’s the definition of real authentication?)
    - Plug into your existing user database or identity provider
6. **API Testing**
    - Using an OpenAPI document as an input
    - For example:
        - Security tools test the API footprint for weakness spots in the implementation.
7. **Optional: Build a Dev Portal.**
