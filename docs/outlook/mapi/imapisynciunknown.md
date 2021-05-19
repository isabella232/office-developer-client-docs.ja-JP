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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405593"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート API を使用する代わりに電子メールを同期するためのメカニズムを提供します。 このインターフェイスは、ストア オブジェクトで公開されます。 このインターフェイスと [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)を使用すると、トランスポート プロバイダーは、Microsoft Outlook の [送受信] ダイアログに表示されるメッセージよりも優れた進行状況とエラー メッセージを提供できます。
  
送信ボックスは既定のストアに残されています。 送信メッセージを外部ストアに保存できないので、Outlook はトランスポート API を使用してメールを送信し続ける。
  
|||
|:-----|:-----|
|次のユーザーによって公開されます。  <br/> |ストア プロバイダーとトランスポート プロバイダー  <br/> |
|実装元:  <br/> |Outlook  <br/> |
|呼び出し元:  <br/> |ストア プロバイダーとトランスポート プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |メッセージ ストア プロバイダーによって実装されます。 このメソッドは、同期を開始するために Outlook 2010 と Outlook 2013 によって呼び出されます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[MAPI のインターフェイス](mapi-interfaces.md)

