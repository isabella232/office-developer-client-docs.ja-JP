---
title: PidTagLastVerbExecuted 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagLastVerbExecuted
api_type:
- HeaderDef
ms.assetid: 502f0261-697f-41bf-8530-75e1d0f503e5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4e5e13f54cf33542ac8a73a28e5cfb948e484dba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587539"
---
# <a name="pidtaglastverbexecuted-canonical-property"></a>PidTagLastVerbExecuted 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
最後に実行された動詞を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_LAST_VERB_EXECUTED  <br/> |
|識別子:  <br/> |0x1081  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |履歴  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、次のいずれかの値を指定できます。
  
|**Verb**|**プロパティ値**|
|:-----|:-----|
|投稿  <br/> |0x00000001  <br/> |
|その他  <br/> |0x00000003  <br/> |
|メールの読み取り  <br/> |0x00000100  <br/> |
|未読メール  <br/> |0x00000101  <br/> |
|送信済みメール  <br/> |0x00000102  <br/> |
|送信されていないメール  <br/> |0x00000103  <br/> |
|受信メール  <br/> |0x00000104  <br/> |
|返信メール  <br/> |0x00000105  <br/> |
|転送されたメール  <br/> |0x00000106  <br/> |
|リモート メール  <br/> |0x00000107  <br/> |
|配信レシート  <br/> |0x00000108  <br/> |
|レシートの読み取り  <br/> |0x00000109  <br/> |
|非送信レシート  <br/> |0x0000010A  <br/> |
|未読の領収書  <br/> |0x0000010B  <br/> |
|Recall_Sメール  <br/> |0x0000010C  <br/> |
|Recall_Fメール  <br/> |0x0000010D  <br/> |
|メールの追跡  <br/> |0x0000010E  <br/> |
|アウト オブ Office メール  <br/> |0x0000011B  <br/> |
|メールの取り消し  <br/> |0x0000011C  <br/> |
|追跡メール  <br/> |0x00000139  <br/> |
|Contact  <br/> |0x00000200  <br/> |
|配布リスト  <br/> |0x00000201  <br/> |
|付箋, 青  <br/> |0x00000300  <br/> |
|付箋, 緑  <br/> |0x00000301  <br/> |
|付箋, ピンク  <br/> |0x00000302  <br/> |
|付箋, 黄色  <br/> |0x00000303  <br/> |
|付箋, 白  <br/> |0x00000304  <br/> |
|単一インスタンスの予定  <br/> |0x00000400  <br/> |
|定期的な予定  <br/> |0x00000401  <br/> |
|単一インスタンス会議  <br/> |0x00000402  <br/> |
|定期的な会議  <br/> |0x00000403  <br/> |
|会議出席依頼/完全更新  <br/> |0x00000404  <br/> |
|承諾  <br/> |0x00000405  <br/> |
|拒否  <br/> |0x00000406  <br/> |
|仮承諾  <br/> |0x00000407  <br/> |
|キャンセル  <br/> |0x00000408  <br/> |
|Informational Update  <br/> |0x00000409  <br/> |
|タスク/タスクの更新  <br/> |0x00000500  <br/> |
|割り当てられていない定期的なタスク  <br/> |0x00000501  <br/> |
|割り当て先のタスク  <br/> |0x00000502  <br/> |
|割り当て人のタスク  <br/> |0x00000503  <br/> |
|タスクの依頼  <br/> |0x00000504  <br/> |
|タスクの受け入れ  <br/> |0x00000505  <br/> |
|タスクの拒否  <br/> |0x00000506  <br/> |
|ジャーナルの会話  <br/> |0x00000601  <br/> |
|ジャーナル 電子メール メッセージ  <br/> |0x00000602  <br/> |
|ジャーナル会議出席依頼  <br/> |0x00000603  <br/> |
|ジャーナル会議の応答  <br/> |0x00000604  <br/> |
|ジャーナル タスク要求  <br/> |0x00000606  <br/> |
|ジャーナル タスクの応答  <br/> |0x00000607  <br/> |
|ジャーナル ノート  <br/> |0x00000608  <br/> |
|ジャーナル FAX  <br/> |0x00000609  <br/> |
|ジャーナル 電話呼び出し  <br/> |0x0000060A  <br/> |
|ジャーナル タスク  <br/> |0x0000060B  <br/> |
|ジャーナル レター  <br/> |0x0000060C  <br/> |
|ジャーナル Microsoft Office Word  <br/> |0x0000060D  <br/> |
|ジャーナル Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|ジャーナル Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|ジャーナル Microsoft Office Access  <br/> |0x00000610  <br/> |
|ジャーナル ドキュメント  <br/> |0x00000612  <br/> |
|ジャーナル 会議  <br/> |0x00000613  <br/> |
|ジャーナル 会議の取り消し  <br/> |0x00000614  <br/> |
|ジャーナル リモート セッション  <br/> |0x00000615  <br/> |
|新しいメール  <br/> |0xFFFFFFFF  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> 
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

