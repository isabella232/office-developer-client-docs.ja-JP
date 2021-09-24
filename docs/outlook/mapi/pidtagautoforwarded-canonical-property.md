---
title: PidTagAutoForwarded 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAutoForwarded
api_type:
- HeaderDef
ms.assetid: 1ba40cc2-ba27-4d75-9682-c536cf3a0d58
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9c0f87108f2ce0b40c0aa53f873db6ee9299604f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550828"
---
# <a name="pidtagautoforwarded-canonical-property"></a>PidTagAutoForwarded 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントが X-MS-Exchange-Organization-AutoForwarded ヘッダー フィールドを要求する場合は TRUE を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_AUTO_FORWARDED  <br/> |
|識別子:  <br/> |0x0005  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |一般的なレポート  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティを FALSE に設定するか使用しない場合、X-MS-Exchange-Organization-AutoForwarded ヘッダー フィールドは作成されません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> MS-OXO プレフィックス付きドキュメントで記述されているオブジェクトで使用される各プロパティを定義します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

