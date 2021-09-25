---
title: 初期化されていない状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f2c2d31033ee77e1de581045012be632f15c5dc4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609237"
---
# <a name="uninitialized-state"></a>初期化されていない状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
初期化されていない状態は、最初に作成する際にオブジェクトが最初に含む必要がある初期状態のフォーム オブジェクトです。 クライアント アプリケーションがフォーム オブジェクトの [IPersistMessage::InitNew](ipersistmessage-initnew.md) または [IPersistMessage::Load](ipersistmessage-load.md) メソッドを呼び出す場合、フォーム オブジェクトはメッセージ データで初期化されます。 次の表では、Unitialized 状態からの許可された移行について説明します。 
  
|**IPersistMessage メソッド**|**操作**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |既定のデータを使用してフォーム オブジェクトを読み込む。  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |ターゲット メッセージのデータを含むフォーム オブジェクトを読み込む。  <br/> |標準  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |成功を返す、または最後のエラーをに設定し、E_UNEXPECTED。  <br/> |初期化されていません  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |最後のエラーを返します。  <br/> |初期化されていません  <br/> |
|その [他の IPersistMessage : 他のインターフェイスからの IUnknown](ipersistmessageiunknown.md) メソッドまたはメソッド  <br/> |最後のエラーを設定し、エラーを返E_UNEXPECTED。  <br/> |初期化されていません  <br/> |
   
## <a name="see-also"></a>関連項目



[標準状態](normal-state.md)
  
[フォームの状態](form-states.md)

