---
title: PidTagIconIndex 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIconIndex
api_type:
- HeaderDef
ms.assetid: 35bb0d6d-41d4-47d6-b161-be3721894201
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 35d9d0a50539f8aab2d26730dd4e4544c2535e60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346621"
---
# <a name="pidtagiconindex-canonical-property"></a>PidTagIconIndex 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
電子メール オブジェクトのグループを表示するときに使用するアイコンを示す番号が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ICON_INDEX  <br/> |
|識別子:  <br/> |0x1080  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティが存在する場合は、クライアントへのヒントです。 クライアントは、このプロパティの値を無視できます。 
  
|**メール アイテムの状態**|**アイコン インデックス**|
|:-----|:-----|
|新しいメール  <br/> |0xFFFFFFFF  <br/> |
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
|配信メール  <br/> |0x00000108  <br/> |
|メールの読み取り  <br/> |0x00000109  <br/> |
|配信以外のメール  <br/> |0x0000010A  <br/> |
|未読メール  <br/> |0x0000010B  <br/> |
|Recall_Sメール  <br/> |0x0000010C  <br/> |
|Recall_Fメール  <br/> |0x0000010D  <br/> |
|メールの追跡  <br/> |0x0000010E  <br/> |
|アウトオブオフィスメール  <br/> |0x0000011B  <br/> |
|メールの取り消し  <br/> |0x0000011C  <br/> |
|追跡メール  <br/> |0x00000130  <br/> |
|Contact  <br/> |0x00000200  <br/> |
|配布リスト  <br/> |0x00000202  <br/> |
|付箋青  <br/> |0x00000300  <br/> |
|付箋グリーン  <br/> |0x00000301  <br/> |
|付箋ピンク  <br/> |0x00000302  <br/> |
|付箋の黄色  <br/> |0x00000303  <br/> |
|付箋白  <br/> |0x00000304  <br/> |
|単一インスタンスの予定  <br/> |0x00000400  <br/> |
|定期的な予定  <br/> |0x00000401  <br/> |
|単一インスタンス会議  <br/> |0x00000402  <br/> |
|定期的な会議  <br/> |0x00000403  <br/> |
|会議出席依頼  <br/> |0x00000404  <br/> |
|承諾  <br/> |0x00000405  <br/> |
|拒否  <br/> |0x00000406  <br/> |
|Tentativly  <br/> |0x00000407  <br/> |
|取り消し  <br/> |0x00000408  <br/> |
|情報更新  <br/> |0x00000409  <br/> |
|タスク/タスク  <br/> |0x00000500  <br/> |
|割り当てられていない定期的なタスク  <br/> |0x00000501  <br/> |
|割り当て先のタスク  <br/> |0x00000502  <br/> |
|割り当て人のタスク  <br/> |0x00000503  <br/> |
|タスク要求  <br/> |0x00000504  <br/> |
|タスクの受け入れ  <br/> |0x00000505  <br/> |
|タスクの拒否  <br/> |0x00000506  <br/> |
|ジャーナルの会話  <br/> |0x00000601  <br/> |
|ジャーナル電子メール メッセージ  <br/> |0x00000602  <br/> |
|ジャーナル会議出席依頼  <br/> |0x00000603  <br/> |
|ジャーナル会議の応答  <br/> |0x00000604  <br/> |
|ジャーナル タスク要求  <br/> |0x00000606  <br/> |
|ジャーナル タスクの応答  <br/> |0x00000607  <br/> |
|ジャーナル ノート  <br/> |0x00000608  <br/> |
|ジャーナル FAX  <br/> |0x00000609  <br/> |
|ジャーナル電話  <br/> |0x0000060A  <br/> |
|ジャーナル レター  <br/> |0x0000060C  <br/> |
|ジャーナル Microsoft Office Word  <br/> |0x0000060D  <br/> |
|ジャーナル Microsoft Office Excel  <br/> |0x0000060E  <br/> |
|ジャーナル Microsoft Office PowerPoint  <br/> |0x0000060F  <br/> |
|ジャーナル Microsoft Office Access  <br/> |0x00000610  <br/> |
|ジャーナル ドキュメント  <br/> |0x00000612  <br/> |
|ジャーナル会議  <br/> |0x00000613  <br/> |
|ジャーナル 会議の取り消し  <br/> |0x00000614  <br/> |
|ジャーナル リモート セッション  <br/> |0x00000615  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
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

