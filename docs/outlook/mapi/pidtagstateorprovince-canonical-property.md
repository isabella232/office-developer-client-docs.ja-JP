---
title: PidTagStateOrProvince 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStateOrProvince
api_type:
- COM
ms.assetid: 5f17874f-fab5-4119-b2eb-845c1f70d882
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 81beb448c7cdb65ec44b9106bafa3b1636d9c7fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278842"
---
# <a name="pidtagstateorprovince-canonical-property"></a>PidTagStateOrProvince 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者の都道府県名を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STATE_OR_PROVINCE、PR_STATE_OR_PROVINCE_A、PR_STATE_OR_PROVINCE_W、PR_BUSINESS_ADDRESS_STATE_OR_PROVINCE、PR_BUSINESS_ADDRESS_STATE_OR_PROVINCE_A、PR_BUSINESS_ADDRESS_STATE_OR_PROVINCE_W  <br/> |
|識別子:  <br/> |0x3a28  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI メールユーザー  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、受信者の id とアクセス情報を提供します。 受信者と受信者の組織によって定義されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

