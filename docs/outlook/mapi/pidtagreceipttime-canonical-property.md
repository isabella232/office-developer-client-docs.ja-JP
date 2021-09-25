---
title: PidTagReceiptTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReceiptTime
api_type:
- COM
ms.assetid: 9c6cd2f4-e769-4786-b9cc-c02641fecc4f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5ca1561704ee79f762b0143065b98be59db9563b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616405"
---
# <a name="pidtagreceipttime-canonical-property"></a>PidTagReceiptTime 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
配信レポートが生成される日時を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECEIPT_TIME  <br/> |
|識別子:  <br/> |0x002A  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |MAPI 封筒  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、元のメッセージを受信し、レポートを生成するメッセージ ストア プロバイダーによって設定する必要があります。 
  
## <a name="related-resources"></a>関連リソース

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

