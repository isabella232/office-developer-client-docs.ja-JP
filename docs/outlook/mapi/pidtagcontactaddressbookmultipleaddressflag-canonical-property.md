---
title: PidTagContactAddressBookMultipleAddressFlag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7ade77c6c519e2c58b45ff60c1748b623e723fbd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571067"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>PidTagContactAddressBookMultipleAddressFlag 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーが連絡先アイテムごとに複数の電子メール アドレスをサポートする場合に TRUE のフラグが含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|識別子:  <br/> |0x6614  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |連絡先アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティが TRUE の場合、プロバイダーは電子メール アドレスのない連絡先を許可しません。 FALSE の場合、プロバイダーは、プライマリ メール アドレスを持っているかどうかに関して、すべての連絡先を表示します。 プライマリ 電子メール アドレスだけが受け入れされます。 これは、連絡先アドレス帳コンテナーのプロパティであり、連絡先アドレス帳コンテナーのテーブル内の列です。
  
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

