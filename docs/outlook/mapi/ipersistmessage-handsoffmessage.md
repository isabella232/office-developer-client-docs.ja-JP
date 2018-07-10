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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fd7e3b1d1284cdf4451330aabcce8fd0279ad5ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801108"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**適用されます**: Outlook 
  
フォームの現在のメッセージを解放するが発生します。
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Parameters

なし
  
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージは正常にリリースされました。
    
## <a name="remarks"></a>備考

HandsOff の 2 つの状態への移行をフォームします。
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
フォームは、これらの状態のいずれかの方法では、永続的に保存されているとします。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

メッセージごとに再帰的に呼び出し**HandsOffMessage**が、現在のメッセージと、[に埋め込まれたフォーム ビューアーは、フォームが[標準](normal-state.md)または[NoScribble](noscribble-state.md)の状態にあるときに、 **IPersistMessage::HandsOffMessage**メソッドを呼び出すとIPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx)各 OLE オブジェクトのメソッドは、現在のメッセージに埋め込まれています。 現在のメッセージとメッセージのすべての埋め込み OLE オブジェクトを解放します。 通常の状態で、フォームがあった場合は、HandsOffFromNormal 状態に移行します。 NoScribble 状態で、フォームがあった場合は、HandsOffAfterSave 状態に移行します。 移行に成功した後メッセージ[が](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出すし、S_OK を返します。 
  
フォーム ビューアーは、HandsOff 状態のいずれかの方法では、フォーム中に**HandsOffMessage**を呼び出す、ときに E_UNEXPECTED を返します。 
  
フォームのさまざまな状態の詳細については、[フォームの状態](form-states.md)を参照してください。 HandsOff 状態のストレージ ・ オブジェクトを操作する方法の詳細については、 [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx)メソッドを参照してください。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage: IUnknown](ipersistmessageiunknown.md)


[フォームの状態](form-states.md)
