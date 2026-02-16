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
    "path": "about-us.html",
    "context": {
      "title": "Tycnodot Business Solutions | About Us",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "Tycnodot Business Solutions | Contact Us",
      "first_heading": "CONTACT US"
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
    "path": "css/7cd3c01f553780097ebe1c4668033bfe.css",
    "context": {
      "path": "css/7cd3c01f553780097ebe1c4668033bfe.css"
    }
  },
  {
    "path": "css/7e610f95a2d26c26bc901487cdcd9a1c.css",
    "context": {
      "path": "css/7e610f95a2d26c26bc901487cdcd9a1c.css"
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
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "how-we-help.html",
    "context": {
      "title": "Tycnodot Business Solutions | How We Help",
      "first_heading": "HOW WE HELP OUR CLIENTS"
    }
  },
  {
    "path": "imgs/066062096e4813caeaaadd31dd341e86.webp",
    "context": {
      "refs": [
        {
          "alt": "Conferenceroom",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0997570f4edb60292d83b72cdec47fb8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Conference Room",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0fa43bef54a63ce2775951b087ea51f6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Security Solutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25a279afec4dc43beb05163411ce2e74.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b11ce3f20c0b19ce4927543b107b4b7.webp",
    "context": {
      "refs": [
        {
          "alt": "Corporate & Government",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2c640e4838c8dc3456d897b6ef024003.webp",
    "context": {
      "refs": [
        {
          "alt": "Craft Solutions and present",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2e76be5a1f49399b6f028e8ec6f9a748.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "CCTV Surveillance",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/308942c31e0966cd0e505a8ed1929646.webp",
    "context": {
      "refs": [
        {
          "alt": "RadioCom",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/354ebb4c792ca2bcdd58cb6f422f37a4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Crestron UC",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3805b640614ba2b867fe26e750ecf2d7.webp",
    "context": {
      "refs": [
        {
          "alt": "AirportKIosk",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3be2c160b0303620aa476d4a293caddc.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3e828ef981a2a4ad74224b1db53071f6.webp",
    "context": {
      "refs": [
        {
          "alt": "Auto Annoucement Software",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/40d896459d26ecee72373d034e7df49c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Kiosk",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4127a5f97cff2ac9028f0dcfe960e690.webp",
    "context": {
      "refs": [
        {
          "alt": "Smart Signage",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4199fe32c9f4ddc7d0e484260b8b1ff1.webp",
    "context": {
      "refs": [
        {
          "alt": "What we do",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/429175aacfc87f4a01fc2b3cc3117344.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Digital Signage Software",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/489bc0fec654836f96b39c6e4e1a6d6f.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Solutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4a096dbd1c52fa18caf2cc8dec71d9c0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Training and Development",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/544b96344a39e74801793f095278cd2a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Smart Retails",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5a65e464ae14608bf5b217019ca383e6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Auto Announcement Software",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5a89c44596312484e4476d84f92ad3a2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Digital Signage Solution",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b4aa5138cbf7070ae20930f8573b967.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Smart Classes",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5bcaeb74b55be9956e8414e68352489b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6008dacdc09ed9881c2b770b9d41e499.webp",
    "context": {
      "refs": [
        {
          "alt": "Meeting & understand requirements",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/635eecc5a3d7681ed41c4f9e50b76762.webp",
    "context": {
      "refs": [
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
    "path": "imgs/6d65b5b96228a7412ab7fe5413c25ba2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Smart Signage",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7de848cb0bb05799a90d46ef58065e65.webp",
    "context": {
      "refs": [
        {
          "alt": "Radios Comm",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8c8ae93cdab368baf95dd9fc3c766cce.webp",
    "context": {
      "refs": [
        {
          "alt": "About the Company",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8de801d5bfa19b65e418ee2442661027.webp",
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
    "path": "imgs/90ac5ba3ccd3bf59b7b27f7ad5b74c77.webp",
    "context": {
      "refs": [
        {
          "alt": "Smart Conference and Meeting Room",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/944b059dd58bf61ba68090ff65974b24.webp",
    "context": {
      "refs": [
        {
          "alt": "CrestronUC",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/95a0a2bee177197d36b5079a623c6bf7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "EPOSE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9a18913f80a7533bb931b31cf251294e.webp",
    "context": {
      "refs": [
        {
          "alt": "Airlines and Airport",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ccb03e8a3a6f476781b11aaaedfe3bf.webp",
    "context": {
      "refs": [
        {
          "alt": "Singage",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9f90d0943bdba95175d25f5fd51c862f.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a052e55b34dffdf07ce920c43c2e9824.webp",
    "context": {
      "refs": [
        {
          "alt": "Identify Technologies",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a7e52012c1b65539c989387ae6030292.webp",
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
        }
      ]
    }
  },
  {
    "path": "imgs/a8ec2c4ef9877fb7db811396a4995137.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Meeting Room",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b3be1571e7aafdf4540e98d4c1b94735.webp",
    "context": {
      "refs": [
        {
          "alt": "PassengerInformationDisplayystem",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b7d7a4d38eb4185d76f7d79aa60f75bf.webp",
    "context": {
      "refs": [
        {
          "alt": "Solutions",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b8dcd1cc7459e142f52cf511309995b3.webp",
    "context": {
      "refs": [
        {
          "alt": "Network and Security",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ba39cebf26c6e5b01afae074d1be9d84.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "PA System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bfd428e7418f3ae7af8b01ee4fb9eae4.webp",
    "context": {
      "refs": [
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
    "path": "imgs/c4d670ecc4f43b7f3dc5f73601df4c60.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Network and Security",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c8639d2c67fb9bfff7a9d91ffb072cd1.webp",
    "context": {
      "refs": [
        {
          "alt": "Digital Signage Software",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cb70b6f45e66289d2b8e20040b853201.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Smart Conference and Meeting Room",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cdfab1f0eebe8626c22bae136ec0bf29.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Singage",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d9441ac50bdc2c36753dd1c14db93bf3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "PA System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eda829404e58aa4dbc70640320af988b.webp",
    "context": {
      "refs": [
        {
          "alt": "Retail and entertainment",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/edd037c8874b914dd84c93ff079a255b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/ef73d0c9bfc6b4db3adf9b57245108df.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Smart Classes",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f6ac042181f0fdff9aa4b25966e415be.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Ordering System",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f6e91d86669e6b4160224e5854651d6d.webp",
    "context": {
      "refs": [
        {
          "alt": "Service Offerings",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/faa6e77688510dfcde91dbf1212effd1.webp",
    "context": {
      "refs": [
        {
          "alt": "Hospital & Hospitality",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fad4a35dc2cd865c977fee3260da7cab.webp",
    "context": {
      "refs": [
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
    "path": "imgs/fbb32a6481c9d49a95cf3ca44cbe81b2.webp",
    "context": {
      "refs": [
        {
          "alt": "Media and Education",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fe96c35a90e6afcd81be5b6a638f0b27.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Airport Kiosk",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Tycnodot Business Solutions | Home",
      "first_heading": "Tycnodot Business Solutions"
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
    "path": "js/6aff2de7d2be92b79c0f49468bc5f7f9.js",
    "context": {
      "path": "js/6aff2de7d2be92b79c0f49468bc5f7f9.js"
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
    "path": "our-solutions-copy.html",
    "context": {
      "title": "Tycnodot Business Solutions | Our Solutions",
      "first_heading": "OUR SOLUTIONS"
    }
  },
  {
    "path": "our-solutions.html",
    "context": {
      "title": "Tycnodot Business Solutions | Our Solution",
      "first_heading": "SOLUTION OFFERING"
    }
  },
  {
    "path": "service-offerings.html",
    "context": {
      "title": "Tycnodot Business Solutions | Delivery Model",
      "first_heading": "DELIVERY MODEL"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.