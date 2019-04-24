---
title: PidTagLastVerbExecuted 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastVerbExecuted
api_type:
- HeaderDef
ms.assetid: 502f0261-697f-41bf-8530-75e1d0f503e5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9abd4eb955428595ebe41ab9b2c661303ee2779a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279616"
---
# <a name="pidtaglastverbexecuted-canonical-property"></a>PidTagLastVerbExecuted 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
最後に実行された動詞を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_LAST_VERB_EXECUTED  <br/> |
|識別子:  <br/> |0x1081  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |履歴  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、次のいずれかの値を指定できます。
  
|**Verb**|**プロパティ値**|
|:-----|:-----|
|投稿  <br/> |0x00000001  <br/> |
|その他  <br/> |0x00000003  <br/> |
|メールの読み取り  <br/> |0x00000100  <br/> |
|未読メール  <br/> |0x00000101  <br/> |
|送信されたメール  <br/> |0x00000102  <br/> |
|未送信メール  <br/> |0x00000103  <br/> |
|受信メール  <br/> |0x00000104  <br/> |
|返信済みメール  <br/> |0x00000105  <br/> |
|転送されたメール  <br/> |0x00000106  <br/> |
|リモートメール  <br/> |0x00000107  <br/> |
|配信確認  <br/> |0x00000108  <br/> |
|開封確認  <br/> |0x00000109  <br/> |
|配信不能メッセージ  <br/> |0x0000010A  <br/> |
|非開封確認メッセージ  <br/> |0x0000010B  <br/> |
|Recall_S メール  <br/> |0x0000010C  <br/> |
|Recall_F メール  <br/> |0x0000010D  <br/> |
|メールの追跡  <br/> |0x0000010E  <br/> |
|不在時のメール  <br/> |0x0000011b  <br/> |
|メールの取り消し  <br/> |0x0000011c  <br/> |
|追跡されたメール  <br/> |0x00000139  <br/> |
|連絡先  <br/> |0x00000200  <br/> |
|配布リスト  <br/> |0x00000201  <br/> |
|付箋、青  <br/> |0x00000300  <br/> |
|付箋、グリーン  <br/> |0x00000301  <br/> |
|付箋: ピンク  <br/> |0x00000302  <br/> |
|付箋 (黄)  <br/> |0x00000303  <br/> |
|付箋 (白)  <br/> |0x00000304  <br/> |
|単一インスタンスの予定  <br/> |0x00000400  <br/> |
|定期的な予定  <br/> |0x00000401  <br/> |
|シングルインスタンス会議  <br/> |0x00000402  <br/> |
|定期的な会議  <br/> |0x00000403  <br/> |
|会議出席依頼/完全更新  <br/> |0x00000404  <br/> |
|承諾  <br/> |0x00000405  <br/> |
|同意  <br/> |0x00000406  <br/> |
|仮承諾  <br/> |0x00000407  <br/> |
|キャン  <br/> |0x00000408  <br/> |
|情報更新  <br/> |0x00000409  <br/> |
|タスク/タスクの更新  <br/> |0x00000500  <br/> |
|割り当てられていない定期タスク  <br/> |0x00000501  <br/> |
|担当者のタスク  <br/> |0x00000502  <br/> |
|Assigner のタスク  <br/> |0x00000503  <br/> |
|タスクの依頼  <br/> |0x00000504  <br/> |
|タスクの承諾  <br/> |0x00000505  <br/> |
|タスクの却下  <br/> |0x00000506  <br/> |
|ジャーナルの会話  <br/> |0x00000601  <br/> |
|ジャーナルメールメッセージ  <br/> |0x00000602  <br/> |
|ジャーナル会議出席依頼  <br/> |0x00000603  <br/> |
|ジャーナル会議の応答  <br/> |0x00000604  <br/> |
|ジャーナルタスクの依頼  <br/> |0x00000606  <br/> |
|ジャーナルタスクの応答  <br/> |0x00000607  <br/> |
|ジャーナルメモ  <br/> |0x00000608  <br/> |
|ジャーナル Fax  <br/> |0x00000609  <br/> |
|履歴電話  <br/> |0x0000060a  <br/> |
|履歴タスク  <br/> |0x0000060b  <br/> |
|仕訳帳レター  <br/> |0x0000060c  <br/> |
|Journal Microsoft Office Word  <br/> |0x0000060d  <br/> |
|Journal Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|Microsoft Office PowerPoint のジャーナル  <br/> |0x0000060f  <br/> |
|Microsoft Office access のジャーナル  <br/> |0x00000610  <br/> |
|ジャーナルドキュメント  <br/> |0x00000612  <br/> |
|ジャーナル会議  <br/> |0x00000613  <br/> |
|ジャーナル会議の取り消し  <br/> |0x00000614  <br/> |
|ジャーナルリモートセッション  <br/> |0x00000615  <br/> |
|新しいメール  <br/> |0xFFFFFFFF  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> 
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

