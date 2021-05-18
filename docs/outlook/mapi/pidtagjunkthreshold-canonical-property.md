---
title: PidTagJunkThreshold 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 078dfcc7c24870cf95a2a4b2385c34fbeb64fac0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326853"
---
# <a name="pidtagjunkthreshold-canonical-property"></a>PidTagJunkThreshold 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
迷惑メール フォルダーに受信メールを積極的に送信する方法を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_JUNK_THRESHOLD  <br/> |
|識別子:  <br/> |0x6101  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |スパム  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、高/低/なしフィルターの設定に対応します。 "0xFFFFFFFF" の値は、スパム フィルターを適用しない必要があるが、ブロック リストを適用する必要があります。 "0x80000000" の値は、信頼できる送信者リストの送信者からのメッセージ、または信頼できる受信者リストの受信者に送信されたメッセージを除く、すべてのメールがスパムである場合を示します。 この値は次のとおりです。
  
|**値**|**説明**|
|:-----|:-----|
|0xFFFFFFFF  <br/> |スパム フィルターなし  <br/> |
|0x00000006  <br/> |低スパム フィルター  <br/> |
|0x00000003  <br/> |高いスパム フィルター  <br/> |
|0x80000000  <br/> |信頼できるリストのみ  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。
    
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

