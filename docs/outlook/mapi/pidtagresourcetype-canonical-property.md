---
title: PidTagResourceType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceType
api_type:
- COM
ms.assetid: 48b634d7-deea-422b-8944-a8d929d83838
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1c7a35ded4861d724520b02ec5d61246774ca5cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434957"
---
# <a name="pidtagresourcetype-canonical-property"></a>PidTagResourceType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーの種類を示す値を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOURCE_TYPE  <br/> |
|識別子:  <br/> |0x3E03  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、次のいずれかの値を指定できます。
  
MAPI_AB 
  
> アドレス帳
    
MAPI_AB_PROVIDER 
  
> アドレス帳プロバイダー
    
MAPI_HOOK_PROVIDER 
  
> スプーラー フック プロバイダー
    
MAPI_PROFILE_PROVIDER 
  
> プロファイル プロバイダー
    
MAPI_SPOOLER 
  
> メッセージ スプーラー
    
MAPI_STORE_PROVIDER 
  
> メッセージ ストア プロバイダー
    
MAPI_SUBSYSTEM 
  
> 内部 MAPI サブシステム
    
MAPI_TRANSPORT_PROVIDER 
  
> トランスポート プロバイダー
    
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

