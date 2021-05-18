---
title: メッセージ全体をダウンロードすることなく IMAP ストア上のメッセージにアクセスする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 194131148cc36dfff791b4cfae01862e8bbef5cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299077"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a><span data-ttu-id="54469-103">メッセージ全体をダウンロードすることなく IMAP ストア上のメッセージにアクセスする</span><span class="sxs-lookup"><span data-stu-id="54469-103">Access a message on an IMAP store without downloading the entire message</span></span>

<span data-ttu-id="54469-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54469-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54469-105">このトピックでは、C++ のコード サンプルを示し **[、IProxyStoreObject](iproxystoreobject.md)** インターフェイスのメッセージ ストアを照会し、返されたポインターと **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** 関数を使用して、ラップされていない IMAP ストア オブジェクトへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="54469-105">This topic shows a code sample in C++ that queries a message store for the **[IProxyStoreObject](iproxystoreobject.md)** interface, and uses the returned pointer and the **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** function to obtain a pointer to an IMAP store object that has been unwrapped.</span></span> <span data-ttu-id="54469-106">このラップされていないストアを使用すると、メッセージ全体のダウンロードを呼び出さずに、現在の状態のメッセージにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="54469-106">Using this unwrapped store allows access to a message in its current state without invoking a download of the entire message.</span></span> 
  
<span data-ttu-id="54469-107">**UnwrapNoRef** はアンラップされたストア オブジェクトへのこの新しいポインターの参照カウントをインクリメントしないので **、UnwrapNoRef** を正常に呼び出した後、参照カウントを維持するために [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="54469-107">Because **UnwrapNoRef** does not increment the reference count for this new pointer to the unwrapped store object, after successfully calling **UnwrapNoRef**, you must call [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) to maintain the reference count.</span></span> 
  
```cpp
HRESULT HrUnWrapMDB(LPMDB lpMDBIn, LPMDB* lppMDBOut) 
{ 
    HRESULT hRes = S_OK; 
    IProxyStoreObject* lpProxyObj = NULL; 
    LPMDB lpUnwrappedMDB = NULL; 
    hRes = lpMDBIn->QueryInterface(IID_IProxyStoreObject,(void**)&lpProxyObj); 
    if (SUCCEEDED(hRes) && lpProxyObj) 
    { 
        hRes = lpProxyObj->UnwrapNoRef((LPVOID*)&lpUnwrappedMDB); 
        if (SUCCEEDED(hRes) && lpUnwrappedMDB) 
        { 
            // UnwrapNoRef doesn't addref, so do it here 
            lpUnwrappedMDB->AddRef(); 
            (*lppMDBOut) = lpUnwrappedMDB; 
        } 
    } 
    if (lpProxyObj) lpProxyObj->Release(); 
    return hRes; 
}
```


