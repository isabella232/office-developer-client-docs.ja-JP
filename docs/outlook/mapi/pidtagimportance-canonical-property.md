---
title: PidTagImportance 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327924"
---
# <a name="pidtagimportance-canonical-property"></a>PidTagImportance 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの重要度に関するメッセージ送信者の意見を示す値を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IMPORTANCE  <br/> |
|識別子:  <br/> |0x0017  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティと **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) プロパティは混同しないでください。 重要度はユーザーに値を示し、優先度はメッセージをメッセージング システム ソフトウェアによって送信する順序または速度を示します。 優先度が高いほど、通常はコストが高くなります。 重要度が高いほど、通常、ユーザー インターフェイスによって別の表示に関連付けられる。 
  
このプロパティには、次のいずれかの値を指定できます。
  
IMPORTANCE_LOW 
  
> メッセージの重要度が低い。
    
IMPORTANCE_HIGH 
  
> メッセージの重要度が高い。
    
IMPORTANCE_NORMAL 
  
> メッセージの重要度は通常です。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
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

