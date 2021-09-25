---
title: PidTagContactAddressBookMultipleAddressFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 72cf1ee919ce9bc49792712f9e0b441d23f1ae01
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566844"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>PidTagContactAddressBookMultipleAddressFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーが連絡先アイテムごとに複数の電子メール アドレスをサポートするかどうかを示すフラグが含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|識別子:  <br/> |0x6625  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |連絡先アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティのフラグが TRUE の場合、プロバイダーには電子メール アドレスのない連絡先は含めずに設定されます。 プライマリ 電子メール アドレスだけが受け入れされます。 これは、[連絡先アドレス帳] プロファイル セクションのプロパティです。
  
## <a name="related-resources"></a>関連リソース

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

