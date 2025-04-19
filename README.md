## 👋 Hi there, I'm Kevin  

Welcome to my GitHub! I'm a developer who enjoys building dynamic web applications using the ASP.NET MVC framework. 

Below are some of my featured projects that showcase both functionality and visual design.

---

## 🚀 Featured Projects

### 📚 [Kevin_MVC](https://github.com/asde9875/Kevin_MVC)  
A full‑stack ASP .NET Core MVC bookstore demo combining a playful front‑end with a robust admin console and complete shopping workflow. Key highlights include:

🧑‍💼**User Experience**  
> -  Dynamic starry background via Particles.js with custom GIF branding  
> -  Full‑width banner carousel for promotions (Stripe deals, new arrivals, editor’s picks)  
> -  “Ways to save and explore books” icon carousel styled like Amazon with arrow controls  
> -  Responsive product grid: six‑column layout, hover zoom/shadow, discount ribbons, and split‑screen ad banners every 12 items  
> -  AJAX‑powered shopping cart badge and live cart count  
> -  Product Details page with quantity selector, role‑based add‑to‑cart, and real‑time price tiers

🔧 **Admin Console (Authenticated Roles)**  
> - **Category Management**: DataTables-powered table with pagination, search, “Create New Category” button, inline Edit/Delete actions (modal dialogs + SweetAlert2 delete confirmations).  
> -  **Product Management**: DataTables CRUD list with warnings for incomplete uploads, create/edit/delete controls, and SweetAlert2 confirmation. Create/Edit pages feature TinyMCE rich-text editor for descriptions, input fields for Title, ISBN, Author, List Price and tiered pricing, Category dropdown, Cover Image & multiple Product Images uploads with file‑upload validation.  
> -  **User Management & Registration**: Admin portal “Register” page to create new accounts with email, name, contact, address fields, and role selection. User List table with Name, Email, Phone, Company, Role columns and Unlock/Permission actions.  
> -  **Order Management**: Filterable order list with status tabs and API endpoints; Order Details view showing pickup info and order summary; buttons for Start Processing, Ship Order, Cancel Order; Stripe Checkout integration with delayed vs. immediate payment, plus refund processing and real-time status updates.

🔑 **Under the Hood**  
> - Architecture: ASP .NET Core MVC, Entity Framework Core, repository & service layer patterns  
> - Front‑end: Bootstrap 5, jQuery, DataTables, Particles.js, SweetAlert2, Toastr.js, TinyMCE, FontAwesome  
> - Authentication/Authorization: ASP .NET Identity roles, Google reCAPTCHA v3 on admin register  
> - Payments: Stripe Checkout Sessions with delayed vs. immediate capture  
> - Dependency Injection for clean code separation and testability  

### 📂 Solution Structure  
Below is the project folder organization for Kevin_MVC:  

``` 
Kevin.sln
├─ Kevin.DataAccess
│  ├─ DAO
│  ├─ Data
│  └─ Migrations
├─ Kevin.Models
│  └─ Entities
├─ Kevin.Utility
├─ KevinWeb
│  ├─ Controllers
│  ├─ Services
│  ├─ Views
│  │  ├─ Cart
│  │  ├─ Category
│  │  ├─ Company
│  │  ├─ Home
│  │  ├─ Order
│  │  ├─ Product
│  │  └─ User
│  ├─ wwwroot
│  ├─ Program.cs
│  └─ appsettings.json
└─ README.md
```  

### 🧩 Dependency Injection Setup
All repository (DAO) and service layers are registered in `Program.cs`:  

```csharp
// Data Access (DAO)
builder.Services.AddScoped<ICategoryDao, CategoryDao>();
builder.Services.AddScoped<IProductDao, ProductDao>();
builder.Services.AddScoped<ICompanyDao, CompanyDao>();
builder.Services.AddScoped<IShoppingCartDao, ShoppingCartDao>();
builder.Services.AddScoped<IApplicationUserDao, ApplicationUserDao>();

// Business Services
builder.Services.AddScoped<ICategoryService, CategoryService>();
builder.Services.AddScoped<IProductService, ProductService>();
builder.Services.AddScoped<ICompanyService, CompanyService>();
builder.Services.AddScoped<IShoppingCartService, ShoppingCartService>();
builder.Services.AddScoped<IApplicationUserService, ApplicationUserService>();

// Other Services
builder.Services.AddScoped<IEmailSender, EmailSender>();
```  

---

---

## 🎥 Demo Video

[▶️ Watch Demo Video](https://drive.google.com/file/d/1aSm9gJFtC6C02egUPmeI0udee4gc_nDT/view)

---

## 🎞️ Screenshots

> _All screenshots are pulled directly from the `Kevin_MVC` repo via raw URLs_

### Home Pages  
| Guest View | Logged‑in View | Product Details |
|:---------:|:--------------:|:---------------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/home_admin_1.png" alt="Home (Guest)" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/home_admin_2.png" alt="Home (User)" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/home_admin_product_details.png" alt="Product Details" style="width:100%;"/></div> |

### Shopping Cart  
| Cart List | Cart Detail |
|:---------:|:-----------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/shopping_cart_1.png" alt="Cart List" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/shopping_cart_2.png" alt="Cart Detail" style="width:100%;"/></div> |

---

### Admin: Category Management  
| List | Create | Edit |
|:----:|:------:|:----:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_category_list.png" alt="Category List" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_category_create.png" alt="Create Category" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_category_edit.png" alt="Edit Category" style="width:100%;"/></div> |

### Admin: Product Management  
| List | Edit 1 | Edit 2 | Delete | Quick Delete |
|:----:|:-----:|:------:|:------:|:------------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_product_list.png" alt="Product List" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_product_edit_1.png" alt="Edit Step 1" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_product_edit_2.png" alt="Edit Step 2" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_product_delete.png" alt="Delete Product" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_product_quickdelete.png" alt="Quick Delete" style="width:100%;"/></div> |

### Admin: Company Management  
| List | Create | Edit | Delete |
|:----:|:------:|:----:|:------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_company_list.png" alt="Company List" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_company_create.png" alt="Create Company" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_company_edit.png" alt="Edit Company" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_company_delete.png" alt="Delete Company" style="width:100%;"/></div> |

### Admin: User Management  
| List | Add User | Create User |
|:----:|:--------:|:-----------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_user_list.png" alt="User List" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_add_user.png" alt="Add User" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_user_create.png" alt="Create User" style="width:100%;"/></div> |

### Admin: Order Management  
| List | Update |
|:----:|:------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_order_list.png" alt="Order List" style="width:100%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/admin_order_update.png" alt="Update Order" style="width:100%;"/></div> |




---

### 🛒 [eCommerceMVC](https://github.com/asde9875/eCommerceMVC)  
A robust and production-style **ASP.NET MVC eCommerce website**, designed to handle real-world use cases like shopping, tracking, and category-based product browsing. Built with scalability in mind, this project covers the full shopping experience from category to checkout.

> 🛠️ **Key Functionalities:**
> - Mobile accessories store with multilingual support  
> - Complete shopping cart and checkout system  
> - Category filters (Headphones, Chargers, Stands, etc.)  
> - Product grid layout with discount tags and slider UI  
> - Clean, modern UI with backend-ready structure

---

Thanks for stopping by! 
Feel free to explore my repositories or connect with me via the sidebar in my projects.
