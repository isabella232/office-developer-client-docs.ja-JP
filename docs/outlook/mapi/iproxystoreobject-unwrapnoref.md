---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ef9f506c1a95fec86c7f092b0299198e6149d3ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320154"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
同期を呼び出してアイテムをダウンロードすることなく、基になる個人用フォルダーファイル (PST) へのアクセスを提供する、ラップされていないインターネットメッセージアクセスプロトコル (IMAP) ストアオブジェクトへのポインターを取得します。
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>パラメーター

 _ppvObject_
  
> 読み上げラップされていない[IMsgStore: imapiprop](imsgstoreimapiprop.md) store オブジェクトへのポインター。 
    
## <a name="return-values"></a>戻り値

S_OK
  
- 呼び出しが正常に実行され、 _ppvObject_でラップされていないインターフェイスへのポインターが返されました。
    
## <a name="remarks"></a>解説

最初に IMAP ストアをラップ解除せずに、ストア内のメッセージにアクセスすると、メッセージ全体をダウンロードしようとする同期が強制的に実行されます。 ラップされていないストアを使用すると、ダウンロードをトリガーすることなく、現在の状態のメッセージにアクセスできます。
  
**UnwrapNoRef**は、ラップされていない store オブジェクトへのこの新しいポインターの参照カウントをインクリメントしないため、 **UnwrapNoRef**の呼び出しに成功した後で、 [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)を呼び出して参照カウントを維持する必要があります。 
  
## <a name="see-also"></a>関連項目



[IProxyStoreObject](iproxystoreobject.md)

