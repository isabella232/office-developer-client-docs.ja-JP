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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341238"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[imapisync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md)の呼び出し中に、ストアプロバイダーを MAPISIB 構造体のフィールドとして渡します。 ストアプロバイダーは、このインターフェイスを使用して、同期の状態に関する Microsoft Outlook へのフィードバックを提供します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> ||
|公開者:  <br/> |Outlook  <br/> |
|実装元:  <br/> |Outlook  <br/> |
|呼び出し元:  <br/> |ストアプロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[進行状況](imapisyncprogresscallback-progress.md) <br/> |ストアプロバイダーは、この関数を定期的に呼び出して、送信/受信ダイアログの状態を更新します。  <br/> |
|[Error](imapisyncprogresscallback-error.md) <br/> |同期中にエラーが発生した場合、ストアプロバイダーはこの関数を呼び出して、送受信ダイアログに表示される詳細情報を提供します。  <br/> |
|[終了](imapisyncprogresscallback-done.md) <br/> |ストアプロバイダーはこの関数を呼び出して、同期が完了したことを Outlook に通知します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISync : IUnknown](imapisynciunknown.md)


[MAPI のインターフェイス](mapi-interfaces.md)

