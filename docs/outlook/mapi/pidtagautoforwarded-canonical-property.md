---
title: PidTagAutoForwarded 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAutoForwarded
api_type:
- HeaderDef
ms.assetid: 1ba40cc2-ba27-4d75-9682-c536cf3a0d58
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 49e5e3f84d747210ba42870be5fc328c83bae883
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565901"
---
# <a name="pidtagautoforwarded-canonical-property"></a>PidTagAutoForwarded 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
クライアントは、X-MS の Exchange の組織に自動転送されたヘッダー フィールドを要求した場合、TRUE が格納されます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_AUTO_FORWARDED  <br/> |
|識別子:  <br/> |0x0005  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |一般エラー報告  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティ false を指定または使用していない、X-MS の Exchange の組織に自動転送されたヘッダー フィールドは作成されません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> MS の OXO のプレフィクスの付いたドキュメントで説明されているオブジェクトで使用されている各プロパティを定義します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
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

