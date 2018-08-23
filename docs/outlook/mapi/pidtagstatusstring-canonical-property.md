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
ms.openlocfilehash: ea24b5e721317668c8f43278a5e4c38d73b3e91c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803577"
---
# <a name="pidtagstatusstring-canonical-property"></a>PidTagStatusString 標準プロパティ

  
  
**適用対象**: Outlook 
  
セッション リソースの現在の状態を示すメッセージが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STATUS_STRING、PR_STATUS_STRING_A、PR_STATUS_STRING_W  <br/> |
|識別子:  <br/> |0x3E08  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、サービス ・ プロバイダー、MAPI など、統合されたアドレス帳または特定のサービス プロバイダーのセッション リソースの状態に関する特定の情報を入力する機会を提供します。 このプロパティについて説明し、ステータス コード、または**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) のプロパティの詳細について説明します。 ステータスのすべてのオブジェクトに必要なは、 **PR_STATUS_CODE** 、 **PR_STATUS_STRING**および関連付けられたプロパティは省略可能です。 トランスポート プロバイダーは、値を指定しなければ、MAPI スプーラーは、既定値を提供します。 
  
MAPI スプーラーを無効にすると、リモート プロシージャ コールの同じ側に文字列が生成されます。プロセス境界を越えてマーシャ リングされるのではなく、共有メモリ経由とするとします。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagStatusCode 標準プロパティ](pidtagstatuscode-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

