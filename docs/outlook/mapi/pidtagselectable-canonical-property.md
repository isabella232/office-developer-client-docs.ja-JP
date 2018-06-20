---
title: PidTagSelectable の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 225c435107ba79183c737ddb8e09cda1ffbd83f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803496"
---
# <a name="pidtagselectable-canonical-property"></a>PidTagSelectable の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
一時テーブル内のエントリを選択できる場合、TRUE が格納されます。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SELECTABLE  <br/> |
|識別子:  <br/> |0x3609  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |アドレス帳コンテナー  <br/> |
   
## <a name="remarks"></a>備考

一時テーブルの見た目を整えるためには、主にこのプロパティを使用します。 グループの見出しを示すエントリを作成するテンプレートをグループ化することができます。 見出しの場合は FALSE にこのプロパティの設定により、ユーザーがグループに、この見出しエントリではないので実際のテンプレートのみを選択できます。 
  
このプロパティは、アドレス帳の階層テーブルに、一時テーブルにのみ適用されます。 
  
MAPI は、2 つの方法で視覚的にアイテムをグループ化、アドレス帳プロバイダーを使用できます。 最初に、特定の行は、選択可能なが見出しとして機能できます。 2 つ目は、 **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) プロパティを使用してするには、その見出しを基準にして選択可能な項目がインデントされます。 このプロパティは、一時アドレスを作成するのには、リストからこの項目を選択できるかどうかを示すために、このようなグループ化で使用されます。 などのクライアントは、fax アドレスを作成するためのいくつかのテンプレートには、表示に次のように。 
  
FAX テンプレート (深さ 0、選択不可)
  
 ローカル (深さ 1、選択可能です) 
  
 長距離 (深さ 1、選択可能です) 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> プロパティは、アドレス帳のテンプレートの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[PidTagFolderType の標準的なプロパティ](pidtagfoldertype-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

