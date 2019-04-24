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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 07acfd8715dccad8833ee14ac8e573fb995539ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337948"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a>PidNameExchangeJunkEmailMoveStamp 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが既に処理されているか、または安全なので、メッセージがスパムフィルターによって処理されないことを示す永続的なメッセージ値が格納されています。
  
|||
|:-----|:-----|
|フレンドリ名:  <br/> |なし  <br/> |
|プロパティセット:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|プロパティ名:  <br/> |https://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |セキュリティで保護されたメッセージング  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、迷惑メールルールによって移動されるすべてのメッセージ、または信頼できるコンテンツとしてスタンプされます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/ブロックリストの処理と、迷惑メールメッセージの決定を有効にします。
    
[[OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)
  
> RSS アイテムを表すプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

