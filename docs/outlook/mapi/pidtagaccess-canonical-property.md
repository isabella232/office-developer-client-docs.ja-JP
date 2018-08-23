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
ms.openlocfilehash: bb00d4e0e1437f9b3c13ac5e7d0a9dc4f3610d32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802416"
---
# <a name="pidtagaccess-canonical-property"></a>PidTagAccess 標準プロパティ

  
  
**適用対象**: Outlook 
  
オブジェクトのクライアントに利用可能な操作を示すフラグのビットマスクを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ACCESS  <br/> |
|識別子:  <br/> |0x0FF4  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |コントロール プロパティにアクセスします。  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、クライアントに対しては読み取り専用です。 ビットごと**または**次の表の値を 0 個以上の必要があります。 
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |書き込み  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |Read  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0x00000004  <br/> |削除  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0x00000008  <br/> |フォルダー階層のサブフォルダーを作成します。  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0x00000010  <br/> |内容のメッセージを作成します。  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0x00000020  <br/> |コンテンツに関連するメッセージを作成します。  <br/> |
   
MAPI_ACCESS_DELETE、MAPI_ACCESS_MODIFY、および MAPI_ACCESS_READ のフラグがあるフォルダーとメッセージのオブジェクトと**PR_ACCESS**列の内容のテーブルと関連付けられている内容のテーブルで。 Folder オブジェクトだけでは、MAPI_ACCESS_CREATE_ASSOCIATED、MAPI_ACCESS_CREATE_CONTENTS、および MAPI_ACCESS_CREATE_HIERARCHY のフラグが見つかりました。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

