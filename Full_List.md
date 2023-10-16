---
publish: true
---

# Toogle

- [t_1:on] this is a toggle `on`

- [t_2:off] this is a toggle `off`

  

# TextField

- [t_3] textfield inferred

- [t_4:number] textfield with numberpad

- [t_5:email] textfield with email

- [t_51:textArea:This is my value content] TextArea

  

# Pickers

Pickers are a different bunch

- [t_6:segmented:option 1/option 2:option 2] Segmented picker

- [t_7:option 3/option 4] dropdown inferred

- [t_8:dropDown:option 5/option 6] dropdown

- [t_9:@date] Date picker

- [t_10:@time] Date and Time Picker

 //NOT IMPLEMENTED -[t_11:@location] Location picker(?!)

```t_12:binding
context.t_1_Bool ? "The first toggle is On" : "The first toggle is Off"
```

```default:action
{

    appendToDailyFormat : "YYYY-MM"

}
```

```output:template
# Toogle

- {{t_1}} this is a toggle `on`

- {{t_2}} this is a toggle `off`

  

# TextField

- {{t_3}} textfield inferred

- {{t_4}} textfield with numberpad

- {{t_5}} textfield with email

- {{t_51}} TextArea

  

# Pickers

Pickers are a different bunch

- {{t_6}} Segmented picker

- {{t_7}} dropdown inferred

- {{t_8}} dropdown

- {{t_9}} Date picker

- {{t_10}} Date and Time Picker

# Binding
- {{t_12}} (should reflect toggle 1)
```