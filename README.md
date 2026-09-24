<a href="https://hemaxprowash.com/"><img src="media/cover.jpg" alt="Hemax Pro Wash, home page on a laptop and a phone" width="100%"></a>

# Hemax Pro Wash

Web shop for a Leskovac distributor of professional cleaning chemicals, where each pack size is a variant with its own code, price and stock.

**[hemaxprowash.com](https://hemaxprowash.com/)** · [Case study (in Serbian)](https://svilenkovic.com/radovi/hemax-pro-wash) · [Srpski](README.sr.md)

> [!NOTE]
> Client project. The source code belongs to the client and stays in a private repository. This page describes what I built and how.

<table>
  <tr><td><b>Client</b></td><td>Hemax Pro Wash</td></tr>
  <tr><td><b>Industry</b></td><td>Professional chemicals for car washes, carpet cleaners and truck washes</td></tr>
  <tr><td><b>Location</b></td><td>Leskovac, Serbia</td></tr>
  <tr><td><b>Type</b></td><td>Web shop</td></tr>
  <tr><td><b>My role</b></td><td>Design, development, SEO, hosting and maintenance</td></tr>
  <tr><td><b>Stack</b></td><td>PHP 8.3, SQLite, Vanilla JS, WebP/srcset, PWA</td></tr>
</table>

## About the project

Hemax Pro Wash supplies professional chemicals and accessories to self-service and hand car washes, carpet cleaners and truck washes, shipping from Leskovac across Serbia. The same product usually comes in several packs, from a small bottle to a 25 kg canister, and prices change too often to go through code every time. The owner wanted people to order without an account and to edit prices himself.

Pack sizes are variants of one product, each with its own label, code, price, stock flag and fiscal register code. A catalogue card shows a from-price, and the product page switches the price as you pick a size. When one size runs out, only that size is switched off: it shows crossed out, the first available one becomes the default, and the cart refuses it even if someone tries to add it another way.

## What I built

- One-step checkout without registration, cash on delivery or bank transfer; the server recalculates the total, delivery and the free-delivery threshold
- Products in several categories at once, with two drag-and-drop orders: one for the whole catalogue and one inside each category
- A4 invoices printed from the panel, with fiscal register codes frozen at the moment of purchase and the total written out in words
- Original photos left untouched as the client asked, with 320, 640 and 960 px WebP copies in srcset; an 829 KB photo loads in a card as 9 KB
- Cookie-free visit stats in the panel, based on a visitor hash that changes every day, and an evening email with orders, turnover, inquiries and visits
- A product view counter that waits for the SQLite lock and can't break the page; twelve parallel requests used to return five errors, now none

## Results

| | Performance | Accessibility | Best practices | SEO |
| :-- | :-: | :-: | :-: | :-: |
| Mobile | 97 | 100 | 100 | 100 |
| Desktop | 100 | 100 | 100 | 100 |

PageSpeed Insights, lab test of the live site, September 2026. Security headers: 6 of 6. HTML validator: no errors. axe accessibility check: no violations. Structured data: `FAQPage`, `OnlineStore`, `Organization`, `Store`.

## Screenshots

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="Hemax Pro Wash, home page on a 1440 px screen"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="Hemax Pro Wash, home page on a phone"></td>
  </tr>
</table>

<img src="media/inner-1.webp" alt="Categories and popular products on the homepage">
<sub>Categories and popular products on the homepage</sub>

<img src="media/inner-2.webp" alt="Further down the homepage">
<sub>Further down the homepage</sub>

---

<sub>Built by [D. Svilenković](https://svilenkovic.com).</sub>
