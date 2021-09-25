---
title: メッセージ全体をダウンロードすることなく IMAP ストア上のメッセージにアクセスする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 61e81b2b078718bdb7d11d3dc5f99e192077eaa9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551451"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>メッセージ全体をダウンロードすることなく IMAP ストア上のメッセージにアクセスする

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、C++ のコード サンプルを示し **[、IProxyStoreObject](iproxystoreobject.md)** インターフェイスのメッセージ ストアを照会し、返されたポインターと **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** 関数を使用して、ラップされていない IMAP ストア オブジェクトへのポインターを取得します。 このラップされていないストアを使用すると、メッセージ全体のダウンロードを呼び出さずに、現在の状態のメッセージにアクセスできます。 
  
**UnwrapNoRef** はアンラップされたストア オブジェクトへのこの新しいポインターの参照カウントをインクリメントしないので **、UnwrapNoRef** を正常に呼び出した後、参照カウントを維持するために [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)を呼び出す必要があります。 
  
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


