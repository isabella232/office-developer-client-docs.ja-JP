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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ef9f506c1a95fec86c7f092b0299198e6149d3ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382933"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
同期を呼び出すと、アイテムをダウンロードせず、元の個人用フォルダー ファイル (PST) へのアクセスを提供する、インターネット メッセージ アクセス プロトコル (IMAP) ラップ解除済みストア オブジェクトにポインターを取得します。
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>パラメーター

 _ppvObject_
  
> [out]ポインター、 [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)ストア オブジェクトをラップすることはありません。 
    
## <a name="return-values"></a>戻り値

S_OK
  
- 呼び出しが成功したし、 _ppvObject_で返されたラップが解除されたインターフェイスへのポインター。
    
## <a name="remarks"></a>備考

せず、最初に、IMAP ストアのラップを解除、ストア内のメッセージにアクセスすることができます、強制的に同期メッセージ全体をダウンロードしようとします。 ラップが解除されたストアを使用すると、ダウンロードをトリガーすることがなく現在の状態のメッセージへのアクセスができます。
  
**UnwrapNoRef**では、 **UnwrapNoRef**の呼び出しに成功した後はこの新しいオブジェクトへのポインター、ラップが解除されたストアでの参照カウントは増分されません、ために、参照カウントを維持するために[IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)を呼び出す必要があります。 
  
## <a name="see-also"></a>関連項目



[IProxyStoreObject](iproxystoreobject.md)

