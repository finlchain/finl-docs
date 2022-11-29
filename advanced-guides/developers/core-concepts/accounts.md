# Accounts

## Accunt Number

### Creation Rules

Account Number consists of a total of 64 bits and is largely divided into Token Account and User Account.

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption><p>Creation Rules of Account Number</p></figcaption></figure>

**NOTE** : Refer to [ISO3166-1](https://en.wikipedia.org/wiki/ISO\_3166-1) numeric for country codes and subdivision codes. If the subdivision codes of a country are NOT numeric values, then the codes should be mapped to numeric values.

### User Account

User Account settings are largely divided into MSB 32 bits and LSB 32 bits.

In the case of MSB 32 bits, it is divided into values that can determine Token Account and User Account, country code, area code, and random number.

If the MSB 4 bits are between 0x2 and 0x7 for User Account, the next MSB 12 bits are set for each country according to the ISO 3166-1 numeric code, a country code table. The next MSB 8 bits is set as the area code according to the country previously set according to the local numeric code table that maps the ISO 3166-2 code, which is the area code table, to numbers. For the next MSB 8 bits, a random number is used. In this case, the range of the random number is 0x00 or more and OxFF or less.

In the case of LSB 32 bits, it is set to UTC second time.

### Token Account

Token Account settings are largely divided into MSB 32 bits and LSB 32 bits.

In the case of MSB 32 bits, it is divided into values that can determine Token Account and User Account, country code, area code, and random number.

If the MSB 4 bits are between 0x2 and 0x7 for User Account, the next MSB 12 bits are set for each country according to the ISO 3166-1 numeric code, a country code table. The following MSB 8 bits are regional codes according to the country set above according to the local numeric code table that maps the ISO 3166-2 code, which is an area code table, to numbers.

Set to draw In the case of the next MSB 8 bits, it is set to 0x0.

In case of LSB 32 bits, Token Number is set to the value of a platform token or a utility token.

&#x20;
