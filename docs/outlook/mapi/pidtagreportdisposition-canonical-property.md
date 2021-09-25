---
title: PidTagReportDisposition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 56b9e7bd-eece-4264-8ee5-a1bcbec4f35c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 574ffba36f96ae370fa70da268b3bfa63627619f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555175"
---
# <a name="pidtagreportdisposition-canonical-property"></a>PidTagReportDisposition 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
受信を要求するメッセージの受信状態を示します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_REPORT_DISPOSITION、PR_REPORT_DISPOSITION_A、PR_REPORT_DISPOSITION_W  <br/> |
|識別子:  <br/> |0x0080  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI 封筒  <br/> |
   
## <a name="remarks"></a>注釈

有効な値は次のとおりです。
  
- "deleted"
    
- "処理"
    
- "dispatched"
    
- "denied"
    
- "failed"
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]] 
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
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

