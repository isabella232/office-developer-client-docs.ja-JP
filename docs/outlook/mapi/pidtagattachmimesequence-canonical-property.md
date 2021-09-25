---
title: PidTagAttachMimeSequence 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachMimeSequence
api_type:
- HeaderDef
ms.assetid: d2a84f24-b4a5-4e16-9219-7a579a31a8f8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d85e13b6b8217bbe0d77304525b740a96e2816fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563855"
---
# <a name="pidtagattachmimesequence-canonical-property"></a>PidTagAttachMimeSequence 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MIME メッセージ添付ファイルの MIME シーケンス番号を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_MIME_SEQUENCE  <br/> |
|識別子:  <br/> |0x3710  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メッセージ添付ファイルのプロパティ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、MHTML のサポートに使用されます。 これは、MIME メッセージの親 MIME マルチパート本文部分内の添付ファイルのシーケンス番号を表します。
  
## <a name="related-resources"></a>関連リソース

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

