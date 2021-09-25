---
title: PidTagSearchAttachments 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 252c556d08a9073940f7c734f157d735f0c0962a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555063"
---
# <a name="pidtagsearchattachments-canonical-property"></a>PidTagSearchAttachments 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストアの添付ファイルの内容でクエリされている Unicode 文字列が含まれます。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEARCH_ATTACHMENTS_W  <br/> |
|識別子:  <br/> |0x0EA5  <br/> |
|プロパティの種類:  <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |検索  <br/> |
   
## <a name="related-resources"></a>関連リソース

> [!NOTE]
> 添付ファイルの内容を検索するときに使用されるこの MAPI 制限タグは、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。 次の値を使用して、コードに追加できます。>  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`
  
### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのMicrosoft Exchange Server提供します。
    
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

