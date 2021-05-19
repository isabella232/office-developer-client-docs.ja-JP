---
title: PidTagInstanceKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358512"
---
# <a name="pidtaginstancekey-canonical-property"></a>PidTagInstanceKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル内の行を一意に識別する値を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_INSTANCE_KEY  <br/> |
|識別子:  <br/> |0x0FF6  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Table  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、テーブル ビュー内の行を一意に識別するバイナリ値です。 ほとんどのテーブルでは必須の列です。 行が 2 つのビューに含まれている場合は、2 つの異なるインスタンス キーがあります。 行のインスタンス キーは、テーブルを開くごとに異なる場合がありますが、テーブルが開いている間は一定のままです。 テーブルの実行中に追加された行は、以前に使用されたインスタンス キーを再利用しないでください。 
  
拡張のすべての **行PR_ENTRYID** 関連付けるには、PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティまたは **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティを使用します。 拡張 **PR_INSTANCE_KEY** 特定のインスタンスを検索するには、次のコマンドを使用します。 
  
テーブル内で複数値プロパティを展開すると、拡張の各インスタンス (つまり、そのプロパティの値ごとに) に対して行が作成されます。 各行には PR_INSTANCE_KEY プロパティの一意の値が設定され **、他のすべての** 列は展開中も元の値を保持します。 
  
テーブルの分類された並べ替えでは、実際のデータに対応しない行を並べ替えの結果に追加できます。 このような各行は、すべてのテーブルのすべての行と同様に、独自の一意のインスタンス キーを持っています。 
  
 **PR_INSTANCE_KEY** は、テーブル イベント通知でも使用されます。 プロパティ **構造体の propIndex** および **propPrior** メンバーは、TABLE_NOTIFICATION値を保持する [SPropValue](spropvalue.md) **PR_INSTANCE_KEY** です。 [](table_notification.md) **propIndex メンバー** は、追加または変更された行を示します。 **propPrior メンバーは**、追加または変更された行の前の **行を示** します (PR_NULL行への変更を示します)。 
  
この値は、表示テーブルの一部としてコピーされません。 
  
 **PR_INSTANCE_KEY** [MAPIUID](mapiuid.md) 構造体です。 すべてのインスタンス キーをバイナリ値として直接比較できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
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

