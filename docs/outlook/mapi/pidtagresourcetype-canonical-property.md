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
ms.openlocfilehash: 56f14488812842d5e9fe63ae228c325059ebe679
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575092"
---
# <a name="pidtagresourcetype-canonical-property"></a>PidTagResourceType 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
サービス プロバイダーの種類を示す値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOURCE_TYPE  <br/> |
|識別子:  <br/> |0x3E03  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、次の値の 1 つだけ持つことができます。
  
MAPI_AB 
  
> アドレス帳
    
MAPI_AB_PROVIDER 
  
> アドレス帳プロバイダー
    
MAPI_HOOK_PROVIDER 
  
> スプーラー フック プロバイダー
    
MAPI_PROFILE_PROVIDER 
  
> プロファイル プロバイダー
    
MAPI_SPOOLER 
  
> スプーラーのメッセージ
    
MAPI_STORE_PROVIDER 
  
> メッセージ ストア プロバイダー
    
MAPI_SUBSYSTEM 
  
> MAPI サブシステムの内部
    
MAPI_TRANSPORT_PROVIDER 
  
> トランスポート プロバイダー
    
## <a name="related-resources"></a>関連リソース

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

