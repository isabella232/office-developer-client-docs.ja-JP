---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c9d769e6a32fad22750a965debbbdce83e4de539
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586459"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォームを管理するフォームのサーバーを表す識別子を返します。 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>パラメーター

 _lpClassID_
  
> [で [チェック アウト]フォームのクラス識別子 (CLSID) へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> クラス識別子が正常に返されました。
    
## <a name="remarks"></a>注釈

**IPersistMessge::GetClassID**メソッドは、フォーム サーバーのクラス id に_lpClassID_パラメーターの内容を設定し、S_OK を返します。 フォーム ビューアーは、 **GetClassID**を呼び出すし、正常に返されます、フォームが[初期化されていない](uninitialized-state.md)状態で配置されます。 
  
構造化ストレージ オブジェクトのクラス識別子を使用する方法の詳細については、 [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx)メソッドのマニュアルを参照してください。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

