---
title: PidTagOtherTelephoneNumber 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOtherTelephoneNumber
api_type:
- COM
ms.assetid: 60b11733-20c2-4fe9-8406-c3103b2852ba
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d9c3fc0eb5b14df27885ec835058f29f9693fb1b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584774"
---
# <a name="pidtagothertelephonenumber-canonical-property"></a>PidTagOtherTelephoneNumber 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者の別の電話番号が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_OTHER_TELEPHONE_NUMBER、PR_OTHER_TELEPHONE_NUMBER_A、PR_OTHER_TELEPHONE_NUMBER_W  <br/> |
|識別子:  <br/> |0x3A1F  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティでは、識別を提供し、受信者の情報にアクセスします。 受信者とその構造によって定義されます。 
  
以外の受信者のオフィス、ホーム、またはオフィスでの電話番号では、これらのプロパティが使用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティは、アドレス帳のテンプレートの許可の操作を指定します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
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

