---
title: PidTagOriginatorNonDeliveryReportRequested 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorNonDeliveryReportRequested
api_type:
- COM
ms.assetid: 0a19ba44-abb0-4868-9d7d-75184058d4c0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 227ceb468c54cea98519057b2f837a4aee84820c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341959"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a>PidTagOriginatorNonDeliveryReportRequested 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ送信者が特定の受信者の配信不能レポートを要求する場合は、TRUE が含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED  <br/> |
|識別子:  <br/> |0x0c08  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、配信できないメッセージを処理するようにメッセージングシステムに指示するために使用されます。 この場合、メッセージでは、 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) プロパティを FALSE に設定する必要もあります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
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

