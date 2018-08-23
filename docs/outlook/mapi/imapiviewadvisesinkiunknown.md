---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f16585a96164835784bfa1af3752bd652daf76e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800860"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**適用対象**: Outlook 
  
フォームからの通知を受信します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって公開されます。  <br/> |シンク オブジェクトをビューに伝えます。  <br/> |
|によって実装されます。  <br/> |フォームの閲覧者  <br/> |
|によって呼び出されます。  <br/> |フォーム オブジェクト  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|ポインターの型。  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[に](imapiviewadvisesink-onshutdown.md) <br/> |フォーム ビューアーに、フォームが閉じられることを通知します。  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |新規または既存のメッセージのいずれかに読み込まれました、フォーム、フォームのビューアーを通知します。  <br/> |
|[印刷時](imapiviewadvisesink-onprint.md) <br/> |フォーム ビューアーのフォームの印刷の状態を通知します。  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |フォーム ビューアーの現在のメッセージが MAPI スプーラーに送信されたことを通知します。  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |フォームの現在のメッセージが保存されているフォーム ビューアーを通知します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

