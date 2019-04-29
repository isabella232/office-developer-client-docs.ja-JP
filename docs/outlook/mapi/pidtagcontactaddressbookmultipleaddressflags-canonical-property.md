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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ecd795490d953f1aa237dfbd77585ba79c8b3234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429251"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>PidTagContactAddressBookMultipleAddressFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーが連絡先アイテムごとに複数の電子メールアドレスをサポートするかどうかを示すフラグを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|識別子:  <br/> |0x6625  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |連絡先のアドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティのフラグが TRUE の場合、プロバイダーには電子メールアドレスのない連絡先は含まれません。 優先されるのは、プライマリ電子メールアドレスのみです。 これは、連絡先のアドレス帳の [プロファイル] セクションのプロパティです。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

