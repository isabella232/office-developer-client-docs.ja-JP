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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316514"
---
# <a name="pidtagaccess-canonical-property"></a>PidTagAccess 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトのクライアントで使用できる操作を示すフラグのビットマスクが含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ACCESS  <br/> |
|識別子:  <br/> |0x0FF4  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |アクセス制御のプロパティ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、クライアントの読み取り専用です。 次の表の 0 以上の値のビット形式 **の OR** である必要があります。 
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |書き込み  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |Read  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0x00000004  <br/> |削除  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0x00000008  <br/> |フォルダー階層にサブフォルダーを作成する  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0x00000010  <br/> |コンテンツ メッセージの作成  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0x00000020  <br/> |関連付けられたコンテンツ メッセージを作成する  <br/> |
   
フォルダー MAPI_ACCESS_DELETE、MAPI_ACCESS_MODIFY、MAPI_ACCESS_READ の各フラグは、フォルダーオブジェクトとメッセージ オブジェクト、およびコンテンツ テーブルおよび関連するコンテンツ テーブルの **PR_ACCESS** 列にあります。 フォルダー MAPI_ACCESS_CREATE_ASSOCIATED、MAPI_ACCESS_CREATE_CONTENTS、MAPI_ACCESS_CREATE_HIERARCHYフラグは、フォルダー オブジェクトでのみ検出されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
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

