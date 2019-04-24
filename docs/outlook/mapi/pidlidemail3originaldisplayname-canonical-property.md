---
title: PidLidEmail3OriginalDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail3OriginalDisplayName
api_type:
- COM
ms.assetid: f3fa392a-c3b1-46dd-bf9b-5ce310719542
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e69bcde35bcfec7746893ee18423aca3a24a6c4a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338074"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a>PidLidEmail3OriginalDisplayName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先に対して指定されている電子メールアドレスに対応する3番目の表示名を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidEmail3OriginalDisplayName  <br/> |
|プロパティセット:  <br/> |PSETID_Address  <br/> |
|ロング ID (LID):  <br/> |0x000080a4  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>解説

**dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) プロパティの値が "SMTP" の場合、それぞれの**dispidEmail3OriginalDisplayName**プロパティの値は、それぞれ**のプロパティの値と等しくなければなりません。dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)) このプロパティの目的は、 **dispidEmail3EmailAddress**にあるものと同等の代替のユーザーフレンドリアドレスを表示することです。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

