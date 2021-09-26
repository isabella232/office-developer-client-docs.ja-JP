---
title: PidTagProviderUid 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 95d42bd6889ca2c8630e2240767a241142aa92d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583248"
---
# <a name="pidtagprovideruid-canonical-property"></a>PidTagProviderUid 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを処理しているサービス プロバイダーの **MAPIUID** 構造を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROVIDER_UID  <br/> |
|識別子:  <br/> |0x300C  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、すべてのサービス プロバイダーによって計算されます。 これは、プロバイダーに [関連付けられた MAPIUID](mapiuid.md) 構造を含み、通常はプロバイダーによってハードコードされます。 通常、特定のプロバイダーによって提供されるアドレス帳コンテナーのみを使用するクライアント アプリケーションで使用されます。 
  
このプロパティは、プロバイダー テーブルの列エントリとしてのみ表示されます。
  
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

