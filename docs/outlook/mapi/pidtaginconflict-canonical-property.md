---
title: PidTagInConflict の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 573e0ba37d4117d85193933a3a5045b5060fbd3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802858"
---
# <a name="pidtaginconflict-canonical-property"></a>PidTagInConflict の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
添付ファイルが別のレプリカを表す場合、TRUE が格納されます。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_IN_CONFLICT  <br/> |
|識別子:  <br/> |0x666C  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |競合メモ  <br/> |
   
## <a name="remarks"></a>備考

電子メール クライアントとサーバーは、レプリカの同期中にメッセージの現在のバージョンとの競合を検出すると、競合解決メッセージを生成する必要があります。 ローカルのレプリカに、メッセージの現在のバージョンが現在の同期操作中に転送されることができることを理解する重要です。 競合既にが存在する場合、サーバー上でローカルのレプリカに矛盾したメッセージのいずれかにダウンロードされた前にこの行われます。 競合を解決すると、メッセージが競合する Pcl を持つ独立したレプリカと同期する必要があります。 メッセージ自体は、クライアントとサーバー間で同期されませんする必要があります、競合の解決します。独立したレプリカのみを交換する必要があります。 同期パートナーは、競合のメッセージの構造に一致する新しいメッセージを生成する必要があります。 したがって、クライアントとサーバーのどちらが「勝者」の項目を検出するために同じアルゴリズムを使用することがあります。 「勝者」を検出するためには、次の規則を適用する必要があります。
  
1. 最終変更時刻です。
    
2. (メモリの比較を使用して) 以上の CN GUID リンク付けを解除します。
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアントの間のメッセージングのオブジェクト データの同期を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

