---
title: PidTagCorrelate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4f1b039de0d61c4adbeea25b1d85a073c1a6370b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600275"
---
# <a name="pidtagcorrelate-canonical-property"></a>PidTagCorrelate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの送信者がメッセージング システムの相関機能を要求する場合は TRUE を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CORRELATE  <br/> |
|識別子:  <br/> |0x0E0C  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、受信レポートと元の送信メッセージとの相関関係を要求するために使用されます。 トランスポート プロバイダーは **、PR_CORRELATE** が TRUE に設定された送信済みメッセージを検出すると **、PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) プロパティをそのメッセージのメッセージ転送システム (MTS) 識別子に設定します。
  
  PR_CORRELATE、X.400 などの MTS 識別子による相関関係をサポートするメッセージング システムで使用する必要があります。 
  
## <a name="related-resources"></a>関連リソース

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

