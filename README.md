## 👋 Hi there, I'm Kevin  

Welcome to my GitHub!

Below are some of my featured projects that showcase both functionality and visual design.

<img src="https://github.com/asde9875/asde9875/raw/main/logo_update.gif" width="300" />

---

## 📚 Project Index

1. [Kevin_MVC](#kevin_mvc)
2. [eCommerceMVC](#ecommercemvc)
3. [manga-detector](#manga-detector)

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





=====================================================================
## 🚀 Featured Projects

### 📚 [MANGA-DETECTOR](https://github.com/asde9875/manga-detector)  <a name="manga-detector"></a>

A manga and comic text cleaning platform that integrates specialised OCR, computer-vision processing, and neural inpainting to convert illustrated pages into readable and localised content. Key highlights include:

- Implemented a **manga-optimised OCR pipeline** using Manga OCR to accurately recognise stylised dialogue and captions that traditional OCR engines handle poorly.  
- Built an **OpenCV processing layer** to generate and refine masks around detected text regions, enabling precise removal without damaging line art.  
- Integrated **DeepL translation service** to support multilingual localisation of recognised text, preserving original tone and layout intent.  
- Designed a **background reconstruction workflow** with BRIA inpainting wrapper to restore artwork after text deletion, producing natural panel and banner visuals.  
- Developed memory-guard utilities to mitigate high resource consumption during inference, ensuring stable processing of high-resolution pages.  
- Containerised Python and Java components with Docker for easy demonstration and sharing with stakeholders and interview reviewers.

Tech: Python, Manga OCR, OpenCV, DeepL API, BRIA Inpainting, Docker, Spring Boot integration



📁Structure for MANGA-DETECTOR

``` 
MANGA-DETECTOR/
├── backend/app/                                  # Python backend application root
│   └── pcleaner/                                 # PCleaner: manga-oriented text detection and cleaning toolkit
│       ├── comic_text_detector/                  # Core text-region detection pipeline for comics and manga pages
│       ├── gui/                                  # Local visual interface tools for selective region inspection
│       ├── ocr/                                  # OCR wrappers used by the cleaning workflow
│       ├── data/                                 # Sample assets and runtime resources
│       ├── **init**.py                           # Package entry
│       ├── main.py                               # Primary processing flow: detect -> mask -> inpaint -> export
│       ├── ctd_interface.py                      # Interface to the text detector model
│       ├── mask.py                               # Mask generation logic
│       ├── masker.py                             # Advanced mask refinement
│       ├── inpainting.py                         # Background reconstruction after text removal
│       ├── denoiser.py                           # Noise reduction to improve downstream quality
│       ├── image_ops.py                          # Common OpenCV image transformations
│       ├── image_export.py                       # Result output utilities
│       ├── memory_watcher.py                     # Guards against high memory usage during inference
│       ├── model_downloader.py                   # Downloads models instead of storing large weights in git
│       ├── helpers.py                            # Shared helper functions
│       └── cli_utils.py                          # Command-line utilities and arguments parser
│
├── backend-v1/                                   # Python API service layer
│   ├── service/                                  # Modular services
│   │   ├── **init**.py
│   │   ├── manga_ocr_service.py                  # Manga OCR recognition service
│   │   ├── manga_cv2_service.py                  # OpenCV-based text removal and image processing
│   │   ├── manga_deepl_service.py                # DeepL translation integration
│   │   └── briaService.py                        # BRIA third-party inpainting/generation wrapper
│   ├── app.py                                    # Backend service entrypoint (FastAPI style)
│   ├── config.py                                 # Environment and paths configuration
│   └── requirements.txt                          # Dependencies for backend-v1
│
├── backend-java/                                 # Java backend (Maven / Spring Boot)
│   ├── src/                                      # Java source code
│   ├── target/                                   # Maven build outputs (ignored in git)
│   ├── .mvn/
│   └── pom.xml                                   # Maven dependencies and build config
│
├── frontend/                                     # React + TypeScript frontend
│   ├── public/                                   # Static public assets
│   ├── src/                                      # UI pages and components
│   ├── index.html                                # SPA entry
│   ├── package.json                              # Frontend dependencies
│   └── tsconfig.json                             # TypeScript config
│
├── fonts/                                        # Multilingual fonts used by OCR and rendering
│   ├── noto_sans_chinese/
│   ├── noto_sans_english/
│   ├── noto_sans_japanese/
│   ├── noto_sans_korean/
│   └── noto_sans_korean/
│
├── static/                                       # Global static resources for the web site
├── model-fake/                                   # Placeholder models for testing without real weights
├── Readme-Pic/                                   # Images referenced by README documentation
│
├── README.md                                     # Overall project documentation
└── requirements.txt                              # Root Python dependencies


``` 


# Boost Frontend:

1. cd frontend/uploadPage
3. npm i
4. npm run dev


## Run backend:

``` 
RUN [pip install pydantic-settings]
``` 

### for api's timezone

``` 
RUN [pip install tzdata]
``` 

### And run the server

``` 
uvicorn backend.app.main:app 
``` 

### The uploaded file will be saved under the folder /static/uploads_imgs


### The removed_text images will be saved under the folder 
``` 
/static/removed_text_imgs
``` 

### The preview images for letting users choose fonts will be saved under the folder 
``` 
/static/edited_imgs/
``` 

### all the environment variable settings can be seen from 
``` 
.env
``` 

### or through 
``` 
/backend/app/configs/config/config.py file
```

### You can also access the open api document to get a better understanding of the api structure and requirement

``` 
http://localhost:8000/docs
``` 

---


# V2.0.0 Manga Backend Image

## 📦 Docker Commands (Windows)

### ✅ Step 1: Pull the image
``` 
docker pull asde9875/manga-backend-winonly:2.0.0
``` 


### ✅ Step 2: Run the container
``` 
docker run --name manga-ocr -p 8000:8000 asde9875/manga-backend-winonly:2.0.0
``` 


This will start the API service and listen on: http://localhost:8000



## 📦 Docker Commands (Mac)

### ✅ Step 1: Pull the image
``` 
docker pull asde9875/manga-backend:2.0.0
``` 


### ✅ Step 2: Run the container
``` 
docker run --name manga-ocr -p 8000:8000 asde9875/manga-backend:2.0.0
``` 


This will start the API service and listen on: http://localhost:8000

---

## V2.0.0 Major Updates

### 1. CV2 Module Updates

``` 
Integrated ONNX AI speech-bubble detection model:

In V2.0.0, we added an AI model that automatically detects manga speech-bubble regions (speech bubbles) into the original CV2 text removal pipeline.

Improved accuracy:

When removing text, the system prioritizes the bubble regions detected by AI (instead of relying only on user-drawn boxes or traditional threshold rules), resulting in smarter and more precise boundaries.

It can automatically avoid common mistakes such as “box too large / too small / shifted”.
``` 


### 2. Why Introduce the ONNX Model?

``` 
To increase automation in text detection and removal:

Previously, relying only on OpenCV or user manual boxes often caused false positives, leftover text, or incomplete removal.

The AI model can adapt to different manga styles and bubble shapes, greatly improving compatibility with complex images and boosting automation.

Human-AI collaboration (human-in-the-loop):

The user box can be used to supplement/correct special areas.

The AI model handles most mainstream speech bubbles automatically.
``` 


### 3. Key Differences vs V1.0.0

| **Feature / Capability**             | **V1.0.0**                                  | **V2.0.0**                                                       |
|-------------------------------------|---------------------------------------------|------------------------------------------------------------------|
| Speech bubble detection             | Traditional methods / manual user boxes only| ✅ Added AI ONNX automatic bubble detection                       |
| Text removal precision              | Depends on user boxes / simple rules        | ✅ AI boxes + user boxes merged for more accurate regions         |
| Automation level                    | Mostly manual                               | ✅ Most bubble regions can be auto-detected/processed             |
| Model management                    | Some models downloaded manually             | ✅ All major models managed via Git LFS                           |
| Dependencies & Docker support       | Python 3.10/3.11 not fully compatible       | ✅ Fully compatible with Python 3.12, more stable Docker setup    |
| Logging & outputs                   | Basic                                       | ✅ Improved log structure and better traceability for debugging   |



### 🔧 Postman Testing Guide

Please ensure Docker is running and port 8000 is open. The following endpoints should be tested in order:



### 🎨 CV2 Fill API

URL: http://localhost:8000/api/v1/images/cv2-fill

Method: POST

Header: Content-Type: application/json

Presigned URL must be obtained via Spring Boot request:

http://localhost:8080/api/image/{fileId}




#### Test Cases

<div style="max-width:300px; margin:1em auto;"><img src="https://github.com/asde9875/manga-detector/blob/main/Readme-Pic/Sample_2.png" alt="Cart Detail" style="width:50%;"/></div>

<div style="max-width:300px; margin:1em auto;"><img src="https://github.com/asde9875/manga-detector/blob/main/Readme-Pic/Sample_1.png" alt="Cart Detail" style="width:30%;"/></div>

---







—— AI Bubble Detection Output Example (Perfect bubble detection) ——

#### #1: {'x_min': 61, 'y_min': 430, 'x_max': 117, 'y_max': 499}

#### #2: {'x_min': 476, 'y_min': 432, 'x_max': 535, 'y_max': 502}

#### #3: {'x_min': 479, 'y_min': 693, 'x_max': 526, 'y_max': 788}

#### #4: {'x_min': 200, 'y_min': 544, 'x_max': 247, 'y_max': 660}

#### #5: {'x_min': 323, 'y_min': 326, 'x_max': 359, 'y_max': 394}

#### #6: {'x_min': 249, 'y_min': 324, 'x_max': 288, 'y_max': 407}


---


#### 1. Completely shifted (box is on blank area, no overlap) (✅ Pass)

```json
{

"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 1, "x_min": 0, "y_min": 0, "x_max": 50, "y_max": 50 }

]

}
```




#### 2. Box too large (covers multiple bubbles) (✅ Pass)

```json
{

"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 2, "x_min": 50, "y_min": 300, "x_max": 540, "y_max": 800 }

]

}
```




#### 3. Box too small (covers only a corner of the bubble) (✅ Pass)

```json
{

"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 3, "x_min": 320, "y_min": 320, "x_max": 330, "y_max": 340 }

]

}
```


#### 4. Mostly correct but slightly shifted (IoU exists but < 0.5) (✅ Pass)

```json
{

"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 4, "x_min": 65, "y_min": 435, "x_max": 120, "y_max": 510 }

]

}
```


#### 5. Totally random box (far away from bubble) (✅ Pass)

```json
{

"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 5, "x_min": 600, "y_min": 50, "x_max": 700, "y_max": 200 }

]

}
```




#### 6. Mixed multiple boxes: one correct + one too large + one too small + one missed completely (✅ Pass)

```json
{

"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 1, "x_min": 323, "y_min": 326, "x_max": 359, "y_max": 394 },    // correct


{ "region_id": 2, "x_min": 0, "y_min": 0, "x_max": 600, "y_max": 800 },        // too large

{ "region_id": 3, "x_min": 478, "y_min": 693, "x_max": 484, "y_max": 698 },    // too small

{ "region_id": 4, "x_min": 10, "y_min": 10, "x_max": 30, "y_max": 20 }         // no hit

]

}
```





#### 7. AI detected boxes overlap / duplicates (✅ Pass)

```json
{

"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 7, "x_min": 240, "y_min": 340, "x_max": 360, "y_max": 480 }

]

}
```

(Assume AI bubbles 340400 and 360420 overlap; this user box may cover both bubbles.)



#### 8. Multiple user boxes overlap the same AI bubble (✅ Pass)

```json
{

"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 8, "x_min": 60, "y_min": 440, "x_max": 120, "y_max": 500 },

{ "region_id": 9, "x_min": 100, "y_min": 460, "x_max": 160, "y_max": 520 }

]

}
```

(Both boxes intersect the same AI bubble; check whether it is processed repeatedly.)



#### 9. Half correct, half wrong user boxes (✅ Pass)

```json
{

"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 10, "x_min": 323, "y_min": 326, "x_max": 359, "y_max": 394 },  // precisely covers AI bubble

{ "region_id": 11, "x_min": 600, "y_min": 50, "x_max": 605, "y_max": 52 }     // completely wrong (too far / too small)

]

}
```

---


#### 10. Extremely small / narrow / flat boxes (✅ Pass)

```json
{

"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 12, "x_min": 320, "y_min": 320, "x_max": 322, "y_max": 400 }, // extremely narrow vertical

{ "region_id": 13, "x_min": 400, "y_min": 500, "x_max": 480, "y_max": 502 }  // extremely flat horizontal

]

}
```




#### 11. A user box fully covers all AI bubbles (✅ Pass)

```json
{

"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 14, "x_min": 0, "y_min": 0, "x_max": 1000, "y_max": 1000 }

]

}
```


(Assume image size is 1000x1000; this box fully contains all bubbles.)



#### 12. User box slightly overlaps a corner of an AI bubble (✅ Pass)

```json
{

"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 15, "x_min": 60, "y_min": 495, "x_max": 65, "y_max": 505 }

]

}
```


(It only touches a small corner of the AI bubble; test AI box merging and processing.)



#### 13. Extreme corner test cases (boundary edge cases) (✅ Pass)

```json
{
"image_url": "https://your-s3-url.jpg",

"regions": [

{ "region_id": 16, "x_min": 0, "y_min": 0, "x_max": 10, "y_max": 10 },         // top-left

{ "region_id": 17, "x_min": 990, "y_min": 0, "x_max": 999, "y_max": 10 },      // top-right

{ "region_id": 18, "x_min": 0, "y_min": 990, "x_max": 10, "y_max": 999 },      // bottom-left

{ "region_id": 19, "x_min": 990, "y_min": 990, "x_max": 999, "y_max": 999 }    // bottom-right

]

}
```




#### OCR Test Results


| Test | Result |
|:---------:|:-----------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://github.com/asde9875/manga-detector/blob/main/Readme-Pic/Sample_3.png" alt="Cart List" style="width:70%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://github.com/asde9875/manga-detector/blob/main/Readme-Pic/Sample_4.png" alt="Cart Detail" style="width:50%;"/></div>  <div style="max-width:300px; margin:1em auto;"><img src="https://github.com/asde9875/manga-detector/blob/main/Readme-Pic/Sample_5.png" alt="Cart Detail" style="width:50%;"/></div> |





#### CV2 Test Results


| Test | Result |
|:---------:|:-----------:|
| <div style="max-width:300px; margin:1em auto;"><img src="https://github.com/asde9875/manga-detector/blob/main/Readme-Pic/Sample_3.png" alt="Cart List" style="width:70%;"/></div> | <div style="max-width:300px; margin:1em auto;"><img src="https://github.com/asde9875/manga-detector/blob/main/Readme-Pic/Sample_6.png" alt="Cart Detail" style="width:50%;"/></div>  <div style="max-width:300px; margin:1em auto;"><img src="https://github.com/asde9875/manga-detector/blob/main/Readme-Pic/Sample_7.png" alt="Cart Detail" style="width:50%;"/></div> |



---


# V1.0.0 Manga Backend Image

## 📦 Docker Commands (Windows / Mac)

### ✅ Step 1: Pull the image

```
docker pull asde9875/manga-backend:1.0.0
```


### ✅ Step 2: Run the container

```
docker run --name manga-ocr -p 8000:8000 asde9875/manga-backend:1.0.0
```


This will start the API service and listen on: http://localhost:8000



### 🔧 Postman Testing Guide

Please ensure Docker is running and port 8000 is open. The following endpoints should be tested in order:



1. ✏️ OCR API

URL: http://localhost:8000/api/v1/images/ocr

Method: POST

Header: Content-Type: application/json

Presigned URL must be obtained via Spring Boot request:

http://localhost:8080/api/image/{fileId}

Request Body:

```json
{

"image_url": "https://manga-ocr-service.s3.ap-southeast-2.amazonaws.com/070af1a0-3ba6-4814-aad7-d8257ab2f322.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20250725T224712Z&X-Amz-SignedHeaders=host&X-Amz-Credential=AKIA4MTWKJPEXDR35KW4%2F20250725%2Fap-southeast-2%2Fs3%2Faws4_request&X-Amz-Expires=1800&X-Amz-Signature=0fd19c1f9a8e3c677fe1f12fe6f6cc0f08368b34d84e9f7d2f0481c35b11108f",

"regions": [

{

"region_id": 1,

"x_min": 680,

"y_min": 70,

"x_max": 792,

"y_max": 247

}

]

}
```


Example Response:

```json
{

"results": [

{

"region_id": 1,

"text": "你到底想說什廖？"

}

]

}
```


2. 🎨 CV2 Fill API

URL: http://localhost:8000/api/v1/images/cv2-fill

Method: POST

Header: Content-Type: application/json

Presigned URL must be obtained via Spring Boot request:

http://localhost:8080/api/image/{fileId}

Request Body:

```json
{

"image_url": "https://manga-ocr-service.s3.ap-southeast-2.amazonaws.com/070af1a0-3ba6-4814-aad7-d8257ab2f322.jpg?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20250725T224712Z&X-Amz-SignedHeaders=host&X-Amz-Credential=AKIA4MTWKJPEXDR35KW4%2F20250725%2Fap-southeast-2%2Fs3%2Faws4_request&X-Amz-Expires=1800&X-Amz-Signature=0fd19c1f9a8e3c677fe1f12fe6f6cc0f08368b34d84e9f7d2f0481c35b11108f",

"regions": [

{

"region_id": 1,

"x_min": 680,

"y_min": 70,

"x_max": 792,

"y_max": 247

}

]

}
```


Example Response: (Returns an image with the selected region filled as a black box)



3. 🌐 Translation API

URL: http://localhost:8000/api/v1/images/translate

Method: POST

Header: Content-Type: application/json

Request Body:

```json
{

"texts": [

"行っちゃったね…俊くん…"

],

"target_lang": "ZH"

}
```


### 🔐 Notes

Please make sure image_url is a valid AWS S3 presigned URL.

Each endpoint uses a different JSON parameter format.

Make sure port 8000 is not occupied and the firewall is not blocking the connection.




---

Thanks for stopping by! 
Feel free to explore my repositories or connect with me via the sidebar in my projects.
