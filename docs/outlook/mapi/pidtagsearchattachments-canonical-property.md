---
title: PidTagSearchAttachments 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 008dd69f5e31b601b678a4346880e6b3c89a0f39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803484"
---
# <a name="pidtagsearchattachments-canonical-property"></a>PidTagSearchAttachments 標準プロパティ

  
  
**適用対象**: Outlook 
  
ストア内の添付ファイルの内容の照会中に Unicode 文字列が含まれています。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEARCH_ATTACHMENTS_W  <br/> |
|識別子:  <br/> |0x0EA5  <br/> |
|プロパティの種類:  <br/> |PT_UNICODE  <br/> |
|領域:  <br/> |検索  <br/> |
   
## <a name="related-resources"></a>関連リソース

> [!NOTE]
> 添付ファイルの内容を検索するときに使用されるこの MAPI 制限タグは可能性があります、現在あるダウンロード可能なヘッダー ファイルで定義されていません。 次の値を使用して、コードに追加できます >。`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`
  
### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
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

