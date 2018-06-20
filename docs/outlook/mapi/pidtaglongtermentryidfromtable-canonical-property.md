---
title: PidTagLongTermEntryIdFromTable の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLongTermEntryIdFromTable
api_type:
- HeaderDef
ms.assetid: d9457fea-4b1e-4cf6-9c4b-14c98fbec2a1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ebb925ac1ff6507a5e686b769ba9d48b095fb527
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802963"
---
# <a name="pidtaglongtermentryidfromtable-canonical-property"></a>PidTagLongTermEntryIdFromTable の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
アイテムの長期間のエントリの識別子を取得します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_LONGTERM_ENTRYID_FROM_TABLE  <br/> |
|識別子:  <br/> |0x6670  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |テーブルのプロパティ  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、短期的なエントリの識別子ではなく、長期的なエントリ id と、アイテムのエントリ id を取得するのには内容のテーブルで使用できます。 長期的および短期的な識別子の詳細については、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagEntryId の標準的なプロパティ](pidtagentryid-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

