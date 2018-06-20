---
title: IMAP ストアにメッセージをメッセージ全体をダウンロードすることがなくアクセスします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2a93ab3e-798f-5741-d5e0-bba8c6b437c7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fa7a61da47169ca7c6a1521ad5b3e84685a9b9a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800238"
---
# <a name="access-a-message-on-an-imap-store-without-downloading-the-entire-message"></a>IMAP ストアにメッセージをメッセージ全体をダウンロードすることがなくアクセスします。

**適用されます**: Outlook 
  
このトピックは、 **[IProxyStoreObject](iproxystoreobject.md)** インターフェイスでは、メッセージ ・ ストアにクエリを実行し、返されたポインターと、 **[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md)** 関数を使用してされた IMAP ストア オブジェクトへのポインターを取得するための C++ のコード サンプルを示しますラップ解除します。 このラップが解除されたストアを使用すると、メッセージ全体のダウンロードを呼び出すことがなく、現在の状態のメッセージへのアクセスができます。 
  
**UnwrapNoRef**では、 **UnwrapNoRef**の呼び出しに成功した後はこの新しいオブジェクトへのポインター、ラップが解除されたストアでの参照カウントは増分されません、ために、参照カウントを維持するために[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx)を呼び出す必要があります。 
  
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


