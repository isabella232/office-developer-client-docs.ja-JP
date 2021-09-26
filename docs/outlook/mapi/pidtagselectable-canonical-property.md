---
title: PidTagSelectable 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 74dfc2b0976f8a27f892caa45de05ff660c5b94b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624504"
---
# <a name="pidtagselectable-canonical-property"></a>PidTagSelectable 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一時テーブル内のエントリを選択できる場合は TRUE を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SELECTABLE  <br/> |
|識別子:  <br/> |0x3609  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |アドレス帳コンテナー  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、主に 1 回のテーブルの視覚的な書式設定に使用されます。 テンプレートは、グループの見出しを示すエントリを作成してグループ化できます。 見出しに対してこのプロパティを FALSE に設定すると、ユーザーはグループ内の実際のテンプレートのみを選択し、この見出しエントリは選択できます。 
  
このプロパティは、アドレス帳階層テーブルではなく、1 回限定のテーブルにのみ適用されます。 
  
MAPI を使用すると、アドレス帳プロバイダーは 2 つの方法でアイテムを視覚的にグループ化できます。 最初に、特定の行は選択できない状態で見出しとして機能します。 次に、選択できる項目を見出しに対してインデントするには、PR_DEPTH **(** [PidTagDepth](pidtagdepth-canonical-property.md)) プロパティを使用します。 このプロパティは、このアイテムをリストから選択して 1 回きりアドレスを作成できるかどうかを示すために、このようなグループ化で使用されます。 たとえば、クライアントに FAX アドレスを作成する複数のテンプレートがある場合、次のように表示できます。 
  
FAX テンプレート (深度 0、選択不可)
  
 ローカル (深度 1、選択可能) 
  
 長距離 (深度 1、選択可能) 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> アドレス帳テンプレートで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[PidTagFolderType 標準プロパティ](pidtagfoldertype-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

