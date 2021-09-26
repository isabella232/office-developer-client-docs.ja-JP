---
title: PidTagServiceExtraUids 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 411adc200d4b337eaaa6b51e47269c0f02d9b899
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624497"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>PidTagServiceExtraUids 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービスの追加のプロファイル セクションを識別する [MAPIUID](mapiuid.md) 構造の一覧が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|識別子:  <br/> |0x3D0D  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ フィルターごとに新しいプロファイル セクションを作成できます。 メッセージ サービスに関する情報を別のプロファイルにコピーする場合は、フィルターの追加プロファイル セクションもコピーすることが重要です。 追加のプロファイル セクションを使用するサービス プロバイダーは、これらのプロファイル セクションの **MAPIUID** 構造を PR_SERVICE_EXTRA_UIDS に格納できます **。これにより**、MAPI は追加のメッセージ サービス情報をコピーできます。
  
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

