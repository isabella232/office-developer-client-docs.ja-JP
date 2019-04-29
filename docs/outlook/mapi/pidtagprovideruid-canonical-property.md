---
title: PidTagProviderUid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0d79075ea1db451e0c3d327df9a662e5032ebb22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422776"
---
# <a name="pidtagprovideruid-canonical-property"></a>PidTagProviderUid 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを処理するサービスプロバイダーの**MAPIUID**構造体が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_UID  <br/> |
|識別子:  <br/> |0x300c  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、すべてのサービスプロバイダーによって計算されます。 この構造体には、に関連付けられ、通常はプロバイダーによってハードコーディングされた[MAPIUID](mapiuid.md)構造が含まれています。 通常、特定のプロバイダーによって提供されるアドレス帳コンテナーのみを対象とするクライアントアプリケーションによって使用されます。 
  
このプロパティは、プロバイダテーブルの列エントリとしてのみ表示されます。
  
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

