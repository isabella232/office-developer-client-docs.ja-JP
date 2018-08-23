---
title: PidTagProviderDisplay 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDisplay
api_type:
- COM
ms.assetid: 62e96db8-4c3e-4f73-b695-99eb4b2396fd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a37382cda1a96025f950d941f83fb5b6a0497bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565502"
---
# <a name="pidtagproviderdisplay-canonical-property"></a>PidTagProviderDisplay 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
サービス プロバイダーのベンダー定義の表示名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_DISPLAY、PR_PROVIDER_DISPLAY_A、PR_PROVIDER_DISPLAY_W  <br/> |
|識別子:  <br/> |0x3006  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |一般的な MAPI  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティと**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) は、サービス プロバイダーに属するプロファイル セクションでのみ定義されます。 MAPISVC.INF に存在する必要があります。
  
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

