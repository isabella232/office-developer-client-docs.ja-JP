---
title: 未初期化状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425562"
---
# <a name="uninitialized-state"></a>未初期化状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
初期化されていない状態は、最初に作成されたときの初期状態のフォームオブジェクトである必要があります。 form オブジェクトは、クライアントアプリケーションが form オブジェクトで[IPersistMessage:: InitNew](ipersistmessage-initnew.md)メソッドまたは[IPersistMessage:: Load](ipersistmessage-load.md)メソッドを呼び出すと、メッセージデータを使用して初期化されます。 次の表は、Unitialized 状態から許可される遷移を示しています。 
  
|**IPersistMessage メソッド**|**操作**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |既定のデータを使用して form オブジェクトを読み込みます。  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |form オブジェクトに対象のメッセージのデータを読み込みます。  <br/> |標準  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |成功を返すか、または最後のエラーを設定して E_UNEXPECTED を返します。  <br/> |初期化されていません  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |直前のエラーを返します。  <br/> |初期化されていません  <br/> |
|その他の[IPersistMessage: IUnknown](ipersistmessageiunknown.md)メソッドまたは他のインターフェイスからのメソッド  <br/> |最後のエラーをに設定し、E_UNEXPECTED を返します。  <br/> |初期化されていません  <br/> |
   
## <a name="see-also"></a>関連項目



[通常の状態](normal-state.md)
  
[フォームの状態](form-states.md)

