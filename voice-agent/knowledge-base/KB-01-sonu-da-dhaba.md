# KB-01: The Golden Spoon

> **GHL Location:** AI Agents â†’ Knowledge Base â†’ + Create Knowledge Base â†’ Name: "KB-01: The Golden Spoon"
> **Attach to:** All Voice AI agents (VA-01 English, VA-02 Hindi, VA-03 Punjabi). Voice AI allows 1 KB â€” this is it.
> **Structure:** This KB uses 3 source types. Set them up in order: Rich Text â†’ CSV Table â†’ FAQ.

---

## SOURCE 1 â€” RICH TEXT: Restaurant Info & Policies

> GHL â†’ KB-01 â†’ + Add Source â†’ Rich Text
> Two sections: one for restaurant info, one for policies.

---

### Rich Text Section 1 of 2: Restaurant Info

**Name:** The Golden Spoon
**Cuisine:** Authentic Punjabi / North Indian
**Hours:** Monday to Sunday, 11:00 AM to 11:00 PM â€” open 7 days a week
**Order Types:** Takeout and Delivery
**Address:** {{custom_values.address}}
**Phone:** {{custom_values.main_phone}}

---

### Rich Text Section 2 of 2: Policies

**Delivery:** We offer both takeout and delivery.

**Spice level:** Customers can request mild, medium, or spicy for all curries, karahi, and masala dishes.

**Allergies:** For allergy questions, always let the team know when collecting the order â€” the kitchen advises directly. Never confirm food safety over the phone.

**Halal:** Callers asking about halal certification should be directed to call the restaurant directly.

**Gluten-free:** Many rice dishes and curries are naturally gluten-free. For specific allergy needs, defer to the kitchen.

**Timing:** Never estimate delivery or wait times â€” the kitchen handles this.

---

## SOURCE 2 â€” CSV TABLE: Menu

> GHL â†’ KB-01 â†’ + Add Source â†’ Tables
> Upload the CSV file below (save as `sonu-da-dhaba-menu.csv`, UTF-8 encoding).
> Indexing takes a few minutes after upload.
> Column headers are on row 1. Do not modify header names.

---

### CSV File Content

```csv
Category,Item,Price,Description,Veg
Starters,Samosa (2 pcs),$6.99,Crispy pastry filled with spiced potato and peas. Served with mint chutney.,Yes
Starters,Aloo Tikki (2 pcs),$7.99,Pan-fried spiced potato patties. Served with tamarind and mint chutney.,Yes
Starters,Onion Pakora,$8.99,Crispy fried onion fritters in a spiced chickpea batter. Also called Pyaaz Pakora.,Yes
Starters,Paneer Tikka,$14.99,Cubes of cottage cheese marinated in spiced yogurt cooked in tandoor. Vegetarian.,Yes
Starters,Chicken Tikka,$15.99,Boneless chicken marinated in tandoori masala cooked in tandoor.,No
Starters,Seekh Kebab (4 pcs),$15.99,Minced lamb mixed with herbs and spices grilled on skewers.,No
Starters,Amritsari Fish Fry,$16.99,Crispy battered fish seasoned with Amritsari spices.,No
Starters,Papdi Chaat,$9.99,Crispy wafers topped with yogurt tamarind chutney sev and spices. Vegetarian.,Yes
Starters,Golgappa / Pani Puri (6 pcs),$8.99,Crispy hollow puris filled with spiced water potato and chickpeas. Also called Pani Puri. Vegetarian.,Yes
Breads,Tandoori Roti,$2.49,Whole wheat flatbread baked in tandoor.,Yes
Breads,Butter Roti,$2.99,Tandoori roti brushed with butter.,Yes
Breads,Plain Naan,$2.99,Leavened white flour bread from tandoor.,Yes
Breads,Butter Naan,$3.49,Plain naan brushed with butter.,Yes
Breads,Garlic Naan,$3.99,Naan topped with garlic and butter.,Yes
Breads,Cheese Naan,$4.49,Naan stuffed with melted cheese.,Yes
Breads,Kulcha,$3.99,Soft leavened bread slightly crispy outside.,Yes
Breads,Puri (2 pcs),$3.99,Deep-fried whole wheat puffed bread.,Yes
Breads,Bhatura (1 pc),$3.49,Large deep-fried leavened bread. Traditionally paired with Chana Masala.,Yes
Breads,Plain Paratha,$3.49,Whole wheat layered flatbread pan-fried.,Yes
Breads,Aloo Paratha,$5.99,Paratha stuffed with spiced mashed potato.,Yes
Breads,Gobi Paratha,$5.99,Paratha stuffed with spiced cauliflower.,Yes
Breads,Paneer Paratha,$6.49,Paratha stuffed with spiced cottage cheese.,Yes
Breads,Onion Paratha,$5.49,Paratha stuffed with spiced onion. Also called Pyaaz Paratha.,Yes
Breads,Makki di Roti,$3.49,Cornflour flatbread. Traditional pair with Sarson da Saag.,Yes
Dal,Dal Makhani,$13.99,Slow-cooked black lentils and kidney beans in a rich buttery tomato cream sauce. Vegetarian.,Yes
Dal,Dal Tadka,$12.99,Yellow lentils tempered with garlic cumin and dried red chilies. Vegetarian.,Yes
Dal,Chana Masala,$12.99,Chickpeas cooked in a tangy onion-tomato masala. Vegetarian.,Yes
Dal,Rajma,$12.99,Red kidney beans slow-cooked in thick onion-tomato gravy. Vegetarian.,Yes
Dal,Kali Dal,$13.99,Whole black lentils cooked overnight on slow flame. Rich and smoky. Vegetarian.,Yes
Paneer,Paneer Butter Masala,$15.99,Cottage cheese in rich creamy tomato-butter sauce. Also called Paneer Makhani. Vegetarian.,Yes
Paneer,Palak Paneer,$15.99,Cottage cheese in a smooth spiced spinach gravy. Vegetarian.,Yes
Paneer,Kadai Paneer,$15.99,Paneer cooked with capsicum and onions in kadai masala. Vegetarian.,Yes
Paneer,Shahi Paneer,$16.49,Paneer in a rich cashew and cream sauce. Royal preparation. Vegetarian.,Yes
Paneer,Paneer Do Pyaza,$15.99,Paneer with double onion in aromatic masala. Vegetarian.,Yes
Paneer,Matar Paneer,$14.99,Cottage cheese and green peas in tomato-onion gravy. Vegetarian.,Yes
Chicken,Butter Chicken,$16.99,Tandoori chicken in smooth mildly spiced tomato butter sauce. Also called Murgh Makhani.,No
Chicken,Chicken Tikka Masala,$16.99,Grilled chicken in richly spiced tomato-cream masala.,No
Chicken,Kadai Chicken,$16.99,Chicken with bell peppers tomatoes and kadai masala.,No
Chicken,Chicken Do Pyaza,$16.49,Chicken with double onion in dry aromatic masala.,No
Chicken,Chicken Rogan Josh,$16.99,Slow-cooked chicken in Kashmiri-style red masala.,No
Chicken,Chicken Karahi,$17.49,Dry-style chicken with tomatoes ginger green chili in karahi.,No
Chicken,Tandoori Chicken Half,$14.99,Chicken marinated in tandoori masala cooked in tandoor. Half portion.,No
Chicken,Tandoori Chicken Full,$27.99,Full chicken marinated and tandoor-cooked.,No
Chicken,Chicken Keema,$15.99,Minced chicken cooked with peas onion and spices.,No
Mutton,Mutton Rogan Josh,$19.99,Tender mutton slow-cooked in Kashmiri aromatic red gravy.,No
Mutton,Mutton Karahi,$20.99,Dry-style mutton with tomatoes ginger green chili in karahi.,No
Mutton,Mutton Keema,$18.99,Minced mutton cooked with peas onion and spices.,No
Mutton,Mutton Korma,$20.49,Slow-cooked mutton in mild rich yogurt and cashew sauce.,No
Mutton,Bhuna Gosht,$20.49,Mutton slow-cooked in thick dry masala until very tender.,No
Vegetarian Mains,Aloo Gobi,$12.99,Dry potato and cauliflower with cumin and spices. Vegetarian.,Yes
Vegetarian Mains,Aloo Matar,$12.99,Potato and green peas in a light tomato gravy. Vegetarian.,Yes
Vegetarian Mains,Bhindi Masala,$12.99,Okra stir-fried with onions tomatoes and spices. Vegetarian.,Yes
Vegetarian Mains,Baingan Bharta,$13.49,Roasted mashed eggplant cooked with onion tomato and spices. Vegetarian.,Yes
Vegetarian Mains,Mixed Veg,$13.99,Seasonal vegetables in a light masala. Vegetarian.,Yes
Vegetarian Mains,Sarson da Saag,$13.99,Classic Punjabi mustard greens. Seasonal dish. Traditionally paired with Makki di Roti. Vegetarian.,Yes
Biryani & Rice,Chicken Biryani,$17.99,Aromatic basmati rice slow-cooked with spiced chicken. Served with raita.,No
Biryani & Rice,Mutton Biryani,$20.99,Aromatic basmati rice slow-cooked with tender mutton. Served with raita.,No
Biryani & Rice,Veg Biryani,$15.99,Fragrant basmati rice with mixed vegetables and whole spices. Served with raita. Vegetarian.,Yes
Biryani & Rice,Jeera Rice,$5.99,Basmati rice tempered with cumin. Light side dish. Vegetarian.,Yes
Biryani & Rice,Plain Rice,$4.99,Simple steamed basmati rice. Also called Steamed Rice. Vegetarian.,Yes
Sides,Raita,$3.49,Chilled yogurt with cucumber and spices. Great with biryani. Vegetarian.,Yes
Sides,Boondi Raita,$3.99,Yogurt with crispy boondi balls. Vegetarian.,Yes
Sides,Papad (2 pcs),$2.49,Crispy lentil crackers. Vegetarian.,Yes
Sides,Green Salad,$4.99,Sliced cucumber tomato onion and lemon. Vegetarian.,Yes
Sides,Onion Salad with Lemon,$2.99,Sliced raw onion with lemon and chili. Vegetarian.,Yes
Sides,Mango Pickle,$1.99,Spicy mango pickle. Also called Aam ka Achar. Vegetarian.,Yes
Sides,Mixed Pickle,$1.99,Assorted vegetable pickle. Vegetarian.,Yes
Sides,Ghee (extra),$1.49,Clarified butter. Add to any bread or dal for extra richness. Vegetarian.,Yes
Sides,Butter (extra),$0.99,Extra butter for breads. Vegetarian.,Yes
Drinks,Sweet Lassi,$5.99,Chilled yogurt drink sweetened. Vegetarian.,Yes
Drinks,Salted Lassi,$5.49,Chilled yogurt drink with salt and cumin. Vegetarian.,Yes
Drinks,Mango Lassi,$6.49,Chilled yogurt blended with mango pulp. Vegetarian.,Yes
Drinks,Masala Chai,$3.49,Spiced Indian milk tea. Vegetarian.,Yes
Drinks,Nimbu Pani,$3.99,Fresh lemonade with salt cumin and mint. Vegetarian.,Yes
Drinks,Coca-Cola,$2.99,Chilled soft drink. Vegetarian.,Yes
Drinks,Sprite,$2.99,Chilled soft drink. Vegetarian.,Yes
Drinks,Fanta Orange,$2.99,Chilled orange flavored soft drink. Vegetarian.,Yes
Drinks,Water (bottle),$1.99,Bottled water. Vegetarian.,Yes
Desserts,Gulab Jamun (2 pcs),$5.99,Soft milk-solid balls soaked in rose-flavored sugar syrup. Vegetarian.,Yes
Desserts,Kheer,$5.49,Slow-cooked rice pudding with cardamom saffron and nuts. Vegetarian.,Yes
Desserts,Gajar ka Halwa,$5.99,Slow-cooked carrot pudding with ghee milk and cardamom. Seasonal. Vegetarian.,Yes
Desserts,Kulfi (stick),$4.99,Traditional dense Indian ice cream. Flavors: Mango Pistachio Rose. Vegetarian.,Yes
Desserts,Ras Malai (2 pcs),$6.49,Soft cottage cheese dumplings in sweet saffron-flavored milk. Vegetarian.,Yes
```

> **Upload instructions:**
> 1. Copy the CSV content above into a text editor
> 2. Save as `sonu-da-dhaba-menu.csv` with UTF-8 encoding
> 3. GHL â†’ KB-01 â†’ + Add Source â†’ Tables â†’ upload the file
> 4. After indexing, click View All â†’ confirm rows loaded â†’ click Train Bot

> **Scaling rule:** To add new items, add rows to the CSV and re-upload. To add a new category, just use a new Category name â€” no restructuring needed.

---

## SOURCE 3 â€” FAQ: Exact-Match Q&A

> GHL â†’ KB-01 â†’ + Add Source â†’ FAQ
> Add each Q&A pair as a separate FAQ entry.
> FAQ entries give exact, reliable responses â€” use this for high-stakes questions.

---

**Q: Do you offer delivery?**
A: Yes, we offer both takeout and delivery.

**Q: What are your hours?**
A: We are open 7 days a week from 11:00 AM to 11:00 PM.

**Q: Are you open today?**
A: Yes, we are open every day from 11:00 AM to 11:00 PM.

**Q: Do you have vegetarian options?**
A: Yes â€” all our dals, most vegetable dishes, paneer dishes, and breads are vegetarian. Just ask and I can suggest some.

**Q: Is your food halal?**
A: For halal certification details, please call us directly â€” the team can confirm.

**Q: Do you have gluten-free options?**
A: Many of our rice dishes and curries are naturally gluten-free. For allergy needs, let the team know when you collect and the kitchen can advise directly.

**Q: Can I customize the spice level?**
A: Yes â€” for all curries, karahi, and masala dishes you can request mild, medium, or spicy.

**Q: What is Sarson da Saag?**
A: Sarson da Saag is a classic Punjabi dish made from mustard greens, traditionally served with Makki di Roti â€” that's cornflour bread. It's a seasonal specialty.

**Q: What is Dal Makhani?**
A: Dal Makhani is slow-cooked black lentils and kidney beans in a rich buttery tomato cream sauce â€” one of our most popular dishes.

**Q: What is Butter Chicken?**
A: Butter Chicken, also called Murgh Makhani, is tandoori chicken in a smooth mildly spiced tomato and butter sauce. It's mild and creamy.

**Q: What bread goes with Dal Makhani?**
A: Dal Makhani goes great with Butter Naan, Garlic Naan, or Tandoori Roti.

**Q: What is Kulfi?**
A: Kulfi is a traditional dense Indian ice cream on a stick â€” richer and creamier than regular ice cream. We have Mango, Pistachio, and Rose flavors.

**Q: What is Ghee?**
A: Ghee is clarified butter â€” a staple in Indian cooking. You can add it to any bread or dal for extra richness.

**Q: What is Bhatura?**
A: Bhatura is a large deep-fried leavened bread. It's traditionally served with Chana Masala â€” a popular combo.

**Q: What is Raita?**
A: Raita is a chilled yogurt dish with cucumber and spices â€” great alongside biryani or spicy curries to balance the heat.

**Q: What goes well with Makki di Roti?**
A: Makki di Roti is traditionally paired with Sarson da Saag â€” that's our Punjabi mustard greens. It's a seasonal classic.

**Q: What is Paneer?**
A: Paneer is Indian cottage cheese â€” fresh, mild, and used in many of our vegetarian dishes like Paneer Butter Masala, Palak Paneer, and Paneer Tikka.

**Q: What is the difference between Paneer Butter Masala and Butter Chicken?**
A: Same sauce base â€” rich tomato and butter â€” but Paneer Butter Masala uses cottage cheese and is vegetarian, while Butter Chicken uses tandoori chicken.

**Q: Do you have a kids menu?**
A: We don't have a separate kids menu, but mild options like Butter Chicken, Paneer Butter Masala, plain rice, and breads are popular with kids.

**Q: What is Chana Masala?**
A: Chana Masala is chickpeas cooked in a tangy onion-tomato masala â€” it's vegetarian and goes great with Bhatura or rice.

---

## Maintenance Notes

> These are internal notes â€” not entered into GHL.

- **Adding menu items:** Add rows to the CSV, re-upload under Tables. No Rich Text changes needed.
- **Price changes:** Update the CSV row and re-upload. The FAQ and Rich Text sections are unaffected.
- **New FAQ:** Add a new FAQ entry in GHL directly â€” no file changes needed.
- **Seasonal items (e.g., Sarson da Saag, Gajar ka Halwa):** Mark active/inactive in the CSV by removing or adding rows. No restructuring needed.
- **If menu grows to 150+ items:** Same CSV structure still works â€” add rows and re-upload. No other changes.
