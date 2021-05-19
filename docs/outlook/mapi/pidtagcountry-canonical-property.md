---
title: PidTagCountry 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCountry
api_type:
- HeaderDef
ms.assetid: c9470496-fb37-4019-ae1b-b4f93ac55048
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 85a0421c8ce364ed75850c2b330ae0a54a5fed9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357912"
---
# <a name="pidtagcountry-canonical-property"></a>PidTagCountry 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者の国/地域の名前が含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_COUNTRY、PR_COUNTRY_A、PR_COUNTRY_W、PR_BUSINESS_ADDRESS_COUNTRY、PR_BUSINESS_ADDRESS_COUNTRY_A、PR_BUSINESS_ADDRESS_COUNTRY_W  <br/> |
|識別子:  <br/> |0x3A26  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、受信者に関する識別情報とアクセス情報を提供するプロパティの例です。 これらのプロパティは、受信者と受信者の組織によって定義されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リスト オブジェクトに対して許容されるプロパティと操作を指定します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

