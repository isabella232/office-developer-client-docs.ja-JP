---
title: PidTagAttachMimeTag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeTag
api_type:
- HeaderDef
ms.assetid: cbc4585d-f970-4b22-ac08-d7fc91bff3d3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f05fa0816db3b412329372ad392c673c240eb59e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389100"
---
# <a name="pidtagattachmimetag-canonical-property"></a>PidTagAttachMimeTag 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
多目的インターネット メール拡張 (MIME) の添付文書に関する書式情報が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_MIME_TAG、PR_ATTACH_MIME_TAG_A、PR_ATTACH_MIME_TAG_W  <br/> |
|識別子:  <br/> |0x370E  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) のプロパティに**OID_MIMETAG**の値が含まれている場合、トランスポート プロバイダーはこれらのプロパティは、添付ファイルの書式を設定する方法を決定するのにを見てください。 
  
これらのプロパティは、受信 MIME ヘッダーのコンテンツ タイプのパラメーターからコピーされます。 文字列の構成は、RFC 1521 ドキュメントで定義されます。 形式は、アプリケーション/バイナリまたはテキスト/形式などは、タイプ/サブタイプです。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限管理でエンコードされたメッセージのプロパティを指定します。
    
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

