---
title: PidLidUseTnef 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315422"
---
# <a name="pidlidusetnef-canonical-property"></a>PidLidUseTnef 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが MAPI から多目的のインターネットメール内線 (MIME) または簡易メール転送プロトコル (SMTP) 形式に変換されたときに、メッセージにトランスポートニュートラルカプセル化形式 (TNEF) を含めるかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidUseTNEF  <br/> |
|プロパティセット:  <br/> |PSETID_Common  <br/> |
|ロング ID (LID):  <br/> |0x00008582  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、メッセージが tnef から MIME または SMTP 形式に変換されたときに、メッセージに tnef を含めるかどうかを指定します。 このプロパティは存在しない場合があり、その場合は TNEF をメッセージに含めることはできません。
  
このプロパティは、メッセージが POP3/SMTP メールアカウントから送信され、メッセージが他のプロバイダー (Microsoft Exchange Server など) によって送信されたときには適用されない場合にのみ適用されます。
  
投票ボタンが有効になっている場合や、OLE 埋め込みオブジェクトがメッセージに添付されている場合など、特定の状況では、Outlook でこのプロパティを設定して TNEF の使用を強制することができます。
  
**PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) プロパティを使用して、メッセージを送信するときに、TNEF ではなくプレーンテキストのみを適用できます。 **PidLidUseTNEF**は**PR_MSG_EDITOR_FORMAT**の設定よりも優先されるので、送信メッセージにプレーンテキストを強制するアプリケーションは、 **PidLidUseTNEF**を検索して FALSE にリセットする必要があります。 さらに、このアドインでは、TNEF を必要とするメッセージ機能を削除して、最終的に送信されるメッセージの添付ファイルを使用しないようにする必要があります。 
  
[iconvertersession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を呼び出して、 **CCSF_USE_TNEF**フラグを使用して、送信 MAPI メッセージを MIME ストリームに変換することにより、TNEF を強制することもできます。 これは、 **PidLidUseTNEF**が設定されていない場合でも適用されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

