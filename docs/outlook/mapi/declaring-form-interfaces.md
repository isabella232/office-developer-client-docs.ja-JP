---
title: フォームインターフェイスの宣言
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0fa742b7ff6d98e3a0f475accbc440d22eac0919
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337059"
---
# <a name="declaring-form-interfaces"></a>フォームインターフェイスの宣言

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI_ _ interface__ メソッドマクロを使用することにより、MAPI フォームインターフェイスの実装の宣言を簡略化できます。この_インターフェイス_は、Mapiform ヘッダーファイルで定義されているフォームインターフェイスです。 これらのマクロを使用する必要はありませんが、指定しない場合は、宣言が Mapiform ヘッダーファイルの宣言に準拠していることに特に注意する必要があります。 たとえば、フォームサーバーの form オブジェクトクラスを次のように宣言できます。 
  
```cpp
class CMyForm : public IPersistMessage, public IMAPIForm,
                public IMAPIFormAdviseSink
{
public:
    CMyForm(CClassFactory *);    // constructorr takes a class factory object
    ~CMyForm(void);
// MAPI methods that need to be implemented.
    MAPI_IUNKNOWN_METHODS(IMPL);
    MAPI_GETLASTERROR_METHOD(IMPL);
    MAPI_IPERSISTMESSAGE_METHODS(IMPL);
    MAPI_IMAPIFORM_METHODS(IMPL);
    MAPI_IMAPIFORMADVISESINK_METHODS(IMPL);
// Add other implementation specific items.
};

```

## <a name="see-also"></a>関連項目



[フォームサーバーコードの記述](writing-form-server-code.md)

