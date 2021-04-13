# EJS Partials
Partials come in handy when you want to reuse the same HTML across multiple views. Think of partials as functions, they make large websites easier to maintain as you don’t have to go and change a piece of text in every page it appears in. Instead, you define that reusable bundle of code in a file andinclude it wherever you need it.


# Example
you can create footer.ejs and header.js just like :


```
// HEADER 
  <div class="header clearfix">
      <nav>
          <ul class="nav nav-pills pull-right">
              <li role="presentation"><a href="/">Home</a></li>
          </ul>
          <h3 class="text-muted">Node.js Blog</h3>
      </nav>
  </div>
//footer
<!-- views/partials/footer.ejs -->
    <footer class="footer">
        <p>© 90210 Lawyer Stuff.</p>
    </footer>
 ```



