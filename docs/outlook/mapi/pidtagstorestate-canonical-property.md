---
title: PidTagStoreState 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreState
api_type:
- COM
ms.assetid: 36e49cf5-1411-42c5-9112-09958243996d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8f00addf7abdd765d97c54350e46979f788f06ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341154"
---
# <a name="pidtagstorestate-canonical-property"></a>PidTagStoreState 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアの状態を示すフラグが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STORE_STATE  <br/> |
|識別子:  <br/> |0x340e  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI メッセージストア  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは動的であり、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティとは異なり、ユーザー操作に基づいて変更できます。 
  
次の値を設定できます。
  
STORE_HAS_SEARCHES 
  
> ユーザーがストア内に1つ以上のアクティブな検索を作成しました。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> コアメッセージストアオブジェクトに対する許容される操作を指定します。
    
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

