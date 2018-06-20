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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bce70d891bc33dcddb94fc05992c09991c6cdc63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800818"
---
# <a name="imapisyncprogresscallback--iunknown"></a>IMAPISyncProgressCallback: IUnknown

  
  
**適用されます**: Outlook 
  
MAPISIB 構造体のフィールドとしての呼び出し中に、ストア プロバイダーを渡します[IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md)。 ストア プロバイダーでは、このインターフェイスを使用して、Microsoft Outlook に同期の状態に関するフィードバックを提供します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> ||
|によって公開されます。  <br/> |Outlook  <br/> |
|によって実装されます。  <br/> |Outlook  <br/> |
|によって呼び出されます。  <br/> |ストア プロバイダー  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPISyncProgressCallback  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[Progress](imapisyncprogresscallback-progress.md) <br/> |ストア プロバイダーは、定期的に [送受信] ダイアログ ボックスのステータスを更新するには、この関数を呼び出します。  <br/> |
|[Error](imapisyncprogresscallback-error.md) <br/> |同期中にエラーが発生する場合、ストア プロバイダーは、[送受信] ダイアログ ボックスに表示される詳細情報を提供するには、この関数を呼び出します。  <br/> |
|[終了](imapisyncprogresscallback-done.md) <br/> |ストア プロバイダーは、Outlook の同期が完了したことを通知するためにこの関数を呼び出します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISync: IUnknown](imapisynciunknown.md)


[MAPI インターフェイス](mapi-interfaces.md)

