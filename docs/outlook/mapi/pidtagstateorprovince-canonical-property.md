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
ms.openlocfilehash: 72f6bc791d9b27e4c9120c059ab7636672e5fa29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573090"
---
# <a name="pidtagstateorprovince-canonical-property"></a>PidTagStateOrProvince 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
受信者の都道府県の名前が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STATE_OR_PROVINCE、PR_STATE_OR_PROVINCE_A、PR_STATE_OR_PROVINCE_W、PR_BUSINESS_ADDRESS_STATE_OR_PROVINCE、PR_BUSINESS_ADDRESS_STATE_OR_PROVINCE_A、PR_BUSINESS_ADDRESS_STATE_OR_PROVINCE_W  <br/> |
|識別子:  <br/> |0x3A28  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI メール ユーザー  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。 受信者と受信者の組織によって定義されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

