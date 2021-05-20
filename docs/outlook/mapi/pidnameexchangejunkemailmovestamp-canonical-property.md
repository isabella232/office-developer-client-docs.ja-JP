---
title: PidNameExchangeJunkEmailMoveStamp 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameExchangeJunkEmailMoveStamp
api_type:
- COM
ms.assetid: 7a52f46c-371c-46d0-8d66-e154482e8269
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 098261cd71631e4816d22272e1b1bef1d5932a94
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540946"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a>PidNameExchangeJunkEmailMoveStamp 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが既に処理済みか安全かのどちらかなので、メッセージをスパム フィルターで処理しなけいというメッセージの永続化された値を格納します。
  
|||
|:-----|:-----|
|分名:  <br/> |なし  <br/> |
|プロパティ セット:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|プロパティ名:  <br/> |http://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |セキュリティで保護されたメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、迷惑メール ルールによって移動される、または信頼できるコンテンツであるすべてのメッセージにスタンプされます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。
    
[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)
  
> RSS アイテムを表すプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

