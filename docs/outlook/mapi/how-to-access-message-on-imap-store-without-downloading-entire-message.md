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
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>メッセージ全体をダウンロードすることなく IMAP ストア上のメッセージにアクセスする

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、 **[iproxystoreobject](iproxystoreobject.md)** インターフェイスのメッセージストアに対してクエリを実行する C++ のコードサンプルを示し、返されたポインターと**[iproxystoreobject:: UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** 関数を使用して、IMAP ストアオブジェクトへのポインターを取得します。解除. このラップされていないストアを使用すると、メッセージ全体のダウンロードを呼び出すことなく、現在の状態のメッセージにアクセスできます。 
  
**UnwrapNoRef**は、ラップされていない store オブジェクトへのこの新しいポインターの参照カウントをインクリメントしないため、 **UnwrapNoRef**の呼び出しに成功した後で、 [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)を呼び出して参照カウントを維持する必要があります。 
  
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


