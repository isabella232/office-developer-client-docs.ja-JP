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
  
メッセージング システムでサポートされていない MAPI プロパティを、メッセージに接続できるバイナリ ストリームにカプセル化するメソッドを提供します。 このカプセル化に使用される形式は、Transport-Neutralカプセル化形式 (TNEF) です。 ターゲット トランスポート プロバイダーまたは MAPI ベースのクライアント アプリケーションは、TNEF 添付ファイルを含むメッセージを受信すると、添付ファイルからプロパティを回復できます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Tnef.h  <br/> |
|次のユーザーによって公開されます。  <br/> |TNEF オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイ  <br/> |
|インターフェイス識別子:  <br/> |IID_ITNEF  <br/> |
|ポインターの種類:  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |呼び出し元のサービス プロバイダーまたはゲートウェイが、メッセージまたは添付ファイルのカプセル化にプロパティを追加できます。  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |TNEF カプセル化からプロパティを抽出します。  <br/> |
|[Finish](itnef-finish.md) <br/> |キューに入れ、待機しているすべての TNEF 操作の処理を終了します。  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |カプセル化されたメッセージのテキストにストリーム インターフェイスを開きます。  <br/> |
|[SetProps](itnef-setprops.md) <br/> |元のメッセージまたは添付ファイルを変更せずに、カプセル化されたメッセージまたは添付ファイルの 1 つ以上のプロパティの値を設定します。  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |メッセージの TNEF データ ストリーム内のメッセージの受信者テーブルのビューをエンコードします。  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |メッセージの個々のコンポーネントを一度に 1 つの TNEF ストリームに処理します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

