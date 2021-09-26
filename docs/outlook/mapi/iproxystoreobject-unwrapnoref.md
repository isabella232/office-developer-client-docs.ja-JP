---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: db3f247fda5be8f93210215fb83d51114a2165d4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620542"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
同期を呼び出してアイテムをダウンロードすることなく、基になる個人用フォルダー ファイル (PST) へのアクセスを提供する、ラップされていないインターネット メッセージ アクセス プロトコル (IMAP) ストア オブジェクトへのポインターを取得します。
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>パラメーター

 _ppvObject_
  
> [out]ラップされていない [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) ストア オブジェクトへのポインター。 
    
## <a name="return-values"></a>戻り値

S_OK
  
- 呼び出しが成功し、ラップされていないインターフェイスへのポインターが  _ppvObject で返されました_。
    
## <a name="remarks"></a>注釈

最初に IMAP ストアをアンラップしない場合、ストア内のメッセージにアクセスすると、メッセージ全体のダウンロードを試みる同期を強制的に実行できます。 ラップされていないストアを使用すると、ダウンロードをトリガーすることなく、現在の状態にあるメッセージにアクセスできます。
  
**UnwrapNoRef** はアンラップされたストア オブジェクトへのこの新しいポインターの参照カウントをインクリメントしないので **、UnwrapNoRef** を正常に呼び出した後、参照カウントを維持するために [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)を呼び出す必要があります。 
  
## <a name="see-also"></a>関連項目



[IProxyStoreObject](iproxystoreobject.md)

