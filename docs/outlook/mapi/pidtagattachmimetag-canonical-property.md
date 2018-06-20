---
title: PidTagAttachMimeTag の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6f65d67903fa9ebb255345f8666cd53de5512cab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802491"
---
# <a name="pidtagattachmimetag-canonical-property"></a>PidTagAttachMimeTag の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
多目的インターネット メール拡張 (MIME) の添付文書に関する書式情報が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_MIME_TAG、PR_ATTACH_MIME_TAG_A、PR_ATTACH_MIME_TAG_W  <br/> |
|識別子:  <br/> |0x370E  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) のプロパティに**OID_MIMETAG**の値が含まれている場合、トランスポート プロバイダーはこれらのプロパティは、添付ファイルの書式を設定する方法を決定するのにを見てください。 
  
これらのプロパティは、受信 MIME ヘッダーのコンテンツ タイプのパラメーターからコピーされます。 文字列の構成は、RFC 1521 ドキュメントで定義されます。 形式は、アプリケーション/バイナリまたはテキスト/形式などは、タイプ/サブタイプです。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限管理でエンコードされたメッセージのプロパティを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

