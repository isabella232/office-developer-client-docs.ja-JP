---
title: PidTagDetailsTable の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a267f9a9fb8d97256cf7a448b453d04db2118180
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802678"
---
# <a name="pidtagdetailstable-canonical-property"></a>PidTagDetailsTable の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
埋め込み表示テーブル オブジェクトが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_DETAILS_TABLE  <br/> |
|識別子:  <br/> |0x3605  <br/> |
|データを入力します。  <br/> |PT_OBJECT  <br/> |
|領域:  <br/> |MAPI のコンテナー  <br/> |
   
## <a name="remarks"></a>備考

このプロパティをオブジェクトの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドに渡すことは、表示された表の作成を可能にする[IMAPITable](imapitableiunknown.md)インターフェイスを返します。 MAPI では、このテーブルを使用して、 [IAddrBook::Details](iaddrbook-details.md)の呼び出しへの応答で、アドレス帳のオブジェクトのプロパティ シートを表示します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagCreateTemplates の標準的なプロパティ](pidtagcreatetemplates-canonical-property.md)
  
[PidTagSearch の標準的なプロパティ](pidtagsearch-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

