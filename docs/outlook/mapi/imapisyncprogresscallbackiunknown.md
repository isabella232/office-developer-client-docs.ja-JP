---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418338"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPISync :SyncInBackground](imapisyncsynchronizeinbackground.md)の呼び出し中に、MAPISIB 構造体のフィールドとしてストア プロバイダーを渡します。 ストア プロバイダーは、このインターフェイスを使用して、同期Outlookに関するフィードバックを Microsoft に提供します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> ||
|次のユーザーによって公開されます。  <br/> |Outlook  <br/> |
|実装元:  <br/> |Outlook  <br/> |
|呼び出し元:  <br/> |ストア プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[進行状況](imapisyncprogresscallback-progress.md) <br/> |ストア プロバイダーは定期的にこの関数を呼び出して、[送受信] ダイアログの状態を更新します。  <br/> |
|[エラー](imapisyncprogresscallback-error.md) <br/> |同期中にエラーが発生した場合、ストア プロバイダーはこの関数を呼び出して、[送受信] ダイアログに表示される詳細を提供します。  <br/> |
|[終了](imapisyncprogresscallback-done.md) <br/> |ストア プロバイダーは、この関数を呼び出して、Outlook完了したと通知します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISync : IUnknown](imapisynciunknown.md)


[MAPI のインターフェイス](mapi-interfaces.md)

