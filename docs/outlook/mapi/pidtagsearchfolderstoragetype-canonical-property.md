---
title: PidTagSearchFolderStorageType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderStorageType
api_type:
- COM
ms.assetid: 1ec21942-47db-43a5-a6ee-ec6fd2135e8b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: accea8bdea25ac44e6cc5d8fe88cb32caf1961be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336408"
---
# <a name="pidtagsearchfolderstoragetype-canonical-property"></a>PidTagSearchFolderStorageType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ ([PidTagSearchFolderDefinition](pidtagsearchfolderdefinition-canonical-property.md)) プロパティに表示されるバイナリ ラージ オブジェクト (BLOB) データをPR_WB_SF_DEFINITIONフラグが含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_WB_SF_STORAGE_TYPE  <br/> |
|識別子:  <br/> |0x6846  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |検索  <br/> |
   
## <a name="remarks"></a>注釈

フラグの定義は [[MS-OXOSRCH] で指定します](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)。 [検索] を **PR_WB_SF_STORAGE_TYPE** します。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> 検索フォルダー 一覧の構成を操作するためのプロパティと操作を指定します。
    
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

