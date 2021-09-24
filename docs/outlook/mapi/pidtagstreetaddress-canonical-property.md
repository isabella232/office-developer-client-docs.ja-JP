---
title: PidTagStreetAddress 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStreetAddress
api_type:
- COM
ms.assetid: 41262e7a-5f5f-4830-b80c-f1be3e9a3276
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fbb4ab3696734f60cd0e6399b10bf817d99afe6c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550324"
---
# <a name="pidtagstreetaddress-canonical-property"></a>PidTagStreetAddress 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者の住所を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STREET_ADDRESS、PR_STREET_ADDRESS_A、PR_STREET_ADDRESS_W、PR_BUSINESS_ADDRESS_STREET、PR_BUSINESS_ADDRESS_STREET_A、PR_BUSINESS_ADDRESS_STREET_W  <br/> |
|識別子:  <br/> |0x3A29  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI メール ユーザー  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、受信者の ID とアクセス情報を提供します。 受信者と受信者の組織によって定義されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
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

