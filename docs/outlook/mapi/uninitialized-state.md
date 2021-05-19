---
title: 初期化されていない状態
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
# <a name="uninitialized-state"></a>初期化されていない状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
初期化されていない状態は、最初に作成する際にオブジェクトが最初に含む必要がある初期状態のフォーム オブジェクトです。 クライアント アプリケーションがフォーム オブジェクトの [IPersistMessage::InitNew](ipersistmessage-initnew.md) または [IPersistMessage::Load](ipersistmessage-load.md) メソッドを呼び出す場合、フォーム オブジェクトはメッセージ データで初期化されます。 次の表では、Unitialized 状態からの許可された移行について説明します。 
  
|**IPersistMessage メソッド**|**Action**|**新しい状態**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |既定のデータを使用してフォーム オブジェクトを読み込む。  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |ターゲット メッセージのデータを含むフォーム オブジェクトを読み込む。  <br/> |標準  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |成功を返す、または最後のエラーをに設定し、E_UNEXPECTED。  <br/> |初期化されていません  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |最後のエラーを返します。  <br/> |初期化されていません  <br/> |
|その [他の IPersistMessage : 他のインターフェイスからの IUnknown](ipersistmessageiunknown.md) メソッドまたはメソッド  <br/> |最後のエラーを設定し、エラーを返E_UNEXPECTED。  <br/> |初期化されていません  <br/> |
   
## <a name="see-also"></a>関連項目



[標準状態](normal-state.md)
  
[フォームの状態](form-states.md)

