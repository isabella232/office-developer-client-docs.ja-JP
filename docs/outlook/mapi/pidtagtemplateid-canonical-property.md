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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 96bcd15606771bd112568ad94133507ab14b2bcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358822"
---
# <a name="pidtagtemplateid-canonical-property"></a>PidTagTemplateid 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
永続的なエントリ **ID PR_ENTRYID** 形式で表される文字列 [(PidTagEntryId)](pidtagentryid-canonical-property.md)が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_TEMPLATEID  <br/> |
|識別子:  <br/> |0x3902  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI �A�h���X��  <br/> |
   
## <a name="remarks"></a>注釈

この値は、ネーム サービス プロバイダー インターフェイス (NSPI) サーバー上のすべてのアドレス帳オブジェクトに対して存在する必要があります。識別名 (DN) は **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) の値と一致する必要があります。その DN はオブジェクトの種類に特定の DN 形式の仕様に従う必要があります。 
  
このプロパティは、オフライン アドレス帳内のオブジェクトには存在しません。
  
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
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

