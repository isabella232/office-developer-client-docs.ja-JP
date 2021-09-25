---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b7486139818ede9bd7e4b66472317ab50b05ba4d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567376"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームから通知を受け取ります。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|次のユーザーによって公開されます。  <br/> |シンク オブジェクトの表示  <br/> |
|実装元:  <br/> |フォーム ビューアー  <br/> |
|呼び出し元:  <br/> |フォーム オブジェクト  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|ポインターの種類:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |フォームが閉じているとフォーム ビューアーに通知します。  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |新しいメッセージまたは既存のメッセージがフォームに読み込まれたとフォーム ビューアーに通知します。  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |フォームの印刷状態をフォーム ビューアーに通知します。  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |現在のメッセージが MAPI スプーラーに送信されたとフォーム ビューアーに通知します。  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |フォームの現在のメッセージが保存されたとフォーム ビューアーに通知します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

