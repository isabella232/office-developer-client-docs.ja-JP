---
title: PidTagToDoItemFlags の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: cae4ef6e4d7634ca2b429eb946aa948f5d90cd92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803672"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>PidTagToDoItemFlags の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
To do アイテムのフラグが設定された状態を表します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|識別子:  <br/> |0x0E2B  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、ビット フィールドの各ビットが 1 に設定する次の表に関連付けられている条件を適用する場合は 0 です。
  
||||
|:-----|:-----|:-----|
|数値  <br/> |名前  <br/> |説明  <br/> |
|存在しません。  <br/> |該当なし  <br/> |フラグなし  <br/> |
|1  <br/> |todoTimeFlagged  <br/> |オブジェクトは、フラグが設定された時間です。  <br/> |
|8  <br/> |todoRecipientFlagged  <br/> |下書きメッセージ オブジェクトにのみ設定する必要があり、受信者のオブジェクトのフラグが設定されていることを意味します。  <br/> |
   
テーブルで指定されていないすべてのビットは予約されています。 これらは、無視する必要がありますが、設定されている場合に保持されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> プロパティ フラグに関連する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

