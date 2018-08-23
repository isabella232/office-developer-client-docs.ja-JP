---
title: PidTagContactAddressBookMultipleAddressFlag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 34f61f3ef64e5751f9be3df534c4379583447799
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592697"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>PidTagContactAddressBookMultipleAddressFlag 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
連絡先アイテムごとに複数の電子メール アドレスをプロバイダーがサポートする場合は TRUE にするフラグが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|識別子:  <br/> |0x6614  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |連絡先のアドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティが TRUE の場合、プロバイダーは電子メール アドレスがない連絡先を許可しません。 FALSE の場合、プロバイダーは、通常の電子メール アドレスがあるかどうかすべての連絡先を示します。 プライマリ電子メール アドレスのみが受け入れられます。 これは、連絡先のアドレス帳コンテナー、および連絡先のアドレス帳コンテナーのテーブル内の列のプロパティです。
  
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

