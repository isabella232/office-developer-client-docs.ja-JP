---
title: PidTagOrganizationalIdNumber 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOrganizationalIdNumber
api_type:
- COM
ms.assetid: 124b9f05-032d-42f1-a3d3-4f4c9b9f7a06
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3df9f163418deca45ebe7d842daae45ee9cfb13c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342687"
---
# <a name="pidtagorganizationalidnumber-canonical-property"></a>PidTagOrganizationalIdNumber 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
従業員 ID 番号など、連絡先の組織 ID 番号が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORGANIZATIONAL_ID_NUMBER、PR_ORGANIZATIONAL_ID_NUMBER_A、PR_ORGANIZATIONAL_ID_NUMBER_W  <br/> |
|識別子:  <br/> |0x3A10  <br/> |
|データの種類 :   <br/> |PT_UNICODE、PT_STRING8  <br/> |
|エリア:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>注釈

これらはオプションのプロパティです。 これらの使用は、メッセージング ユーザーまたは組織によって決まります。
  
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
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

