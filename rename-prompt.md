You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "Employee-Login.html",
    "context": {
      "title": "Welcome to AMS Human Resources Pvt. Ltd.",
      "first_heading": ""
    }
  },
  {
    "path": "aboutus.html",
    "context": {
      "title": "About AMS HR",
      "first_heading": "About Company"
    }
  },
  {
    "path": "blog-effective-ways-to-build-team-s-communication-while-working-remotely.html",
    "context": {
      "title": "Effective ways to build team\u2019s communication while working remotely",
      "first_heading": "Effective ways to build team\u2019s communication while working remotely"
    }
  },
  {
    "path": "blog-employee-retention-a-critical-aspect-to-ensure-stability-and-success-of-your-business.html",
    "context": {
      "title": "Employee Retention - A critical aspect to ensure stability and success of your Business",
      "first_heading": "Employee Retention - A critical aspect to ensure stability and success of your Business"
    }
  },
  {
    "path": "blog-how-investing-in-human-resources-can-help-startups-and-msmes-grow.html",
    "context": {
      "title": "How investing in Human Resources can help Startups and MSMEs grow?",
      "first_heading": "How investing in Human Resources can help Startups and MSMEs grow?"
    }
  },
  {
    "path": "blog-how-payroll-outsourcing-can-be-beneficial-for-organizations.html",
    "context": {
      "title": "How Payroll Outsourcing Can Be Beneficial For Organizations?",
      "first_heading": "How Payroll Outsourcing Can Be Beneficial For Organizations?"
    }
  },
  {
    "path": "blog-maharashtra-most-preferred-hiring-destination.html",
    "context": {
      "title": "Maharashtra most preferred hiring destination",
      "first_heading": "Maharashtra most preferred hiring destination"
    }
  },
  {
    "path": "blog-temporary-staffing-an-enabler-to-your-business.html",
    "context": {
      "title": "Temporary staffing - An enabler to your business",
      "first_heading": "Temporary staffing - An enabler to your business"
    }
  },
  {
    "path": "blog-workplace-stress-alert-60-of-employees-plan-to-quit-jobs-soon-says-a-survey.html",
    "context": {
      "title": "Workplace stress alert: 60% of employees plan to quit jobs soon, says a survey",
      "first_heading": "Workplace stress alert: 60% of employees plan to quit jobs soon, says a survey"
    }
  },
  {
    "path": "blog-you-can-manage-your-stress-while-working-from-home-it-s-not-that-difficult.html",
    "context": {
      "title": "You can manage your stress while working from home - It\u2019s not that difficult!",
      "first_heading": "You can manage your stress while working from home - It\u2019s not that difficult!"
    }
  },
  {
    "path": "blog.html",
    "context": {
      "title": "",
      "first_heading": "Blog & News"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "",
      "first_heading": "ContactUs"
    }
  },
  {
    "path": "css/00b3da1e093db19e4cf870faaeec5bd5.css",
    "context": {
      "path": "css/00b3da1e093db19e4cf870faaeec5bd5.css"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/774da17082f90a3b333546af7cd3ecd1.css",
    "context": {
      "path": "css/774da17082f90a3b333546af7cd3ecd1.css"
    }
  },
  {
    "path": "css/83fb52acc44fd2c6cbd6553da2fbc725.css",
    "context": {
      "path": "css/83fb52acc44fd2c6cbd6553da2fbc725.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/a9e8199f16808a35e5f3e34c5bbd6f10.css",
    "context": {
      "path": "css/a9e8199f16808a35e5f3e34c5bbd6f10.css"
    }
  },
  {
    "path": "css/eca01d6fc8d2d7aca2c856baa355437e.css",
    "context": {
      "path": "css/eca01d6fc8d2d7aca2c856baa355437e.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "current-openings.html",
    "context": {
      "title": "Temporary Staffing Services",
      "first_heading": "Current Openings"
    }
  },
  {
    "path": "cv-writing-services.html",
    "context": {
      "title": "Resume Writing - CV Writing Services",
      "first_heading": "Resume Writing Services"
    }
  },
  {
    "path": "hr-advisory-services.html",
    "context": {
      "title": "HR Advisory Services",
      "first_heading": "HR Advisory Services"
    }
  },
  {
    "path": "imgs/038fc76234920444dfb66b2d46621cf0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/04cd26a7e71848a5ebf8e88a2669b63b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/070fe204d186f093cceb8f3bc2c22de7.webp",
    "context": {
      "refs": [
        {
          "alt": "Looking for a Job?",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0a86150b60a32eba047ec05421de717a.webp",
    "context": {
      "refs": [
        {
          "alt": "Management Team",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1090c1e6afe69fb2de485acde733b59f.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1afea54310900bfda92aa0c3a31dbbd6.webp",
    "context": {
      "refs": [
        {
          "alt": "\u201cPrevention of Workplace Harassment\u201d \u2013 A stepping stone towards creating Gender Diversity",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2170b33adaeaf10dd7e00480730d4a0e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/286c3f6a8e22466ca97ace98f4aed983.webp",
    "context": {
      "refs": [
        {
          "alt": "Dheeraj Lalvaney",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2c45f748ce125a83067465df7265f779.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/328f37317b7ecd0d0cc8745800807c82.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/371cd9c4752fd50d6a72cd0cba994035.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/391754384792b6a888b5dbb6da5fd671.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3e39582987706d41db721482687f8a62.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3ecbce1fc6fde8e2c52743f881c586ad.webp",
    "context": {
      "refs": [
        {
          "alt": "Industries Served",
          "title": ""
        },
        {
          "alt": "Industry Verticals",
          "title": ""
        },
        {
          "alt": "Industries Served",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4e7c1247ba843ec8abda6a0536159550.webp",
    "context": {
      "refs": [
        {
          "alt": "Positive Attitude",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5129179ed16b49f84b44db7ce79bfa2d.webp",
    "context": {
      "refs": [
        {
          "alt": "Manufacturing",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/541021f8f4c21a420c4031f1dab3facd.webp",
    "context": {
      "refs": [
        {
          "alt": "Retail",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/55377f2fc83236e9f14ebfd16492ec28.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5607dcd6c8265fb6586121a58a3e9859.webp",
    "context": {
      "refs": [
        {
          "alt": "Temporary staffing is a good way of giving your organization the workforce flexibility.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5d6a417cb05a99cb6acbf1d33a6e1c53.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/66d3047ee362a8b4eb22cbfe0270c756.webp",
    "context": {
      "refs": [
        {
          "alt": "Fundamentals of Leadership",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/679f1969f673f93b7ce756a19617b00f.webp",
    "context": {
      "refs": [
        {
          "alt": "Statutory Compliance Management",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/68e7b66e16dcf59745b5d1fbd64fc546.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6b5a6300155369f29a80e99647520cc2.webp",
    "context": {
      "refs": [
        {
          "alt": "Logistics",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6ba79f2795b39bfa6fc19fcb238caaf5.webp",
    "context": {
      "refs": [
        {
          "alt": "Global Business Etiquette",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6e2b502b58a6aee0c3ffe7463913f6b6.webp",
    "context": {
      "refs": [
        {
          "alt": "Payroll Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/714945ada5fe9a8232c147466798c3c1.webp",
    "context": {
      "refs": [
        {
          "alt": "Learning & Development",
          "title": ""
        },
        {
          "alt": "Learning & Development Solutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/75846477162fd86a2385da0256fc2c39.webp",
    "context": {
      "refs": [
        {
          "alt": "Looking for HR Solution?",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/76fb6308c45c840561977dec28c5b759.webp",
    "context": {
      "refs": [
        {
          "alt": "Learning & Development",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/778ce088b476a3490d58caa02448e0e9.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/7e24c73f5606bec36615e299649ca952.webp",
    "context": {
      "refs": [
        {
          "alt": "Advantages of Outsourcing Compliance Activities",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8cf90fae40b0a8ef72edd45dec08f1aa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8db9eb277c2d844cda731bf68ebcfc40.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8eaa98d024691d1bef4c6e60c16811cb.webp",
    "context": {
      "refs": [
        {
          "alt": "HR Advisory Services",
          "title": ""
        },
        {
          "alt": "HR Advisory Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/907f6656bcd769f795f263ff6a433f1e.webp",
    "context": {
      "refs": [
        {
          "alt": "Permanent Staffing Solutions",
          "title": ""
        },
        {
          "alt": "Permanent Staffing Solutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9459f24baaea1096069f86a87acea052.webp",
    "context": {
      "refs": [
        {
          "alt": "About Company",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9837ebff3012948cc26db05333a6d356.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/986e97850bc1116096082fbad15b8c1b.webp",
    "context": {
      "refs": [
        {
          "alt": "Statutory Compliance Services",
          "title": ""
        },
        {
          "alt": "Statutory Compliance Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/98d048157833e846710898487cf450dc.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/9bc71177b9c19485b5f89d77dc3a724b.webp",
    "context": {
      "refs": [
        {
          "alt": "HR Advisory Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9c50b7a9ef79b5808d0cc460db021082.webp",
    "context": {
      "refs": [
        {
          "alt": "Here are few questions for you regarding Payroll Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a490f104164a21f043b30ed302f2b591.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/a678683bad8bea6454a08b70643418a1.webp",
    "context": {
      "refs": [
        {
          "alt": "Pharma",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a77d7757f79db83c02026cd84bec2d9a.webp",
    "context": {
      "refs": [
        {
          "alt": "HighTech",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ac7570929c72f238b14268546c2c2165.webp",
    "context": {
      "refs": [
        {
          "alt": "Value Proposition & Strengths of AMS - Partnership, Process, People, Progress",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae1606d1c51197ff5a31f62126b437b5.webp",
    "context": {
      "refs": [
        {
          "alt": "Get the best talent filtered through our proven methodology!",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae7aa9ef887806e83c1043ed9398714b.webp",
    "context": {
      "refs": [
        {
          "alt": "Insurance",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae8aad159e071b2c6335dd40e473c5b7.webp",
    "context": {
      "refs": [
        {
          "alt": "Business Communication",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0dc1228f2c289cb6d03084943206cf0.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b0f3edf865dad4976df89ae8e33ee767.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b49aeb98a3ee25c12d255bab6a14e467.webp",
    "context": {
      "refs": [
        {
          "alt": "Banking",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5721aca08135b6e061e17fae4016faa.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b64133c13f0741c01afe65c0a591fba6.webp",
    "context": {
      "refs": [
        {
          "alt": "Dheeraj Lalvaney",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b6e2e37c0469f5590410e7aec0ef3ac0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9832ce1e3dabce86326d05cacb89f43.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/bbca0810c7a5ad08bb64b3df3d7f568d.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc26b60905a3cde8bd01d4872187a47a.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/be7b3ee99b12fa939c35a0e1c9b6c367.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c0dd964dae8639209677d983ee8c2dc0.webp",
    "context": {
      "refs": [
        {
          "alt": "TemporaryStaffingLandingForground",
          "title": ""
        },
        {
          "alt": "Temporary Staffing",
          "title": ""
        },
        {
          "alt": "Temporary Staffing",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1ec2177520de19f711646ff95f865e6.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c31a06fed06d7067d7e2ba348bec9420.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c586fc6da08e15963dde52f836f7d130.webp",
    "context": {
      "refs": [
        {
          "alt": "Resume Writing Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c6ca604be78b1d71970678300ad99b68.webp",
    "context": {
      "refs": [
        {
          "alt": "Resources",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c705f441cd9fd7cc2a2c4ed95a8dbf6b.webp",
    "context": {
      "refs": [
        {
          "alt": "Art of Public Speaking \u2013 Walk the talk",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c86f77e8f0fe9e0050defeba111fa31f.webp",
    "context": {
      "refs": [
        {
          "alt": "Compliance Audit",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c9ad7a60a89f057aac01bb7e21b8f1b3.webp",
    "context": {
      "refs": [
        {
          "alt": "Business Presentation Skills",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cbf4933c709f9471d15aac8d0af572fa.webp",
    "context": {
      "refs": [
        {
          "alt": "HR Advisory",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0ff6d44c0609e8df4c761f2eadf145c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d4052beb4fd9f9ae8034c6d287d16bae.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d732f726ed9ac5778b8f59a88cce9fb1.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d9c1706bda09f289b710d47c423b3d26.webp",
    "context": {
      "refs": [
        {
          "alt": "Stress Management",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dd967d640e56d0b653e41f29daaeb45a.webp",
    "context": {
      "refs": [
        {
          "alt": "Time Management",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de753a4fc9da856175ef11076213d4b5.webp",
    "context": {
      "refs": [
        {
          "alt": "Temporary or Contract Staffing",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e73b1f12d7adfd6dac9a7ef535234219.webp",
    "context": {
      "refs": [
        {
          "alt": "Payroll Services",
          "title": ""
        },
        {
          "alt": "Payroll Services",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec7549f4723798d70851c22c31705bb3.webp",
    "context": {
      "refs": [
        {
          "alt": "Team Building & Conflict Management",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ef1b985c9cfcee05be58fdfb03a31a63.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ef5911c5f25d0b29003f44f15e58709f.webp",
    "context": {
      "refs": [
        {
          "alt": "Compliance Management",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f2eb8293bb43e708a9c7cfe481b39046.webp",
    "context": {
      "refs": [
        {
          "alt": "Train the Trainer",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f400e64a58b7e2a681c03e61e1f58a4e.webp",
    "context": {
      "refs": [
        {
          "alt": "Automotive",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f4093f9f5a492284f7980ab6cafc1a59.webp",
    "context": {
      "refs": [
        {
          "alt": "Payroll Service Offerings",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f71f0c82e42bfd7eee4debb44f47ac55.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f8e61fac65c46610099273776128c5a5.webp",
    "context": {
      "refs": [
        {
          "alt": "Permanent Staffing",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f93fc7f7d2a35bf8ab9e7991c630cbcb.webp",
    "context": {
      "refs": [
        {
          "alt": "Compliance Advisory",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Welcome to AMS Human Resources Pvt. Ltd.",
      "first_heading": "Staffing | Compliances | HR Advisory | Learning Solutions"
    }
  },
  {
    "path": "industries-served.html",
    "context": {
      "title": "Industry Verticals",
      "first_heading": "Industries Served"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/fd8b05e4ab768b134ce5d3c4dd39046a.js",
    "context": {
      "path": "js/fd8b05e4ab768b134ce5d3c4dd39046a.js"
    }
  },
  {
    "path": "learning-and-development-solutions.html",
    "context": {
      "title": "Learning & Development - Training & Development Solutions",
      "first_heading": "Learning & Development Solutions"
    }
  },
  {
    "path": "management-team.html",
    "context": {
      "title": "",
      "first_heading": "Management Team"
    }
  },
  {
    "path": "payroll-services.html",
    "context": {
      "title": "Payroll Outsourcing Services",
      "first_heading": "Payroll Services"
    }
  },
  {
    "path": "permanent-staffing-solutions.html",
    "context": {
      "title": "Permanent Staffing - Recruitment Solutions",
      "first_heading": "Permanent Staffing Solutions"
    }
  },
  {
    "path": "services-offered.html",
    "context": {
      "title": "",
      "first_heading": "ServicesOffered"
    }
  },
  {
    "path": "statutory-compliance-services.html",
    "context": {
      "title": "Statutory Compliance Services",
      "first_heading": "Statutory Compliance Services"
    }
  },
  {
    "path": "temporary-staffing.html",
    "context": {
      "title": "Temporary Staffing Services",
      "first_heading": "Temporary Staffing"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.