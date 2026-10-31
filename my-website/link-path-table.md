# Assignment 2.4: Link and Path Table

Site structure:

my-website/
├── index.html
├── about.html
├── projects.html
├── contact.html
└── pages/
└── services.html

Every path below is explained from the file the link is written in, not from the project root.

## A. Navigation links

The same five-link navigation appears on every page.

|#| Source file | Link name | Destination | Link type | Why it works |

|1| index.html | Home | `index.html` | Relative (same folder) | This is the current page, and it is in the same folder, so the filename alone points back to it. |

|2| index.html | About | `about.html` | Relative (same folder) | Both files are in the main `my-website/` folder, so the filename alone is enough. |

|3| index.html | Services | `pages/services.html` | Relative (child folder) | `services.html` is inside the `pages` folder, so the path goes down into `pages/` and then to the file. |

|4| index.html | Projects | `projects.html` | Relative (same folder) | Both files are in the main `my-website/` folder. |

|5| index.html | Contact | `contact.html` | Relative (same folder) | Both files are in the main `my-website/` folder. |

|6| about.html | Home | `index.html` | Relative (same folder) | Both files are in the main `my-website/` folder. |

|7| about.html | About | `about.html` | Relative (same folder) | This is the current page, in the same folder. |

|8| about.html | Services | `pages/services.html` | Relative (child folder) | The path goes down into the `pages` folder to reach the file. |

|9| about.html | Projects | `projects.html` | Relative (same folder) | Both files are in the main folder. |

|10| about.html | Contact | `contact.html` | Relative (same folder) | Both files are in the main folder. |

|11| projects.html | Home | `index.html` | Relative (same folder) | Both files are in the main folder. |

|12| projects.html | About | `about.html` | Relative (same folder) | Both files are in the main folder. |

|13| projects.html | Services | `pages/services.html` | Relative (child folder) | The path goes down into the `pages` folder to reach the file. |

|14| projects.html | Projects | `projects.html` | Relative (same folder) | This is the current page, in the same folder. |

|15| projects.html | Contact | `contact.html` | Relative (same folder) | Both files are in the main folder. |

|16| contact.html | Home | `index.html` | Relative (same folder) | Both files are in the main folder. |

|17| contact.html | About | `about.html` | Relative (same folder) | Both files are in the main folder. |

|18| contact.html | Services | `pages/services.html` | Relative (child folder) | The path goes down into the `pages` folder to reach the file. |

|19| contact.html | Projects | `projects.html` | Relative (same folder) | Both files are in the main folder. |

|20| contact.html | Contact | `contact.html` | Relative (same folder) | This is the current page, in the same folder. |

|21| pages/services.html | Home | `../index.html` | Relative (parent folder) | `services.html` is located inside `pages/`, so `../` steps up one level to `my-website/`, where `index.html` is. |

|22| pages/services.html | About | `../about.html` | Relative (parent folder) | `about.html` is in the main folder, not in `pages/`, so the path must use `../` to leave the `pages` folder first. |

|23| pages/services.html | Services | `services.html` | Relative (same folder) | This is the current page, and it is already inside `pages/`, so no folder steps are needed. Writing `pages/services.html` here would look for `pages/pages/services.html`, which does not exist. |

|24| pages/services.html | Projects | `../projects.html` | Relative (parent folder) | `projects.html` is in the main folder, so `../` steps up out of `pages/` to reach it. |

|25| pages/services.html | Contact | `../contact.html` | Relative (parent folder) | `contact.html` is in the main folder, so `../` steps up out of `pages/` to reach it. |

## B. Other links

|26| index.html | MDN Web Docs | `https://developer.mozilla.org` | External (absolute URL) | It is a full web address with the `https://` protocol and a domain name, so it works from any page in any folder without folder logic. |

|27| contact.html | developer@example.com | `mailto:developer@example.com` | Email link | The `mailto:` scheme tells the browser to open the device's default email app with that address filled in. |

|28| projects.html | Jump to Project Highlight section | `#highlight` | Fragment link (same page) | The `#` means "look on this page", so the browser scrolls to the element with `id="highlight"`. No filename is needed. |

|29| index.html | Back to top | `#top` | Fragment link (same page) | It scrolls to the element with `id="top"` on the current page, without loading a different file. |

|30| about.html | Back to top | `#top` | Fragment link (same page) | It scrolls to the element with `id="top"` on the current page. |

|31| projects.html | Back to top | `#top` | Fragment link (same page) | It scrolls to the element with `id="top"` on the current page. |

|32| contact.html | Back to top | `#top` | Fragment link (same page) | It scrolls to the element with `id="top"` on the current page. |

|33| pages/services.html | Back to top | `#top` | Fragment link (same page) | It scrolls to the element with `id="top"` on the current page. |
