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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429419"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームから通知を受信します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
|公開者:  <br/> |アドバイズシンクオブジェクトの表示  <br/> |
|実装元:  <br/> |フォームビューアー  <br/> |
|呼び出し元:  <br/> |フォーム オブジェクト  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|ポインターの種類:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[onshutdown](imapiviewadvisesink-onshutdown.md) <br/> |フォームが閉じられていることをフォームビューアーに通知します。  <br/> |
|[onnewmessage](imapiviewadvisesink-onnewmessage.md) <br/> |フォームビューアーに、新規または既存のメッセージがフォームにロードされたことを通知します。  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |フォームの印刷状態をフォームビューアーに通知します。  <br/> |
|[onsubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |現在のメッセージが MAPI スプーラーに送信されたことをフォームビューアーに通知します。  <br/> |
|[onsaved](imapiviewadvisesink-onsaved.md) <br/> |フォームの現在のメッセージが保存されたことをフォームビューアーに通知します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

