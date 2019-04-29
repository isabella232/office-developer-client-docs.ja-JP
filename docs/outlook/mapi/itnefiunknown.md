---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1f815a914deb5e21f3d913abe46a84cc7a32b4ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428516"
---
# <a name="itnef--iunknown"></a>ITnef : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージングシステムでサポートされていない MAPI プロパティを、メッセージに添付できるバイナリストリームにカプセル化するためのメソッドを提供します。 このカプセル化に使用される形式は、トランスポートに依存しないカプセル化形式 (TNEF) です。 その後、宛先のトランスポートプロバイダーまたは MAPI ベースのクライアントアプリケーションは、TNEF 添付ファイルを含むメッセージを受信するときに、添付ファイルからプロパティを回復します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Tnef  <br/> |
|公開者:  <br/> |TNEF オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |トランスポートプロバイダー、メッセージストアプロバイダー、ゲートウェイ  <br/> |
|インターフェイス識別子:  <br/> |IID_ITNEF  <br/> |
|ポインターの種類:  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[addprops](itnef-addprops.md) <br/> |呼び出し元のサービスプロバイダーまたはゲートウェイが、メッセージまたは添付ファイルのカプセル化にプロパティを追加できるようにします。  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |TNEF のカプセル化からプロパティを抽出します。  <br/> |
|[Finish](itnef-finish.md) <br/> |キューに入って待機しているすべての TNEF 操作の処理を終了します。  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |カプセル化されたメッセージのテキストにストリームインターフェイスを開きます。  <br/> |
|[setprops による](itnef-setprops.md) <br/> |元のメッセージまたは添付ファイルを変更せずに、カプセル化されたメッセージまたは添付ファイルの1つ以上のプロパティの値を設定します。  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |メッセージの受信者テーブルのビューを、メッセージの TNEF データストリームでエンコードします。  <br/> |
|[finish コンポーネント](itnef-finishcomponent.md) <br/> |メッセージから1つずつ、個々のコンポーネントを TNEF ストリームに処理します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

