---
title: PidTagRowType の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7fdb8781c39d7814ff2c38ff4df4545511d28a5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803378"
---
# <a name="pidtagrowtype-canonical-property"></a>PidTagRowType の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
テーブル内の行の種類を示す値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ROW_TYPE  <br/> |
|識別子:  <br/> |0x0FF5  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>備考

内容のテーブルにのみ、このプロパティが表示されます。 カテゴリは、項目がある場合にのみ存在します。
  
このプロパティは、次の値の 1 つだけ持つことができます。
  
TBL_LEAF_ROW 
  
> カテゴリの行ではなく、実際のデータを表します。
    
TBL_EMPTY_CATEGORY 
  
> 現在使用されていません。
    
TBL_EXPANDED_CATEGORY 
  
> カテゴリが展開されています。ユーザー インターフェイスでは、その横にあるマイナス記号 (-) でこの通常表示します。
    
TBL_COLLAPSED_CATEGORY 
  
> カテゴリが折りたたまれています。ユーザー ・ インタ フェースでは、その横にあるプラス記号 (+) でこの通常表示します。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> テーブルのコア オブジェクトに許容される操作が含まれます。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagRowid の標準的なプロパティ](pidtagrowid-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

