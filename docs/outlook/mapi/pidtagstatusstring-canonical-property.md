---
title: PidTagStatusString 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f1c82448e3989ca45676e1347d86ca1f53ed9062
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599390"
---
# <a name="pidtagstatusstring-canonical-property"></a>PidTagStatusString 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッション リソースの現在の状態を示すメッセージが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STATUS_STRING、PR_STATUS_STRING_A、PR_STATUS_STRING_W  <br/> |
|識別子:  <br/> |0x3E08  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティを使用すると、サービス プロバイダーと MAPI は、統合アドレス帳や特定のサービス プロバイダーなど、セッション リソースの状態に関する特定の情報を提供できます。 このプロパティは、状態コードまたはプロパティ[(PidTagStatusCode)](pidtagstatuscode-canonical-property.md)プロパティPR_STATUS_CODE説明し、その他の情報を提供します。  すべての状態 **PR_STATUS_CODE** 必要な場合は、PR_STATUS_STRING **関連付** けられているプロパティは省略可能です。 トランスポート プロバイダーが値を指定しない場合、MAPI スプーラーは既定値を提供します。 
  
この文字列は、MAPI スプーラーと同じ側のリモート プロシージャ呼び出しで生成されます。プロセス境界を越えてマーシャリングされるのではなく、共有メモリを通過します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagStatusCode 標準プロパティ](pidtagstatuscode-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

