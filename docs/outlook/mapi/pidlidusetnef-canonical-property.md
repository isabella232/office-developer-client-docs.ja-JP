---
title: PidLidUseTnef 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d5d38f98402c0804633d3bcb0f9ca196fa15795f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610056"
---
# <a name="pidlidusetnef-canonical-property"></a>PidLidUseTnef 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが MAPI から多目的インターネット メール拡張機能 (MIME) または簡易メール転送プロトコル (SMTP) 形式に変換される場合に、トランスポート ニュートラル カプセル化形式 (TNEF) をメッセージに含めるかどうかを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidUseTNEF  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008582  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージが TNEF から MIME または SMTP 形式に変換される場合に、TNEF をメッセージに含めるかどうかを指定します。 このプロパティが存在しない場合、TNEF をメッセージに含めません。
  
このプロパティは、メッセージが POP3/SMTP メール アカウントから送信された場合にのみ適用され、メッセージが他のプロバイダー (Microsoft Exchange Server など) によって送信された場合には適用されません。
  
投票ボタンが有効になっている場合や、OLE 埋め込みオブジェクトがメッセージに添付されている場合など、特定の状況では、Outlook は TNEF を強制的に使用するためにこのプロパティを設定できます。
  
メッセージ **PR_MSG_EDITOR_FORMAT** 送信時に、[テキスト形式 (PidTagMessageEditorFormat)](pidtagmessageeditorformat-canonical-property.md)プロパティを使用して、TNEF ではなくプレーン テキストのみを適用できます。 **PidLidUseTNEF** は **PR_MSG_EDITOR_FORMAT** の設定を上書きしますので、送信メッセージでテキストを強制的に送信するアプリケーションは **、PidLidUseTNEF** も検索して FALSE にリセットする必要があります。 さらに、最終的に送信されるメッセージの使用できない添付ファイルを避けるために、アドインは TNEF を必要とするメッセージ機能を削除する必要があります。 
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を呼び出して発信 MAPI メッセージを MIME ストリームに変換する場合は、CCSF_USE_TNEF フラグを使用して TNEF を強制できます。  これは **、PidLidUseTNEF** が設定されていない場合でも適用されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

