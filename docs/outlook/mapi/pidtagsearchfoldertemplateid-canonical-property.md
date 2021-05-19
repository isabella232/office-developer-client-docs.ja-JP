---
title: PidTagSearchFolderTemplateId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bee22a7a435b99f4b94473a3f6eb4b7f32517128
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336625"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a>PidTagSearchFolderTemplateId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
検索に使用されているテンプレートの ID を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_WB_SF_TEMPLATE_ID  <br/> |
|識別子:  <br/> |0x6841  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |検索  <br/> |
   
## <a name="remarks"></a>注釈

検索フォルダーの条件は、テンプレートによって指定されます。 検索フォルダーを定義するメッセージのこのプロパティは、対応するテンプレートを識別します。 テンプレートは、検索条件の定義に加えて、検索から除外するフォルダーを定義し、検索から除外するアイテムを定義し **、PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType)](pidtagsearchfolderstoragetype-canonical-property.md)の値を指定します。
  
検索フォルダー テンプレートの詳細については [、「[MS-OXOSRCH] 」を参照してください](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) 。 
  
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

