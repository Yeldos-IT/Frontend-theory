# CSS (Cascading Style Sheets) Theory

CSS is used to style and layout HTML documents, enabling control over the presentation of web pages. Below is a comprehensive theory covering the CSS section from the roadmap.

---

## **1. CSS Basics**

### **Connecting CSS to HTML:**
- **External file:** Linked via `<link>` in the `<head>` of the HTML document:
  ```html
  <link rel="stylesheet" href="styles.css">
  ```
- **Internal styles:** Defined inside a `<style>` tag in the `<head>`:
  ```html
  <style>
    body { background-color: lightblue; }
  </style>
  ```
- **Inline styles:** Applied directly to an HTML element using the `style` attribute:
  ```html
  <div style="color: red;">Text</div>
  ```

### **Selectors:**
- **Element selector:** Targets all elements of a type: `p { color: blue; }`
- **Class selector:** Targets elements with a specific class: `.box { margin: 10px; }`
- **ID selector:** Targets a single element with a unique ID: `#header { text-align: center; }`
- **Attribute selector:** Targets elements with specific attributes: `[type="text"] { border: 1px solid; }`
- **Pseudo-classes:** Add special styles to elements in specific states: `a:hover { color: green; }`
- **Pseudo-elements:** Style parts of an element: `::before`, `::after`.

### **CSS Properties:**
- **Colors:** `color`, `background-color`
- **Box Model:** `width`, `height`, `padding`, `margin`, `border`
- **Typography:** `font-family`, `font-size`, `font-weight`
- **Borders:** `border`, `border-radius`

---

## **2. Key Concepts**

### **Box Model:**
Defines how elements are structured:
- **Content:** The actual content inside the box.
- **Padding:** Space between the content and the border.
- **Border:** The boundary around the padding.
- **Margin:** Space outside the border.

### **Cascade, Inheritance, and Specificity:**
- **Cascade:** Rules with higher specificity override less specific ones.
- **Inheritance:** Some properties (e.g., `color`, `font-family`) are inherited by child elements.
- **Specificity:** Inline styles > IDs > Classes > Elements.

---

## **3. Modern Layout Techniques**

### **Flexbox:**
A layout model for flexible alignment and distribution of items:
```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

### **Grid:**
A powerful system for creating complex, responsive layouts:
```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
}
```

---

## **4. Advanced Topics**

### **Media Queries:**
Enable responsive design by applying styles based on screen size:
```css
@media (max-width: 600px) {
  body { font-size: 14px; }
}
```

### **Animations:**
Adding transitions and animations to elements:
- **Transitions:**
  ```css
  div { transition: all 0.3s; }
  div:hover { transform: scale(1.2); }
  ```
- **Keyframes:**
  ```css
  @keyframes example {
    from { background-color: red; }
    to { background-color: yellow; }
  }
  div { animation: example 2s infinite; }
  ```

### **CSS Variables:**
Reusable custom properties:
```css
:root { --main-color: #ff5733; }
body { color: var(--main-color); }
```
