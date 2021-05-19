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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fc2774efed1a15fe79e167149f2cb162bae7642c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358535"
---
# <a name="pidtaginconflict-canonical-property"></a>PidTagInConflict 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルが代替レプリカを表す場合は TRUE を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_IN_CONFLICT  <br/> |
|識別子:  <br/> |0x666C  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |競合に関するメモ  <br/> |
   
## <a name="remarks"></a>注釈

同期中にレプリカの現在のバージョンのメッセージとの競合を検出する場合、電子メール クライアントとサーバーは競合解決メッセージを生成する必要があります。 ローカル レプリカ内のメッセージの現在のバージョンが現在の同期操作中に送信された可能性を理解することが重要です。 これは、競合するメッセージがローカル レプリカにダウンロードされる前に、競合がサーバー上に既に存在する場合に発生します。 競合解決メッセージは、競合する PCL を持つ独立したレプリカとして同期する必要があります。 競合解決メッセージ自体は、クライアントとサーバーの間で同期する必要があります。独立したレプリカのみを交換する必要があります。 同期パートナーは、競合メッセージの構造に一致する新しいメッセージを生成する必要があります。 したがって、クライアントとサーバーが同じアルゴリズムを使用して "勝者" アイテムを検出することが重要です。 "勝者" を検出するには、次のルールを適用する必要があります。
  
1. 最終変更時刻。
    
2. より高い CN GUID (メモリ比較を使用) を使用してタイを破る。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアント間のメッセージング オブジェクト データの同期を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

