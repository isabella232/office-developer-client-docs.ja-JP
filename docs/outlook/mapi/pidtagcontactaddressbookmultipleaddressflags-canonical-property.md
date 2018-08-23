---
title: PidTagContactAddressBookMultipleAddressFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b783a624ef5358a69d65dd52785b285db1a70df7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588672"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>PidTagContactAddressBookMultipleAddressFlags 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
連絡先アイテムごとでは、プロバイダーが複数の電子メールをサポートするかどうかを示すフラグが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|識別子:  <br/> |0x6625  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|領域:  <br/> |連絡先のアドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティのフラグが TRUE の場合は、プロバイダーでは、この電子メール アドレスがない連絡先は含まれません。 プライマリ電子メール アドレスのみが受け入れられます。 これは、アドレス帳の連絡先のプロファイル セクションのプロパティです。
  
## <a name="related-resources"></a>関連リソース

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

