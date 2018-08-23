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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e8267b254648870cea4e16b4dea0e9c92e316fb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801258"
---
# <a name="itnef--iunknown"></a>ITnef : IUnknown

  
  
**適用対象**: Outlook 
  
メッセージに関連付けることができるバイナリ ストリームに、メッセージング システムがサポートされていない MAPI プロパティをカプセル化するためのメソッドを提供します。 このカプセル化に使用される形式は、トランスポート ニュートラル カプセル化形式 (TNEF) です。 ターゲット トランスポート プロバイダーまたは MAPI ベースのクライアント アプリケーション、TNEF の添付ファイルを含むメッセージを受信するには、回復できます、プロパティ、添付ファイルから。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Tnef.h  <br/> |
|によって公開されます。  <br/> |TNEF オブジェクト  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイ  <br/> |
|インターフェイスの識別子。  <br/> |IID_ITNEF  <br/> |
|ポインターの型。  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |メッセージまたは添付ファイルをカプセル化するプロパティを追加するのには、呼び出し元のサービス プロバイダーまたはゲートウェイを有効にします。  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |TNEF のカプセル化のプロパティを抽出します。  <br/> |
|[Finish](itnef-finish.md) <br/> |完了するとキューに登録されたすべての TNEF の操作を処理し、待機しています。  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |カプセル化されたメッセージのテキストのストリームのインタ フェースを開きます。  <br/> |
|[SetProps](itnef-setprops.md) <br/> |元のメッセージまたは添付ファイルを変更することがなくカプセル化されたメッセージまたは添付ファイルの 1 つまたは複数のプロパティの値を設定します。  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |メッセージの TNEF データ ストリーム内のメッセージの受信者テーブルのビューをエンコードします。  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |TNEF ストリームに同時に 1 つのメッセージからの個々 のコンポーネントを処理します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

