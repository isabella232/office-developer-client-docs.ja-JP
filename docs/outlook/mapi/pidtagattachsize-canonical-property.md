---
title: PidTagAttachSize の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2d6b585c00ffb3d9dd5fb0864d98b0a221c7d8c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802499"
---
# <a name="pidtagattachsize-canonical-property"></a>PidTagAttachSize の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
添付ファイルのすべてのプロパティのサイズの合計 (バイト単位) にはが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_SIZE  <br/> |
|識別子:  <br/> |0x0e20 が使えるはず  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

サブオブジェクトの添付ファイルが、 **PR_ATTACH_SIZE**プロパティを公開することをお勧めします。 **PR_ATTACH_SIZE**に含まれている合計には、 **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) または**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) のプロパティのサイズが含まれています。 したがって、 **PR_ATTACH_SIZE**は、通常、単独での添付ファイルの内容より大きくです。 
  
モデム経由でリモートの転送を実行する前に添付ファイルのおおよそのサイズを確認し、添付ファイルをディスクに保存するときに進行状況インジケーターを表示するのには、このプロパティを使用できます。 添付された OLE オブジェクトで特に便利です。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagMessageSize の標準的なプロパティ](pidtagmessagesize-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

