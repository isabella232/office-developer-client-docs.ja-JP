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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0deb1b34a437d47ab53cdb2e13cda006d9116f65
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570122"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>PidTagServiceExtraUids 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ サービスの追加のプロファイル セクションを識別する[MAPIUID](mapiuid.md)構造体の一覧が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|識別子:  <br/> |0x3D0D  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

各メッセージ フィルターの新しいプロファイルのセクションを作成できます。 メッセージ サービスについては、別のプロファイルにコピーするのには、それが同様のフィルターの追加のプロファイル セクションをコピーするのには重要です。 追加のプロファイル セクションを使用するサービス プロバイダーは、 **PR_SERVICE_EXTRA_UIDS**、その他のメッセージ サービスの情報をコピーするのには MAPI を使用するにこれらのプロファイル セクションの**MAPIUID**構造体を格納できます。
  
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

