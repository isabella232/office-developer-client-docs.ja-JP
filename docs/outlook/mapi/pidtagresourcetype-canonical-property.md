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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1c7a35ded4861d724520b02ec5d61246774ca5cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330129"
---
# <a name="pidtagresourcetype-canonical-property"></a>PidTagResourceType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービスプロバイダの種類を示す値を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOURCE_TYPE  <br/> |
|識別子:  <br/> |0x3e03  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、次のいずれかの値を指定できます。
  
MAPI_AB 
  
> アドレス帳
    
MAPI_AB_PROVIDER 
  
> アドレス帳プロバイダー
    
MAPI_HOOK_PROVIDER 
  
> スプーラーフックプロバイダー
    
MAPI_PROFILE_PROVIDER 
  
> プロファイルプロバイダ
    
MAPI_SPOOLER 
  
> メッセージスプーラー
    
MAPI_STORE_PROVIDER 
  
> メッセージストアプロバイダー
    
MAPI_SUBSYSTEM 
  
> MAPI の内部サブシステム
    
MAPI_TRANSPORT_PROVIDER 
  
> トランスポートプロバイダー
    
## <a name="related-resources"></a>関連リソース

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

