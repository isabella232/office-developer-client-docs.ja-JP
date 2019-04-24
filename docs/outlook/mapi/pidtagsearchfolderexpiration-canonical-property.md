---
title: PidTagSearchFolderExpiration 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderExpiration
api_type:
- COM
ms.assetid: e5746090-c850-4e95-b1e7-a07e42c87179
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a119bb735f752719d292371d4dc43e72450b33c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336471"
---
# <a name="pidtagsearchfolderexpiration-canonical-property"></a>PidTagSearchFolderExpiration 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
検索フォルダーコンテナーが古くなり、更新または再作成が必要になる時刻を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_WB_SF_EXPIRATION  <br/> |
|識別子:  <br/> |0x683a  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |検索  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、1601年1月1日の午前0時 (UTC) からの分数を分単位で書式設定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
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

