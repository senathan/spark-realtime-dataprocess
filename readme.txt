spark streaming、spark连接mysql、gp的相关技术。
Category

📂 Database Stories
| DB-01 | Schema Design Updates | Create new tables and update existing ones with additional columns based on new ERD. | Database | 2 | Schema |
| DB-02 | Java Layer Implementation | Implement repositories, POJO classes, and unit tests for all new DB entities. | Database | 3 | Backend Java |

📂 Batch Jobs
| BATCH-01 | Add Email Field in SPDW Table | Modify existing table schema to include email field with validations and impact analysis. | Batch | 1 | Schema |
| BATCH-02 | Load Akamai Templates | Pull templates data via API and store in Akamai_Templates table. | Batch | 2 | Data Load |
| BATCH-03 | Load Akamai Property Configs | Fetch and persist property config data into DB with config_id mapping. | Batch | 2 | Data Load |
| BATCH-04 | Load Akamai Security Policies | Retrieve and store security policy data mapped by config_id. | Batch | 2 | Data Load |
| BATCH-05 | Load Akamai Host Information | Collect HTTP methods, TTL, DNS record type, etc. and persist. | Batch | 2 | Data Load |
| BATCH-06 | Load Akamai Certificate Info | Extract certificate info (status, validity, primary) from CPS API. | Batch | 2 | Data Load |
| BATCH-07 | Map Hostnames with Other Tables | Integrate Akamai_Hostnames data with property config and security policy mappings. | Batch | 2 | Integration |
| BATCH-08 | MDC Logging Setup | Setup MDC context for batch logging with trace and correlation IDs. | Batch | 1 | Logging |
| BATCH-09 | UAT Data Load & Cron Validation | Load UAT data and validate scheduled jobs via cron. | Batch | 1 | UAT Prep |

📂 UI Stories
| UI-01 | Design Menu and Landing Page | Create Angular-based layout for main menu and landing page. | UI | 1.5 | UI Design |
| UI-02 | Display Onboarding Grid | Fetch and display onboarding data from DB in a responsive table. | UI | 2 | Data Display |
| UI-03 | Display Service Info | Load and render service information section when row is selected. | UI | 1.5 | Data Display |
| UI-04 | Implement Filter/Search | Add search and filter support with validations. | UI | 1.5 | UX Enhancements |
| UI-05 | Display Host Info | Render host-specific values in section 2 of the UI. | UI | 1.5 | Data Display |
| UI-06 | New Onboarding Modal | Create pop-up modal with stepper for new onboarding flow. | UI | 2 | UX Feature |
| UI-07 | Additional User Fields Grid | Show user inputs in grid layout before review. | UI | 1.5 | UX Feature |
| UI-08 | Configuration Details View | Load and display Akamai property/config/security mappings. | UI | 1.5 | Data Display |
| UI-09 | Error State Handling | Show error states on onboarding failure (API/data mismatch). | UI | 1.5 | Validation |
| UI-10 | Review Page Before Submit | Build final preview screen summarizing all user inputs. | UI | 1.5 | UX Feature |
| UI-11 | UI Logging Setup | Enable UI logs with MDC context + error capture. | UI | 1 | Logging |

📂 Common Stories
| COMMON-01 | CI/CD Pipeline Updates | Update pipeline for UAT/PROD image promotions, system account setup. | Common | 2 | DevOps |
| COMMON-02 | Project Documentation | Prepare README, Architecture, Runbook, LCT for all components. | Common | 2.5 | Documentation |
| COMMON-03 | UAT Release Planning | Coordinate UAT deployment plan with validation checklist. | Common | 1.5 | Release Management |

