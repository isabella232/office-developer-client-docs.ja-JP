---
title: PidTagAttachAdditionalInformation の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 83de3a4ad7c93b2dfee8063ab63bfbf0724a5f61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802454"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a>PidTagAttachAdditionalInformation の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
Windows 以外の添付ファイルのファイルの種類の情報を提供します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_ADDITIONAL_INFO  <br/> |
|識別子:  <br/> |0x370F  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、添付ファイルのエンコーディングに基づいて、特定の添付ファイルに関するメタデータを提供します。 たとえば、 **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) のプロパティには、MacBinary が含まれている、 **PR_ATTACH_ADDITIONAL_INFO**が含まれています、Macintosh のファイルの作成者とファイルの種類を":CREA:TYPE"として書式設定を表す文字列にはエンコード済みの Macintosh のファイルです。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
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

