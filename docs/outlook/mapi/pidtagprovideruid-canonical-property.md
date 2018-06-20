---
title: PidTagProviderUid の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7a42a3b50cfa5630ac66cb03caac06dd7cb00e6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803212"
---
# <a name="pidtagprovideruid-canonical-property"></a>PidTagProviderUid の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージを処理するサービス プロバイダーの**MAPIUID**構造体が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_PROVIDER_UID  <br/> |
|識別子:  <br/> |0x300C  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |一般的な MAPI  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、すべてのサービス プロバイダーによって計算されます。 [MAPIUID](mapiuid.md)構造体には、関連付けられている、通常、ハードコーディングによって、プロバイダーが含まれています。 通常は、特定のプロバイダーから提供されているアドレス帳コンテナーのみに興味を持っているクライアント アプリケーションによって使用されます。 
  
このプロパティは、プロバイダーのテーブルの列のエントリとしてのみ表示されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

