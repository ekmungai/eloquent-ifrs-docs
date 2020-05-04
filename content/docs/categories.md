---
title: 'Categories'
date: 2018-11-28T15:14:39+10:00
weight: 13
---
Categories are a means of grouping together several accounts of the same type. This is useful for further subividing the financial reports apart from the classifications defined by IFRS.

### Attributes
+ `name`: The name of the category 
+ `category_type`: The category type must be one of the account types defined in Account. See Account for more details.
+ `entity_id`: The Id of the entity associated with the category. Defaults to the id of entity of the logged in user.

### Relations
+ `$category->entity:` The entity associated with the category. 
+ `$category->accounts:` Accounts belonging to the category. 

### Methods
+ `$category->attributes():` Presents the category's attributes as an object. Useful for debugging. 

***