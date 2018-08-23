---
title: PidTagTemplateid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7672c18f18d39ed1e4e8b4664ba7990563419a20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803630"
---
# <a name="pidtagtemplateid-canonical-property"></a>PidTagTemplateid 標準プロパティ

  
  
**適用対象**: Outlook 
  
**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))、永続的なエントリ ID の形式で表されますが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_TEMPLATEID  <br/> |
|識別子:  <br/> |0x3902  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI �A�h���X��  <br/> |
   
## <a name="remarks"></a>注釈

この値は、ネーム サービス プロバイダー インターフェイス (NSPI) サーバー上のすべてのアドレス帳オブジェクトのために存在する必要があります。、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) の値に一致する必要があります。、識別名 (DN) およびその識別名が DN の形式に従う必要があります。仕様のオブジェクトの種類を特定します。 
  
このプロパティは、オフライン アドレス帳内のオブジェクトに存在しません。
  
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
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

