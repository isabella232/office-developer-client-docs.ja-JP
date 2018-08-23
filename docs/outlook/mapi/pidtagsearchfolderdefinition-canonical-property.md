---
title: PidTagSearchFolderDefinition 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2f17f273afc3f2537195cde21c7bc30626b13a26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573203"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a>PidTagSearchFolderDefinition 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
検索条件を指定するデータが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_WB_SF_DEFINITION  <br/> |
|識別子:  <br/> |0x6845  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |検索  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティに含まれるバイナリ ラージ オブジェクト (BLOB) の各フィールドの特定のコンテンツは、 **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)) のプロパティで指定されているテンプレートの ID に依存します。 BLOB の構造と検索テンプレートの詳細については、 [[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)を参照してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。
    
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

