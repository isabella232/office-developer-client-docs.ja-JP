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
ms.openlocfilehash: 7c6c763e918947c423c5dae283b0d4ab2f880616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801151"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**適用されます**: Outlook 
  
同期を呼び出すと、アイテムをダウンロードせず、元の個人用フォルダー ファイル (PST) へのアクセスを提供する、インターネット メッセージ アクセス プロトコル (IMAP) ラップ解除済みストア オブジェクトにポインターを取得します。
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>Parameters

 _ppvObject_
  
> [out]ポインター、 [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)ストア オブジェクトをラップすることはありません。 
    
## <a name="return-values"></a>戻り値

S_OK
  
- 呼び出しが成功したし、 _ppvObject_で返されたラップが解除されたインターフェイスへのポインター。
    
## <a name="remarks"></a>備考

せず、最初に、IMAP ストアのラップを解除、ストア内のメッセージにアクセスすることができます、強制的に同期メッセージ全体をダウンロードしようとします。 ラップが解除されたストアを使用すると、ダウンロードをトリガーすることがなく現在の状態のメッセージへのアクセスができます。
  
**UnwrapNoRef**では、 **UnwrapNoRef**の呼び出しに成功した後はこの新しいオブジェクトへのポインター、ラップが解除されたストアでの参照カウントは増分されません、ために、参照カウントを維持するために[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)を呼び出す必要があります。 
  
## <a name="see-also"></a>関連項目



[IProxyStoreObject](iproxystoreobject.md)
