---
title: PidLidHtml 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidHtml
api_type:
- COM
ms.assetid: 5598cbaf-cb9a-4d3a-b123-9108a7aa7c1c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c6ac6ad0d6fad3e6dfc2f98b04adc4ef1af6b4b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600597"
---
# <a name="pidlidhtml-canonical-property"></a>PidLidHtml 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先のビジネス Web ページ URL を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidHTML  <br/> |
|プロパティ セット:  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x0000802B  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値が存在する場合は、プロパティ ([PidTagBusinessHomePage](pidtagbusinesshomepage-canonical-property.md) **)** プロパティのPR_BUSINESS_HOME_PAGEと同じ値を指定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

