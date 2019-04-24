---
title: PidTagSelectable 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359018"
---
# <a name="pidtagselectable-canonical-property"></a>PidTagSelectable 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1回限りのテーブル内の項目を選択できる場合は、TRUE が含まれます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SELECTABLE  <br/> |
|識別子:  <br/> |0x3609  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |アドレス帳コンテナー  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、1回限りのテーブルの表示形式に主に使用されます。 テンプレートは、グループの見出しを示すエントリを作成することによってグループ化できます。 見出しに対してこのプロパティを FALSE に設定すると、ユーザーはグループ内の実際のテンプレートのみを選択できるようになり、この見出しエントリは選択できません。 
  
このプロパティは、アドレス帳の階層テーブルではなく、1回限りのテーブルにのみ適用されます。 
  
MAPI では、アドレス帳プロバイダーは2つの方法でアイテムを視覚的にグループ化することができます。 最初に、特定の行を unselectable にして見出しとして機能させることができます。 次に、 **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) プロパティを使用して、選択可能なアイテムを見出しに対してインデントすることができます。 このプロパティは、このようなグループ化で、この項目をリストから選択して1回限りのアドレスを作成できるかどうかを示します。 たとえば、クライアントに fax アドレスを作成するためのテンプレートがいくつかある場合は、次のように表示できます。 
  
FAX テンプレート (深さ0、選択不可)
  
 ローカル (深さ1、選択可能) 
  
 長距離 (深さ1、選択可能な) 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> アドレス帳テンプレートで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[PidTagFolderType 標準プロパティ](pidtagfoldertype-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

