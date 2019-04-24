---
title: PidTagOriginalSensitivity 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e712a4cc49541ee4330f479d7a03af323bdbc887
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341231"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a>PidTagOriginalSensitivity 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの最初のバージョンの送信者によって割り当てられた、転送または返信される前のメッセージの秘密度の値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_SENSITIVITY  <br/> |
|識別子:  <br/> |0x002e  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

クライアントアプリケーションでは、メッセージが最初に送信されるときに、このプロパティを**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) プロパティと同じ値に設定する必要があります。 後で変更することはできません。
  
このプロパティは、コピーしたエントリの感度を保護するためにトランスポートプロバイダーによって使用されます。 これにより、 **SENSITIVITY_PRIVATE**として最初にマークされたメッセージの転送または返信時に、元のメッセージテキストの変更をブロックすることができます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
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

