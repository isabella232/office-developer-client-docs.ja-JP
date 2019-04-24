---
title: PidTagStatusString 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278894"
---
# <a name="pidtagstatusstring-canonical-property"></a>PidTagStatusString 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッションリソースの現在の状態を示すメッセージを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STATUS_STRING、PR_STATUS_STRING_A、PR_STATUS_STRING_W  <br/> |
|識別子:  <br/> |0x3e08  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティによって、サービスプロバイダーと MAPI は、統合されたアドレス帳や特定のサービスプロバイダーなど、セッションリソースの状態に関する特定の情報を提供する機会を提供します。 このプロパティは、状態コードまたは**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティについて説明し、追加情報を提供します。 **PR_STATUS_CODE**はすべての状態オブジェクトに必要ですが、 **PR_STATUS_STRING**と関連付けられたプロパティは省略可能です。 トランスポートプロバイダーで値が指定されていない場合、MAPI スプーラーは既定値を提供します。 
  
文字列は、リモートプロシージャコールの同じ側で MAPI スプーラーとして生成されます。プロセス境界を越えてマーシャリングされるのではなく、共有メモリを経由します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagStatusCode 標準プロパティ](pidtagstatuscode-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

