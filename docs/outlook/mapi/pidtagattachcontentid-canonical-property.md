---
title: PidTagAttachContentId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentId
api_type:
- HeaderDef
ms.assetid: 46f31089-3b66-41a2-8094-e3db52464b9f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 78b157dfb11eb7e97d90142a148e3741e3d818d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572649"
---
# <a name="pidtagattachcontentid-canonical-property"></a>PidTagAttachContentId 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
多目的インターネット メール拡張 (MIME) メッセージの添付ファイルのコンテンツの識別のヘッダーが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_CONTENT_ID、PR_ATTACH_CONTENT_ID_A、PR_ATTACH_CONTENT_ID_W  <br/> |
|識別子:  <br/> |0x3712  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティの使用は、MHTML をサポートするためです。 適切な MIME ボディ部のコンテンツの識別のヘッダーを表します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
## <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

