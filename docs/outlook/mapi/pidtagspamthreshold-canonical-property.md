---
title: PidTagSpamThreshold 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2b2d6b8e-e3dd-4a9b-8bb5-53add675605d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d43a0229f232f9437d1746799534c0f2d6fba83f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346313"
---
# <a name="pidtagspamthreshold-canonical-property"></a>PidTagSpamThreshold 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
スパム フィルターのレベルを示す長い値。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SPAM_THRESHOLD  <br/> |
|長い ID (LID):  <br/> | 0x041B  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |スパム  <br/> |
   
## <a name="values"></a>値

スパム フィルターの値は次のとおりです。
  
|**スパム レベル**|**値**|
|:-----|:-----|
|なし  <br/> |0xFFFFFFFF  <br/> |
|低い  <br/> |0x00000006  <br/> |
|中  <br/> |0x00000005  <br/> |
|高い  <br/> |0x00000003  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのMicrosoft Exchange Serverを提供します。
    
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

