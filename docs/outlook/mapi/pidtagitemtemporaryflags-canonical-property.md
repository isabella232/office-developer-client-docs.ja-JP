---
title: PidTagItemTemporaryflags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagItemTemporaryflags
api_type:
- HeaderDef
ms.assetid: 8066de8e-2b77-4bac-8df3-e64b03ee42b9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ec092e6cc6174e156dbfe7784143c9d74715eef7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357702"
---
# <a name="pidtagitemtemporaryflags-canonical-property"></a>PidTagItemTemporaryflags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが読み取り済みで、読み取りとしてマークされていないかどうかを示すフラグが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ITEM_TMPFLAGS  <br/> |
|識別子:  <br/> |0x1097  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、Outlook の [未読メッセージ] 検索フォルダーで使用され、実際に読み取りとしてマークせずに読み取ったメッセージを追跡し、フォルダーから削除します。 ビューが変更されると、このプロパティは削除され、アイテムは読み取りとしてマークされます。 このプロパティは、このプロパティと同期Exchange Server。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
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

