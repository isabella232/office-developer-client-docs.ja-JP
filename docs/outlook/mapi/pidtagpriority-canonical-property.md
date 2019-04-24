---
title: PidTagPriority 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339432"
---
# <a name="pidtagpriority-canonical-property"></a>PidTagPriority 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの相対的な優先度を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PRIORITY  <br/> |
|識別子:  <br/> |0x0026  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |電子メール  <br/> |
   
## <a name="remarks"></a>解説

このプロパティと**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) プロパティを混同しないようにしてください。 重要度ユーザーにとっての値を示します。 priority は、メッセージングシステムソフトウェアがメッセージを送信する順序または速度を示します。 通常、高い優先度は、高いコストを示します。 通常、ユーザーインターフェイスによって、より重要度が異なるディスプレイに関連付けられます。
  
レポートメッセージの優先度は、報告される元のメッセージの優先度と同じである必要があります。
  
このプロパティには、次のいずれかの値を指定できます。
  
PRIO_NONURGENT 
  
> メッセージが不急ではない。
    
PRIO_NORMAL 
  
> メッセージは通常の優先度を持っています。
    
PRIO_URGENT 
  
> メッセージが緊急である。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。
    
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

