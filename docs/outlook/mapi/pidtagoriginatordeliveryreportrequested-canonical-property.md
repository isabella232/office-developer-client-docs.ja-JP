---
title: PidTagOriginatorDeliveryReportRequested 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e508f9c3d84272a0641a27e18c94e0620a7072c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574406"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a>PidTagOriginatorDeliveryReportRequested 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージの送信者は、メッセージがメッセージ ・ ストアに配置される前に特定の受信者のメッセージング システムから、配信レポートを要求した場合、TRUE が格納されます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED  <br/> |
|識別子:  <br/> |0x0023  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>注釈

メッセージング システムに配信されるメッセージの処理を指示するこのプロパティを使用します。 この例では、メッセージは**PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) プロパティを FALSE に設定をも提供する必要があります。
  
**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED**プロパティをメッセージの設定は、すべての受信者に対する配信状態レポートを要求する方法です。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
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

