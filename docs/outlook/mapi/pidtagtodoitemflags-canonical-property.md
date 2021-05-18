---
title: PidTagToDoItemFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6ddc7231afef0a224b92be7fe86216e56200ab70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284484"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>PidTagToDoItemFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アイテムのフラグTo-Do条件を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|識別子:  <br/> |0x0E2B  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティはビット フィールドで、次の表の関連する条件が適用される場合は各ビットを 1 に設定し、それ以外の場合は 0 に設定します。
  
||||
|:-----|:-----|:-----|
|数値  <br/> |名前  <br/> |説明  <br/> |
|存在しない  <br/> |該当なし  <br/> |フラグが設定されていない  <br/> |
|1  <br/> |todoTimeFlagged  <br/> |オブジェクトに時間フラグが設定されている  <br/> |
|8  <br/> |todoRecipientFlagged  <br/> |下書きメッセージ オブジェクトにのみ設定する必要があります。つまり、オブジェクトに受信者のフラグが設定されます。  <br/> |
   
テーブルで指定されていないビットはすべて予約済みです。 これらは無視する必要がありますが、設定されている場合は保持する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
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

