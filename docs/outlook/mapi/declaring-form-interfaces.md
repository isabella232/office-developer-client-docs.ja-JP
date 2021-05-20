---
title: フォーム インターフェイスの宣言
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0fa742b7ff6d98e3a0f475accbc440d22eac0919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437512"
---
# <a name="declaring-form-interfaces"></a>フォーム インターフェイスの宣言

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapiform.h ヘッダー ファイルで定義されているフォーム インターフェイスである MAPI_ _interface__METHOD マクロを使用すると、MAPIフォーム インターフェイスの実装の宣言を簡略化できます。 これらのマクロを使用する必要はありません。ただし、使用しない場合は、宣言が Mapiform.h ヘッダー ファイルの宣言に準拠している場合は特に注意する必要があります。 たとえば、フォーム サーバーのフォーム オブジェクト クラスを次のように宣言できます。 
  
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



[フォーム サーバー コードの作成](writing-form-server-code.md)

