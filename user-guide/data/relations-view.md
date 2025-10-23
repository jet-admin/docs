---
description: Link tables together to display related data without switching between views
---

# Relations View

The Relations View in JetAdmin helps you understand how your data is connected. Easily link tables using foreign key fields and explore related records without switching tabs.

#### Steps

1. **Add a relation field:** Open your table (for example, _Tickets_) and click **Add Field → link to record**.
2. **Choose the related table:** In the setup, select _Users_ as the table you want to connect to.
3. **Pick the linking field:** Choose the field from _Users_ (like `User ID`) that uniquely identifies each record.
4. **Link records:** In your _Tickets_ table, fill the new relation column with the correct _User ID_. Each ticket will now be linked to a user.
5. **View related data:** Click the linked user inside the cell to view that user’s details directly, no need to open the _Users_ table separately.

{% @arcade/embed flowId="do6hXU4Yfp1dY0unnPLV" url="https://app.arcade.software/share/do6hXU4Yfp1dY0unnPLV" %}



