---
title: IMAPISync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8e2e7a3f9279485d862fac5bb6413b3d3eb1343e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589085"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
トランスポート API を使用する代わりに e メールを同期するためのメカニズムを提供します。 ストア オブジェクトには、このインターフェイスは公開されています。 このインターフェイスを使用して、 [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)トランスポート プロバイダーより良い進行状況を提供できるし、エラー メッセージよりも、Microsoft Outlook で [送受信] ダイアログ ボックスに表示されます。
  
[送信トレイ] は、既定のストアにまだが。 トランスポート Api を使用して送信するメッセージは、外部ストアにすることはできませんので、メールを送信するのには、outlook が続行されます。
  
|||
|:-----|:-----|
|によって公開されます。  <br/> |ストアおよびトランスポート プロバイダー  <br/> |
|によって実装されます。  <br/> |Outlook  <br/> |
|によって呼び出されます。  <br/> |ストアおよびトランスポート プロバイダー  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |メッセージ ストア プロバイダーによって実装されます。 このメソッドは同期を開始するには、Outlook 2010、Outlook 2013 で呼び出されます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[MAPI インターフェイス](mapi-interfaces.md)

