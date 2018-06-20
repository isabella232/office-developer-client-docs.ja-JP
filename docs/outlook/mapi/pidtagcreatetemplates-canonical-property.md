---
title: PidTagCreateTemplates の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 82da274670c9266a746defcf6bbd5dbcf621901b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802646"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>PidTagCreateTemplates の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
ダイアログ ボックス テンプレートのエントリの識別子を格納している埋め込みテーブル オブジェクトが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CREATE_TEMPLATES  <br/> |
|識別子:  <br/> |0x3604  <br/> |
|データを入力します。  <br/> |PT_OBJECT  <br/> |
|領域:  <br/> |アドレス帳  <br/> |
   
## <a name="remarks"></a>備考

コンテナーの内部オブジェクトを作成するテンプレートについては、このプロパティの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 結果のオブジェクトは、コンテナー内に作成できるテンプレートをすべてのエントリの識別子を提供する一時テーブルです。 
  
テンプレート オブジェクトを作成するには、一時テーブルから**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) の列の値に、コンテナー オブジェクトの**CreateEntry**メソッドを呼び出します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

