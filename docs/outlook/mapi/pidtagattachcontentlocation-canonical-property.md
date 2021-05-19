---
title: PidTagAttachContentLocation 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentLocation
api_type:
- HeaderDef
ms.assetid: af2f776c-1b77-4942-827a-4363eda3924f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f279d8ea305c0b1e609881b15e39653c41d5828e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345480"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a>PidTagAttachContentLocation 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多目的インターネット メール拡張機能 (MIME) メッセージ添付ファイルのコンテンツの場所ヘッダーを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_CONTENT_LOCATION、PR_ATTACH_CONTENT_LOCATION_A、PR_ATTACH_CONTENT_LOCATION_W  <br/> |
|識別子:  <br/> |0x3713  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、MHTML のサポートに使用されます。 これらは、適切な MIME 本文パーツのコンテンツの場所ヘッダーを表します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
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

