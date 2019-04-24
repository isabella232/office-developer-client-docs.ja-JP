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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3f0d98b8ffa13fe238fc0fcf8ff0ec76a3a284eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309626"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームを管理できるフォームサーバーを表す識別子を返します。 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>パラメーター

 _lpclassid_
  
> [入力]フォームのクラス識別子 (CLSID) へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> クラス識別子が正常に返されました。
    
## <a name="remarks"></a>解説

**IPersistMessge:: GetClassID**メソッドは、 _lpclassid_パラメーターの内容をフォームサーバーのクラス識別子に設定し、S_OK を返します。 フォームビューアーが**GetClassID**を呼び出して正常に戻ると、フォームは[初期化](uninitialized-state.md)されていない状態になります。 
  
構造化ストレージオブジェクトでクラス識別子を使用する方法の詳細については、 [IPersist:: GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx)メソッドのドキュメントを参照してください。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

