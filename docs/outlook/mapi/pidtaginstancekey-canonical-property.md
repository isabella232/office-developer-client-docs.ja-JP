---
title: PidTagInstanceKey の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bc16e88035f091a4f42a03342a70e7e3a1da5e0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802861"
---
# <a name="pidtaginstancekey-canonical-property"></a>PidTagInstanceKey の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
テーブル内の行を一意に識別する値が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_INSTANCE_KEY  <br/> |
|識別子:  <br/> |0x0FF6  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |テーブル  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、表形式ビュー内の行を一意に識別するバイナリ値です。 ほとんどのテーブルの必要な列があります。 行が 2 つのビューに含まれている場合は、2 つの別のインスタンスのキーがあります。 行のインスタンスのキーは、テーブルを開くたびに異なる場合がありますが、テーブルの中に一定に開いています。 テーブルの使用中に追加された行は、使用していたインスタンスのキーを再利用しません。 
  
**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) または**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) のプロパティを使用して、拡張のすべての行を関連付けるには。 **PR_INSTANCE_KEY**を使用して、展開内の特定のインスタンスを探します。 
  
表内の複数値を持つプロパティが拡張されると、行が作成、展開の各インスタンスは、そのプロパティの値ごとに。 各行は、展開全体の元の値を保持する他のすべての列に、 **PR_INSTANCE_KEY**プロパティに一意の値を持ちます。 
  
分類された種類のテーブル、行の実際のデータには対応しない、並べ替えの結果に追加できます。 すべてのテーブル内のすべての行と同様に、このような行には、独自の一意のインスタンスのキーがあります。 
  
 **PR_INSTANCE_KEY**は、表のイベント通知にも使用されます。 **PropIndex** 、 **propPrior** 、 [TABLE_NOTIFICATION](table_notification.md)構造体のメンバーは、 **PR_INSTANCE_KEY**の値を保持している[SPropValue](spropvalue.md)構造体です。 **PropIndex**メンバーは、追加または変更された行を示します。 **PropPrior**メンバーは、(**PR_NULL**は、最初の行への変更を示します) の追加または変更された行の前に行を示します。 
  
表示された表の一部としては、この値はコピーされません。 
  
 **PR_INSTANCE_KEY**は、 [MAPIUID](mapiuid.md)構造です。 バイナリ値として、すべてのインスタンスのキーを直接比較できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

