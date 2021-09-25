---
title: IPersistMessageGetClassID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5d8f4283d2cf9e5de7547264de429ef8b17d9667
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561440"
---
# <a name="ipersistmessagegetclassid"></a>IPersistMessage::GetClassID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームを管理できるフォーム サーバーを表す識別子を返します。 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a>パラメーター

 _lpClassID_
  
> [in, out]フォームのクラス識別子 (CLSID) へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> クラス識別子が正常に返されました。
    
## <a name="remarks"></a>注釈

**IPersistMessge::GetClassID** メソッドは _、lpClassID_ パラメーターの内容をフォーム サーバーのクラス識別子に設定し、S_OK。 フォーム ビューアーが **GetClassID** を呼び出して正常に返されると、フォームは初期化されていない [状態になります](uninitialized-state.md) 。 
  
構造化ストレージ オブジェクトでクラス識別子を使用する方法の詳細については [、IPersist::GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) メソッドのドキュメントを参照してください。 
  
## <a name="see-also"></a>関連項目



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

