---
title: PidTagServiceExtraUids 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0fb688e2a845186224c1802f9df2ac537d5bb4d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422307"
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

