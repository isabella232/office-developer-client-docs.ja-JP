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
ms.openlocfilehash: 95729474db29fe21f808ec5c8f571bec4600db70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336324"
---
# <a name="pidtagsearchattachments-canonical-property"></a>PidTagSearchAttachments 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストア上の添付ファイルコンテンツで照会されている Unicode 文字列が格納されています。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SEARCH_ATTACHMENTS_W  <br/> |
|識別子:  <br/> |0x0EA5  <br/> |
|プロパティの種類:  <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |検索  <br/> |
   
## <a name="related-resources"></a>関連リソース

> [!NOTE]
> 添付ファイルのコンテンツを検索するときに使用されるこの MAPI 制限タグは、現在持っているダウンロード可能なヘッダーファイルでは定義されていない場合があります。 コードに追加するには、次の値を使用します。 >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`
  
### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Microsoft Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> 検索フォルダーリストの構成を操作するためのプロパティと操作を指定します。
    
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

