---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 502f43eb5caecbc9285036c5ab7eb14cafded65b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575779"
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

