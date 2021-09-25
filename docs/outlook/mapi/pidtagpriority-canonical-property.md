---
title: PidTagPriority 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: be32e8c8c83305ec759062c523c0567b39239178
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574903"
---
# <a name="pidtagpriority-canonical-property"></a>PidTagPriority 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの相対的な優先度を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PRIORITY  <br/> |
|識別子:  <br/> |0x0026  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メール  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティと **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) プロパティは混同しないでください。 重要度はユーザーに値を示し、優先度はメッセージをメッセージング システム ソフトウェアによって送信する順序または速度を示します。 優先度が高いほど、通常はコストが高くなります。 重要度が高いほど、通常、ユーザー インターフェイスによって別の表示に関連付けられる。
  
レポート メッセージの優先度は、報告される元のメッセージの優先度と同じである必要があります。
  
このプロパティには、次のいずれかの値を指定できます。
  
PRIO_NONURGENT 
  
> メッセージは緊急ではありません。
    
PRIO_NORMAL 
  
> メッセージの優先度は通常です。
    
PRIO_URGENT 
  
> メッセージは緊急です。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
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

