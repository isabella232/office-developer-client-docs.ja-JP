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
  
フォームに現在のメッセージを解放させます。
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>パラメーター

なし
  
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージが正常に解放されました。
    
## <a name="remarks"></a>解説

フォームは2つの HandsOff 状態に遷移します。
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
フォームがこれらの状態のいずれかになっている場合、フォームは永続的に保存されています。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォームが[標準](normal-state.md)または[noscribble](noscribble-state.md)状態であるときに、フォームビューアーが**IPersistMessage::** モジュールの入力メソッドを呼び出すと、 **** 現在のメッセージに埋め込まれた各メッセージと、 [IPersistStorage::](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx)現在のメッセージに埋め込まれている各 OLE オブジェクトに対して、"soffstorage method" を入力します。 次に、現在のメッセージとすべての埋め込みメッセージと OLE オブジェクトを解放します。 フォームが通常の状態であった場合は、[標準] [標準] 状態に移行します。 フォームが noscribble 状態であった場合は、[保存] 状態に切り替えます。 移行が正常に完了したら、メッセージの[IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出し、S_OK を返します。 
  
フォームが HandsOff 状態のいずれかであるときに、フォームビューアーが入力した**soffmessage**を呼び出すと、E_UNEXPECTED を返します。 
  
フォームのさまざまな状態の詳細については、「[フォームの状態](form-states.md)」を参照してください。 ストレージオブジェクトの HandsOff 状態を操作する方法の詳細については、「 [IPersistStorage:: 「保存](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx)方法」を参照してください。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[フォームの状態](form-states.md)

