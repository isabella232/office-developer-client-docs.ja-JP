---
title: PidTagInConflict 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fc2774efed1a15fe79e167149f2cb162bae7642c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358535"
---
# <a name="pidtaginconflict-canonical-property"></a>PidTagInConflict 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルが代替レプリカを表す場合は TRUE が含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IN_CONFLICT  <br/> |
|識別子:  <br/> |0x666c  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |競合メモ  <br/> |
   
## <a name="remarks"></a>解説

同期中にレプリカ内のメッセージの現在のバージョンに対して競合を検出する場合、電子メールクライアントとサーバーは競合の解決メッセージを生成する必要があります。 現在の同期操作中にローカルレプリカ内のメッセージの現在のバージョンが転送された可能性があることを理解しておくことが重要です。 これは、競合しているメッセージがローカルレプリカにダウンロードされる前に、サーバー上に競合が既に存在する場合に発生します。 競合を解決するメッセージは、pcls が競合している独立したレプリカとして同期する必要があります。 競合を解決するメッセージ自体は、クライアントとサーバーの間で同期してはなりません。独立したレプリカのみを交換する必要があります。 同期パートナーは、競合メッセージの構造に一致する新しいメッセージを生成する必要があります。 そのため、クライアントとサーバーが同じアルゴリズムを使用して "勝者" アイテムを検出することが重要です。 "勝者" を検出するには、次のルールを適用する必要があります。
  
1. 最終変更日時。
    
2. 関連付けを解除するために、より高い CN GUID (メモリ比較を使用)。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアントの間でメッセージオブジェクトデータの同期を処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

