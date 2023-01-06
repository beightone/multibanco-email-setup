# Multibanco Email Template

### VTEX Setup

1. Access your admin page
2. Open Message Center below **CUSTOMER**
3. Click on templates
4. Click on the Green Button with **New Template** label
5. Update title located at the top of the page written **New Template** with `Multibanco Payment Information`
6. Select the **Use default sender** option
7. Add a Title for **Email Subject** field
8. Copy and paste `{{recipient}}` on **To:** field
9. Use this [Template](https://raw.githubusercontent.com/beightone/multibanco-email-setup/main/body.html) to begin your customization and paste it on **HTML** Field
10. Use this [JsonData](https://raw.githubusercontent.com/beightone/multibanco-email-setup/main/jsonData.json) to preview your email.

After the setup, it should look like this
![VTEX Email Template](https://github.com/beightone/multibanco-email-setup/blob/main/example.png?raw=true "VTEX Email Template")

### Customizing

You probabily want to customize this HTML Template, for this you can edit it's body section. Use the fields in [JsonData](https://raw.githubusercontent.com/beightone/multibanco-email-setup/main/jsonData.json) to send the correct information to your customer. You should add two brackets before and after the required field, like this: `{{reference}}`

On template you can edit those information on this part:

```
<div>
   <h3 style="margin:0;margin-top:16px">
      Entity
   </h3>
   <p style="margin-top:4px">{{entity}}</p>

   <h3 style="margin:0;margin-top:16px">Reference</h3>
   <p style="margin-top:4px">{{reference}}</p>

   <h3 style="margin:0;margin-top:16px">Value</h3>
   <p style="margin-top:4px">{{value}}</p>

   <h3 style="margin:0;margin-top:16px">
      Expiration Date
   </h3>
   <p style="margin-top:4px">{{expiresAt}}</p>
</div>
```
