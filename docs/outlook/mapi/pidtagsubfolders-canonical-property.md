---
title: PidTagSubfolders 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubfolders
api_type:
- COM
ms.assetid: b456b07b-4d83-46bf-a305-4f322ea7dbd1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: acde7f18324d5642f7b8f8b5aa25721c4019ce3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803604"
---
# <a name="pidtagsubfolders-canonical-property"></a>PidTagSubfolders 標準プロパティ

  
  
**適用対象**: Outlook 
  
フォルダーにサブフォルダーが含まれている場合、TRUE が格納されます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SUBFOLDERS  <br/> |
|識別子:  <br/> |0x360A  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |MAPI のコンテナー  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ ・ ストアは、すべてのフォルダーに対してこのプロパティを指定しなければなりません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダーの操作を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

