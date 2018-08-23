---
title: フォーム インターフェイスの宣言
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79283301-e544-4a4d-96c2-3f81dc5b3731
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8f4d8842efbba2f1f2b7281e5d4741b89f975b3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799880"
---
# <a name="declaring-form-interfaces"></a>フォーム インターフェイスの宣言

  
  
**適用対象**: Outlook 
  
MAPI フォームのインターフェイスの実装の宣言は、マクロを使用して、MAPI_ _interface__METHOD、Mapiform.h ヘッダー ファイルで定義されているフォームのインタ フェースの_インタ フェース_が簡略化できます。 これらのマクロを使用する必要はありませんが、宣言は、Mapiform.h ヘッダー ファイル内の宣言に準拠している特定の注意を行う必要がない場合は。 たとえば、次のように、フォームのサーバーのフォーム オブジェクトのクラスを宣言できます。 
  
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



[フォーム サーバー コードの記述](writing-form-server-code.md)

