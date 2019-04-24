---
title: PidTagAccess 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316514"
---
# <a name="pidtagaccess-canonical-property"></a>PidTagAccess 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトに対してクライアントが使用できる操作を示すフラグのビットマスクを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ACCESS  <br/> |
|識別子:  <br/> |0x0ff4  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |アクセス制御のプロパティ  <br/> |
   
## <a name="remarks"></a>解説

このプロパティはクライアントに対して値の取得のみ可能です。 このパラメーターは、次**** の表の0個以上の値のビット単位の or 演算である必要があります。 
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |書き込み  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |読み取り  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0x00000004  <br/> |削除  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0x00000008  <br/> |フォルダー階層にサブフォルダーを作成する  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0x00000010  <br/> |コンテンツメッセージを作成する  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0x00000020  <br/> |関連するコンテンツメッセージを作成する  <br/> |
   
MAPI_ACCESS_DELETE、MAPI_ACCESS_MODIFY、および MAPI_ACCESS_READ フラグは、フォルダーとメッセージオブジェクト、および contents tables および関連する contents テーブルの**PR_ACCESS**列にあります。 MAPI_ACCESS_CREATE_ASSOCIATED、MAPI_ACCESS_CREATE_CONTENTS、および MAPI_ACCESS_CREATE_HIERARCHY フラグは、folder オブジェクトでのみ検出されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
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

