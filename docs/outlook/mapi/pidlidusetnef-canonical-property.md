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
ms.openlocfilehash: b0d5588218fd74f005de19daba002cd622c13a17
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587188"
---
# <a name="pidlidusetnef-canonical-property"></a>PidLidUseTnef 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
トランスポート ニュートラル カプセル化形式 (TNEF) をそのメッセージは MAPI から多目的インターネット メール拡張 (MIME) または簡易メール転送プロトコル (SMTP) の形式に変換するとメッセージに含める必要があるかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidUseTNEF  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008582  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティでは、TNEF をメッセージには TNEF から MIME または SMTP 形式に変換するとメッセージに含める必要があるかどうかを指定します。 このプロパティが失われている可能性があり、メッセージの TNEF を含めない場合は、します。
  
このプロパティは、メッセージが POP3 または SMTP のメール アカウントから送信され、Microsoft Exchange Server など、他のプロバイダーによって、メッセージが送信されるときは適用されませんがある場合にのみ適用されます。
  
状況によっては、オブジェクトがメッセージに接続されているボタンが有効になっている場合や OLE 埋め込みを返信するときなど、Outlook プロパティを設定この TNEF の使用を強制します。
  
メッセージを送信するときに、プレーン テキストと、TNEF ではないだけを適用するのには、 **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) プロパティを使用できます。 **PidLidUseTNEF**は、 **PR_MSG_EDITOR_FORMAT**の設定をオーバーライドするため送信メッセージのテキスト形式を強制的にしようとしているアプリケーション必要がありますもの**PidLidUseTNEF**を FALSE にリセットします。 さらに、アドインは、最後に送信されるメッセージに添付ファイルを使用できなくなるを避けるために tnef メッセージ機能を削除する必要があります。 
  
使用中の MAPI メッセージを MIME ストリームに変換する[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を呼び出すときに**CCSF_USE_TNEF**フラグは、TNEF にも適用できます。 これは、 **PidLidUseTNEF**が設定されていない場合でも適用されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
[[MS OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> エンコードし、メッセージと添付ファイルのオブジェクトを効率的なストリーム形式をデコードします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

