---
title: PidTagSearchFolderEfpFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderEfpFlags
api_type:
- COM
ms.assetid: ef82a75f-a09f-4880-ba6a-e739b16422a3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d670aa91cc60c051f8464f9d83536b888b44ca9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336429"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a>PidTagSearchFolderEfpFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
検索フォルダーの検索フォルダーコンテナーに適用する拡張フォルダーフラグが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_WB_SF_EFP_FLAGS  <br/> |
|識別子:  <br/> |0x684 8  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |検索  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、フォルダーのフィールド b に、 **PR_EXTENDED_FOLDER_FLAGS** ([PidTagExtendedFolderFlags](pidtagextendedfolderflags-canonical-property.md)) プロパティと**extendedflags**サブプロパティのフラグが明示的に含まれている必要があります。 フォルダーフラグの詳細については、 [[OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)を参照してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> 検索フォルダーリストの構成を操作するためのプロパティと操作を指定します。
    
[[OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> カテゴリの共有リストや稼働時間など、クライアントおよびサーバーの構成データの場所とプロパティを指定します。
    
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

