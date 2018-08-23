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
ms.openlocfilehash: 4687b07c89d866acbe3b6a8f4cde3262657a06b5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584248"
---
# <a name="declaring-form-interfaces"></a><span data-ttu-id="42a36-103">フォーム インターフェイスの宣言</span><span class="sxs-lookup"><span data-stu-id="42a36-103">Declaring Form Interfaces</span></span>

  
  
<span data-ttu-id="42a36-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42a36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42a36-105">MAPI フォームのインターフェイスの実装の宣言は、マクロを使用して、MAPI_ _interface__METHOD、Mapiform.h ヘッダー ファイルで定義されているフォームのインタ フェースの_インタ フェース_が簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="42a36-105">You can simplify the declarations of your implementations of MAPI form interfaces by using the MAPI_ _interface__METHOD macros, where  _interface_ is a form interface defined in the Mapiform.h header file.</span></span> <span data-ttu-id="42a36-106">これらのマクロを使用する必要はありませんが、宣言は、Mapiform.h ヘッダー ファイル内の宣言に準拠している特定の注意を行う必要がない場合は。</span><span class="sxs-lookup"><span data-stu-id="42a36-106">You are not required to use these macros, but if you do not, you should take particular care that your declarations conform to the declarations in the Mapiform.h header file.</span></span> <span data-ttu-id="42a36-107">たとえば、次のように、フォームのサーバーのフォーム オブジェクトのクラスを宣言できます。</span><span class="sxs-lookup"><span data-stu-id="42a36-107">For example, you could declare your form server's form object class like the following:</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="42a36-108">関連項目</span><span class="sxs-lookup"><span data-stu-id="42a36-108">See also</span></span>



[<span data-ttu-id="42a36-109">フォーム サーバー コードの記述</span><span class="sxs-lookup"><span data-stu-id="42a36-109">Writing Form Server Code</span></span>](writing-form-server-code.md)

