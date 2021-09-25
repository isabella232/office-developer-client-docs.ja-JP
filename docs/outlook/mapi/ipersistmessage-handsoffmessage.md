---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5962da45d4b1cb6d0be53eb1a039657058e3df21
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587931"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームが現在のメッセージを解放します。
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージが正常にリリースされました。
    
## <a name="remarks"></a>注釈

フォームは 2 つの HandsOff 状態に移行します。
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
フォームがいずれかの状態にある場合、フォームは永続的に保存されているプロセスです。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォーム ビューアーが **IPersistMessage::HandsOffMessage** メソッドを呼び出す場合 [](normal-state.md)、フォームが Normal または [NoScribble](noscribble-state.md)状態のときに、現在のメッセージに埋め込まれている各メッセージで **HandsOffMessage** を再帰的に呼び出し、現在のメッセージに埋め込まれている各 OLE オブジェクトの [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx)メソッドを呼び出します。 次に、現在のメッセージとすべての埋め込みメッセージと OLE オブジェクトを解放します。 フォームが Normal 状態の場合は、HandsOffFromNormal 状態に移行します。 フォームが NoScribble 状態の場合は、HandsOffAfterSave 状態に移行します。 移行が成功したら、メッセージの [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) メソッドを呼び出し、S_OK。 
  
フォームビューアーが **HandsOffMessage を呼び出** し、フォームがいずれかの HandsOff 状態にある場合は、次のE_UNEXPECTED。 
  
フォームの異なる状態の詳細については、「フォームの状態」 [を参照してください](form-states.md)。 ストレージ オブジェクトの HandsOff 状態を操作する方法の詳細については [、「IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) メソッド」を参照してください。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[フォームの状態](form-states.md)

