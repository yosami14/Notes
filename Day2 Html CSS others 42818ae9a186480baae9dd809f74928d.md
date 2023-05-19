# Day2 Html/CSS/others

<h1> the heading tag 2,3,4

<p> paragraph

<a> anchor tag used to link 

<div> used to provide the different section

<img> used to provide image

<br> break 

<strong> Used to show the font Stronger

<b> bold

<i> itailc

<ul> used to define lists

<li> unordered list 

<ol> ordered list

CSS

```html
<!DOCTYPE html>
<html>
<head>
  <title>CSS Properties Example</title>
</head>
<body>
  <h1>Example Page</h1>
  <p>This is an example paragraph with some CSS properties applied to it.</p>
  <div class="highlight">Highlighted Text</div>
  <div class="box">Box with borders and padding</div>
  <div class="box shadow">Box with Shadow</div>
</body>
</html>
```

```html

    /* CSS properties */
    body {
      background-color: lightblue;
    }
    
    h1 {
      color: darkred;
      text-align: center;
    }
    
    p {
      font-family: Arial, sans-serif;
      font-size: 16px;
      line-height: 1.5;
    }
    
    .highlight {
      background-color: yellow;
      padding: 10px;
    }
 .shadow {
      box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.4);
   
```

### Difference between CSS and SCSS

CSS (Cascading Style Sheets) and SCSS (Sassy CSS) are both style sheet languages used for styling web pages. The main difference between CSS and SCSS lies in their syntax and capabilities.

CSS is the standard styling language for the web. It uses a simple syntax with a set of predefined properties and values to apply styles to HTML elements. CSS files have a .css extension.

On the other hand, SCSS is a superset of CSS, meaning that all valid CSS code is also valid SCSS code. SCSS introduces additional features and enhancements to the CSS syntax, making it more powerful and flexible. SCSS files have a .scss extension.

The key feature of SCSS is its support for variables, nesting, and mixins. Variables allow you to define reusable values, making it easier to maintain and update styles. Nesting lets you nest selectors inside one another, improving readability and reducing repetition. Mixins are reusable code snippets that can be included in multiple styles, promoting code reusability.

To use SCSS, it needs to be compiled into regular CSS code, which can be done using a preprocessor or build tools. The resulting CSS can then be used in web pages like regular CSS.

In summary, while CSS is the standard styling language, SCSS is an extension of CSS with additional features and a more advanced syntax, including variables, nesting, and mixins, which can enhance the maintainability and reusability of styles.

### How does transistors work in computer (Whats the function)

Transistors are crucial components in computers that amplify and switch electrical signals. Made from semiconductor materials like silicon, transistors control the flow of current. They play a fundamental role in digital circuits by serving as building blocks for logic gates. These gates combine multiple transistors to perform logical operations, enabling computers to process information and make decisions.

In addition to signal amplification and logic operations, transistors are integral to computer memory. They facilitate data storage and retrieval by storing electrical charges in capacitors, as seen in Dynamic Random Access Memory (DRAM) chips. Moreover, transistors are essential in microprocessors—the heart of a computer. With millions or billions of transistors working together, microprocessors execute instructions, perform calculations, and govern overall computer operations.

In summary, transistors in computers serve three key functions: amplifying and switching signals, enabling logical operations in digital circuits, and contributing to memory storage and microprocessor functionality. These tiny electronic components are foundational to the operation and capabilities of modern computers.

### Css Selector

CSS selectors are patterns used to select and target specific HTML elements on a web page for styling or applying specific behaviors. They allow you to specify which elements should be affected by CSS rules. Here are some commonly used CSS selectors:

1. Element Selector: Targets elements based on their HTML tag name. For example, `p` selects all `<p>` elements.
2. Class Selector: Targets elements with a specific class attribute. It is denoted by a dot (.) followed by the class name. For example, `.my-class` selects all elements with the class "my-class".
3. ID Selector: Targets a specific element with a unique ID attribute. It is denoted by a hash (#) followed by the ID name. For example, `#my-id` selects the element with the ID "my-id".
4. Attribute Selector: Targets elements based on specific attribute values. It is denoted by square brackets ([]). For example, `[type="submit"]` selects all elements with the attribute `type` set to "submit".
5. Descendant Selector: Targets elements that are descendants of another element. It uses a space between two selectors. For example, `div p` selects all `<p>` elements that are inside a `<div>`.
6. Child Selector: Targets elements that are direct children of another element. It uses the greater-than symbol (>). For example, `ul > li` selects all `<li>` elements that are immediate children of a `<ul>`.
7. Adjacent Sibling Selector: Targets elements that are immediately next to another element. It uses the plus symbol (+). For example, `h2 + p` selects the `<p>` element that immediately follows an `<h2>`.
8. Pseudo-classes: Targets elements based on a specific state or condition. For example, `:hover` selects an element when the mouse is hovered over it.

These are just a few examples of CSS selectors. CSS offers a wide range of selectors that allow you to precisely target and style elements on a web page based on various criteria.

### **Whats CDN**

CDN stands for Content Delivery Network. It is a distributed network of servers located in different geographic locations worldwide. The primary purpose of a CDN is to deliver web content, such as images, videos, scripts, and other static or dynamic files, to end users more efficiently and quickly.

When a user requests a resource from a website, the CDN determines the server closest to the user's location and delivers the content from that server. This proximity reduces the distance the data needs to travel, minimizing latency and improving the overall performance of the website.

CDNs offer several benefits:

1. Improved Website Performance: By serving content from servers closer to users, CDNs reduce latency and enable faster content delivery. This results in improved page load times and a better user experience.
2. Scalability: CDNs can handle high volumes of traffic and distribute the load across multiple servers. This scalability helps websites handle increased traffic without overloading their origin server.
3. Global Reach: CDNs have servers distributed worldwide, allowing content to be delivered quickly to users regardless of their geographic location. This global presence ensures consistent performance for users across different regions.
4. Load Balancing: CDNs balance traffic across multiple servers, optimizing resource utilization and preventing any single server from becoming overwhelmed. Load balancing helps maintain high availability and reduces the risk of server downtime.
5. Caching: CDNs cache content at edge servers, storing copies of frequently accessed resources closer to users. Caching reduces the load on the origin server and speeds up subsequent requests for the same content.
6. DDoS Mitigation: Some CDNs offer protection against Distributed Denial of Service (DDoS) attacks. They have built-in security measures and can absorb and mitigate traffic spikes, protecting websites from malicious attacks.

CDNs are widely used by websites and online services to improve performance, scalability, and reliability. By leveraging a CDN's network infrastructure, websites can deliver content faster and more efficiently to users, resulting in an enhanced browsing experience.