---
title: imapisync IUnknown
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
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341280"
---
# <a name="imapisync--iunknown"></a>IMAPISync : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート API を使用する代わりに、電子メールを同期するためのメカニズムを提供します。 このインターフェイスは、store オブジェクトに公開されます。 このインターフェイスと[IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)を使用することにより、トランスポートプロバイダーは、Microsoft Outlook の送受信ダイアログに表示されるのとは異なる進行状況およびエラーメッセージを提供できます。
  
送信トレイはまだ既定のストアにあります。 送信メッセージが外部ストアに存在できないため、Outlook は引き続きトランスポート api を使用してメールを送信します。
  
|||
|:-----|:-----|
|公開者:  <br/> |ストアとトランスポートプロバイダー  <br/> |
|実装元:  <br/> |Outlook  <br/> |
|呼び出し元:  <br/> |ストアとトランスポートプロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPISync  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[SynchronizeInBackground](imapisyncsynchronizeinbackground.md) <br/> |メッセージストアプロバイダーによって実装されます。 このメソッドは、outlook 2010 および outlook 2013 によって呼び出され、同期を開始します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)


[MAPI のインターフェイス](mapi-interfaces.md)

