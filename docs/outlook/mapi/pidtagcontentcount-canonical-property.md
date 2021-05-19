---
title: PidTagContentCount 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCount
api_type:
- HeaderDef
ms.assetid: 27c75031-a968-4636-98a6-4a5b7422f57c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7e9994da72bbc38a546f220e5ecf8768b80c6f1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331956"
---
# <a name="pidtagcontentcount-canonical-property"></a>PidTagContentCount 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストアによって計算されるフォルダー内のメッセージの数を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTENT_COUNT  <br/> |
|識別子:  <br/> |0x3602  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ ストアによって計算されるこのプロパティは、関連する 2 つの異なる目的で使用されます。 MapiFolder オブジェクトには、フォルダー内のメッセージの数が含まれます。 分類された MAPI テーブルの見出し行には、その見出し行に対応するカテゴリ内の関連付けされていないメッセージの数が含まれます。
  
このプロパティに含まれる番号には、フォルダーに関連付けられたエントリは含めされません。 **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md)) には、フォルダーの未読メッセージの数が含まれます。 クライアント アプリケーションは、このプロパティとプロパティを読み取り、変更 **PR_CONTENT_UNREAD。** 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのMicrosoft Exchange Server提供します。
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> コア テーブル オブジェクトに対して許容される操作が含まれます。
    
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

