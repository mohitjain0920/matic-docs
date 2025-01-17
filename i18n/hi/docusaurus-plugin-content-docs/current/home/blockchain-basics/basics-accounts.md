---
id: accounts
title: अकाउंट क्या हैं?
sidebar_label: Accounts
description: "EOAs और अनुबंध अकाउंट."
keywords:
  - docs
  - matic
  - polygon
  - accounts
  - EOAs
  - contract accounts
image: https://wiki.polygon.technology/img/polygon-wiki.png
---

# अकाउंट क्या हैं? {#what-are-accounts}

एथेरेयम की ग्लोबल स्टेट में ऐसे अकाउंट शामिल हैं जो एक मैसेज पास करने वाले फ़्रेमवर्क के माध्यम से एक दूसरे से इंटरैक्ट करते हैं. सबसे बुनियादी बातचीत यह है कि कुछ वैल्यू - जैसे मैटिक टोकन्स, पॉलीगॉन का मूल टोकन या ${ ET, जो Ethereum ब्लॉकचेन का मूल टोकन भेजने का है.

हर अकाउंट की पहचान 20 बाइट हेक्स पहचानकर्ता द्वारा की जाती है जिसे पता कहा जाता है - जो अकाउंट की सार्वजनिक की से उत्पन्न होता है.

अकाउंट दो प्रकार के होते हैं: **बाहरी स्वामित्व वाले अकाउंट**और **अनुबंध स्वामित्व वाले अकाउंट**.

## बाहरी स्वामित्व वाले अकाउंट {#externally-owned-accounts}

EOA वे अकाउंट होते हैं जिन्हें निजी कुंजी द्वारा नियंत्रित किया जाता है, जिनमें टोकन और संदेश भेजने की क्षमता होती है.

1. वे ट्रांजैक्शन भेज सकते हैं (ईथर ट्रांसफर या ट्रिगर अनुबंध कोड),
2. उन्हें निजी कुंजियों द्वारा नियंत्रित किया जाता है,
3. और उनसे कोई कोड नहीं जुड़ा होता.

## अनुबंध स्वामित्व वाले अकाउंट {#contract-owned-accounts}
अनुबंध स्वामित्व वाले अकाउंट वे अकाउंट हैं जिनके साथ एक स्मार्ट अनुबंध कोड जुड़ा होता है और जिनकी निजी की कुंजी किसी के पास नहीं होती है.

1. उनसे कोड जुड़ा होता है,
2. उनका कोड एग्जीक्यूशन अन्य अनुबंध से प्राप्त ट्रांजैक्शन या संदेशों (कॉल) द्वारा ट्रिगर होता है.
3. और जब कोड निष्पादित किया जाता है - यह मनमानी जटिलता (ट्यूरिंग संपूर्णता क्षमता) के संचालन करता है - यह अपनी स्वयं की स्थायी स्टोरेज में हेरफेर करता है और यह अन्य अनुबंधों को कॉल कर सकता है.

### संसाधन {#resources}

- [अकाउंट के बारे में और ज़्यादा पढ़ें](https://github.com/ethereum/homestead-guide/blob/master/source/contracts-and-transactions/account-types-gas-and-transactions.rst#externally-owned-accounts-eoas)
