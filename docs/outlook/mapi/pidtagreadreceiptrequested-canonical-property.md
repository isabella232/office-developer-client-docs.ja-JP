---
title: PidTagReadReceiptRequested 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0e49b73c777988ad3559a442af920af3d8f4bdbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356470"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a>PidTagReadReceiptRequested 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信者がメッセージを読み取ったときにメッセージ送信者がメッセージ システムに読み取りレポートを生成する場合は TRUE を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_READ_RECEIPT_REQUESTED  <br/> |
|識別子:  <br/> |0x0029  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |メール  <br/> |
   
## <a name="remarks"></a>注釈

**PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) および PR_READ_RECEIPT_SEARCH_KEY ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) プロパティの値を検証するには、このプロパティを **TRUE** に設定する必要があります。
  
メッセージング システムが **読み取りレポートを生成する前** に、PR_READ_RECEIPT_REQUESTEDを含むメッセージが削除または期限切れになった場合は、読み取り以外のレポートが生成されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
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

