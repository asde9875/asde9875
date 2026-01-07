## 👋 Hi there, I'm Kevin  

Welcome to my GitHub!

Below are some of my featured projects that showcase both functionality and visual design.

<img src="https://github.com/asde9875/asde9875/raw/main/logo_update.gif" width="300" />

---

## 📚 Project Index

1. [Kevin_MVC](#kevin_mvc)
2. [eCommerceMVC](#ecommercemvc)

---

## 🚀 Featured Projects

### 📚 [Kevin_MVC](https://github.com/asde9875/Kevin_MVC)  <a name="kevin_mvc"></a>
A full‑stack ASP .NET Core MVC bookstore demo combining a playful front‑end with a robust admin console and complete shopping workflow. Key highlights include:

<div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/Kevin_MVC/master/images/home_admin_1.png" alt="Home (Guest)" style="width:100%;"/></div>


### 🛠️ Key Functionalities

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

## 🎥 Demo Video

[▶️ Watch Demo Video](https://drive.google.com/file/d/1aSm9gJFtC6C02egUPmeI0udee4gc_nDT/view)

---

## Screenshots

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


## ═════════════════════════════════════════════════════


### 📚 [eCommerceMVC](https://github.com/asde9875/eCommerceMVC)  <a name="ecommercemvc"></a> 
A robust and production-style **ASP.NET MVC eCommerce website**, designed to handle real-world use cases like shopping, tracking, and category-based product browsing. Built with scalability in mind, this project covers the full shopping experience from category to checkout.

<div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/home_page_1.png" /></div>

### 🛠️ Key Functionalities

> - Mobile accessories store with multilingual support  
> - Complete shopping cart and checkout system  
> - Category filters (Headphones, Chargers, Stands, etc.)  
> - Product grid layout with discount tags and slider UI  
> - Clean, modern UI with backend-ready structure

**Database & Identity**  
> - Default: Microsoft SQL Server via Entity Framework Core  
> - Easily swap to other providers (PostgreSQL, MySQL, Oracle, SQLite, IBM DB2)  
> - Auto‑seeded roles & users (Administrator, Moderator, User) via `eCommerceDbInitializer`

**Admin Dashboard**  
> - Overview cards for Total Products, Categories, Orders, Comments, Users, and Roles  
> - Sidebar navigation: Dashboard, Categories, Products, Promos, Orders, Comments, Users, Roles, Newsletter, Languages, Configurations  
> - Real‑time role‑based data summary (Products, Users, Orders, etc.)

**Category Management**  
> - Hierarchical category structure with parent–child relationships  
> - Search/filter by Parent Category, DataTables list with inline Edit/Delete  
> - Admins can add/edit categories using modal or dedicated form

**Product Management**  
> - Searchable and paginated product table  
> - Admin CRUD: add/edit product name, description (TinyMCE), price tiers, category, tags, and multiple product images  
> - Stock quantity & low‑stock indicators supported

**Order Management**  
> - Filterable Orders list, each with a summary view  
> - Real‑time order tracking, support for Stripe delayed payment  
> - Admin actions: Process, Ship, Cancel, Refund

**Localization & Language Switching**  
> - UI for adding custom languages with short codes and icons  
> - Fully switchable UI (e.g. English ↔ Mandarin)  
> - Built-in support for RTL and locale expansion

**Customer Experience**  
> - Cart & Checkout process with address and contact form  
> - Profile section with editable avatar, change password, comment history, and order list  
> - Guest vs. Logged-in UI, multilingual switcher with flag dropdown


---

### 📂 Solution Structure  
Below is the project folder organization for Kevin_MVC:  

```
eCommerceMVC/
├── eCommerce.Data/                # Handles EF context and DB initialisation
│   ├── Migrations/                # EF migrations folder
│   ├── eCommerceContext.cs       # Main DB context
│   └── eCommerceDBInitializer.cs # Seeds roles, admin users etc.
│
├── eCommerce.Entities/           # Defines all domain models (ORM-mapped)
│   ├── BaseEntity.cs             # Base class for common entity properties
│   ├── Product.cs, Category.cs   # Product-related models
│   ├── Order.cs, OrderItem.cs    # Order and order item models
│   ├── eCommerceUser.cs          # Extended Identity user model
│   ├── Language.cs, LanguageResource.cs  # For localisation support
│   ├── Promo.cs, PromoTypes.cs   # Promo and pricing types
│   └── [Others...]               # Comments, Configurations, Newsletter, etc.
│
├── eCommerce.Services/           # Business logic layer (Service classes)
│   ├── OrdersService.cs
│   ├── ProductsService.cs
│   ├── LanguagesService.cs
│   ├── eCommerceUserManager.cs   # Custom identity manager
│   └── [Others...]               # Role mgmt, email, dashboard service, etc.
│
├── eCommerce.Shared/             # Shared utilities & helpers
│   ├── Attributes/               # Custom data annotations
│   ├── Enums/                    # Enum definitions (OrderStatus, Roles etc.)
│   ├── Extensions/, Helpers/     # Common helper methods
│   └── Methods.cs
│
└── eCommerce.Web/                # MVC UI application
    ├── Areas/                    # Separated areas (e.g., Admin area)
    ├── Controllers/              # CartController, ProductController etc.
    ├── ViewModels/               # Models passed to views
    ├── Views/
    │   ├── Cart/, Orders/, Users/
    │   ├── Categories/, Comments/
    │   └── Shared/               # _Layout.cshtml, partials
    ├── App_Start/, Global.asax   # Routing, bundles, filters
    ├── Content/                  # CSS, JS, icons
    └── Web.config, Startup.cs    # Web app entry and DI config
```    
---

### 🧩 Dependencies (NuGet)

The following NuGet packages are included in this project (`packages.config` based - targeting .NET Framework 4.7.2 / 4.8):

- **Entity Framework & Identity**
  - `EntityFramework` `v6.4.4`
  - `Microsoft.AspNet.Identity.Core` `v2.2.3`
  - `Microsoft.AspNet.Identity.EntityFramework` `v2.2.3`
  - `Microsoft.AspNet.Identity.Owin` `v2.2.3`

- **ASP.NET MVC & Web API**
  - `Microsoft.AspNet.Mvc` `v5.2.9`
  - `Microsoft.AspNet.Razor` `v3.2.9`
  - `Microsoft.AspNet.WebPages` `v3.2.9`
  - `Microsoft.AspNet.WebApi.Core` `v5.2.9`
  - `Microsoft.AspNet.WebApi.WebHost` `v5.2.9`
  - `Microsoft.AspNet.WebApi.Owin` `v5.2.9`
  - `Microsoft.AspNet.WebApi.Client` `v5.2.9`
  - `Microsoft.AspNet.Web.Optimization` `v1.1.3`

- **OWIN & External Auth**
  - `Microsoft.Owin` `v4.2.2`
  - `Microsoft.Owin.Host.SystemWeb` `v4.2.2`
  - `Microsoft.Owin.Security.*` (Cookies, OAuth, Facebook, Google, Twitter, MicrosoftAccount) `v4.2.2`
  - `Owin` `v1.0`

- **Other Core Libraries**
  - `Newtonsoft.Json` `v13.0.2`
  - `System.Net.Http` `v4.3.4`
  - `System.Memory` `v4.5.5`
  - `System.Buffers` `v4.5.1`
  - `System.Numerics.Vectors` `v4.5.0`
  - `System.Text.Encoding.CodePages` `v7.0.0`
  - `System.Runtime.CompilerServices.Unsafe` `v6.0.0`

- **Security & Cryptography**
  - `System.Security.Cryptography.Algorithms` `v4.3.1`
  - `System.Security.Cryptography.Encoding` `v4.3.0`
  - `System.Security.Cryptography.Primitives` `v4.3.0`
  - `System.Security.Cryptography.X509Certificates` `v4.3.2`

- **Image & Web Tools**
  - `SixLabors.ImageSharp` `v2.1.3`
  - `WebGrease` `v1.6.0`
  - `Microsoft.Web.Infrastructure` `v2.0.0`

- **Others**
  - `AuthorizeNet` `v2.0.3` – for payment gateway integration
  - `Antlr` `v3.5.0.2` – dependency for Razor or Web API parsing internals
  - `Microsoft.CodeDom.Providers.DotNetCompilerPlatform` `v3.6.0` – C# compiler support for ASP.NET runtime

---

## 🎥 Demo Video  
[▶️ Watch Demo Video](https://drive.google.com/file/d/1NU70T0xibMHGMVzVLM0NQ5r-GsndL4gC/view?usp=sharing)

---

## Screenshots  
> _All screenshots use absolute GitHub paths with consistent formatting_

### Home Page  
| Banner View | Carousel + Category | Product Grid |
|:-----------:|:-------------------:|:------------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/home_page_1.png" /></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/home_page_2.png" /></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/home_page_3.png" /></div> |

### Product & Cart  
| Product List | Product Detail | Add to Cart |
|:------------:|:--------------:|:-----------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/product_1.png" /></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/product_details.png" /></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/product_add_to_cart.png" /></div> |

| Cart View | Checkout |
|:---------:|:--------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/cart_detail.png" /></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/check_out.png" /></div> |

### User Profile  
| User Dashboard | Order History |
|:--------------:|:-------------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/user_profile.png" /></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/customer_profile.png" /></div> |

### Language & Navigation  
| Change Language | Set Language Successfully |
|:---------------:|:----------------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/home_page_change_bgcolor.png" /></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/language_change_successful.png" /></div> |

### Admin Dashboard  
| Dashboard | Overview |
|:---------:|:--------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/admin_dashboard_1.png" /></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/admin_dashboard_2.png" /></div> |

### Order Management  
| Order Tracking | Admin Order Control |
|:--------------:|:-------------------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/tracking.png" /></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/admin_dashboard_4.png" /></div> |

### Others  
| Fake About Us | Refund Policy | Register |
|:-------------:|:-------------:|:--------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/fake_about_us.png" /></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/refund_policy_1.png" /></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://raw.githubusercontent.com/asde9875/eCommerceMVC/master/images/register_account.png" /></div> |


---

Thanks for stopping by! 
Feel free to explore my repositories or connect with me via the sidebar in my projects.
