---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 84f0ca88403980ff9ea1c91821a8a3d7edae74fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309717"
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

