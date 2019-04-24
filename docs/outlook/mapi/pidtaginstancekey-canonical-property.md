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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358512"
---
# <a name="pidtaginstancekey-canonical-property"></a>PidTagInstanceKey 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル内の行を一意に識別する値を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_INSTANCE_KEY  <br/> |
|識別子:  <br/> |0x0ff6  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |Table  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、テーブルビューの行を一意に識別するバイナリ値です。 ほとんどのテーブルでは必須の列です。 行が2つのビューに含まれている場合は、2つの異なるインスタンスキーがあります。 行のインスタンスキーは、テーブルが開かれるたびに異なる場合がありますが、テーブルを開いている間は一定のままです。 テーブルが使用されている間に追加された行は、以前に使用されていたインスタンスキーを再利用しません。 
  
拡張のすべての行を関連付けるには、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) または**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティを使用します。 **PR_INSTANCE_KEY**を使用して、拡張内で特定のインスタンスを検索します。 
  
複数値プロパティがテーブルで展開されている場合は、そのプロパティの各値に対して、拡張の各インスタンスに対して1つの行が作成されます。 各行には、 **PR_INSTANCE_KEY**プロパティの一意の値がありますが、他のすべての列は、拡張全体を通じて元の値を保持します。 
  
表の分類された並べ替えでは、実際のデータに対応していない行は、並べ替えの結果に追加できます。 このような各行には、すべてのテーブルのすべての行と同様に、固有のインスタンスキーがあります。 
  
 **PR_INSTANCE_KEY**は、テーブルイベント通知でも使用されます。 **propindex**と[TABLE_NOTIFICATION](table_notification.md)構造体の**前**のメンバーは、 **PR_INSTANCE_KEY**の値を保持する[spropvalue](spropvalue.md)構造です。 **propindex**メンバーは、追加または変更された行を示します。 **propprior**メンバーは、追加または変更された行の前の行を示します (**PR_NULL**は、最初の行に対する変更を示します)。 
  
この値は、表示テーブルの一部としてコピーされません。 
  
 **PR_INSTANCE_KEY**は、 [MAPIUID](mapiuid.md)構造体です。 すべてのインスタンスキーは、バイナリ値として直接比較できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
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

