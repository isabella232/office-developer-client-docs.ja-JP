---
title: PidTagAttachTag 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d8d8d32bddb98e0ac180b0898478c67297980492
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802517"
---
# <a name="pidtagattachtag-canonical-property"></a>PidTagAttachTag 標準プロパティ

  
  
**適用対象**: Outlook 
  
添付ファイルを提供するアプリケーションを指定する ASN.1 オブジェクト識別子が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_TAG  <br/> |
|識別子:  <br/> |0x370A  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、最初の添付ファイルを生成したアプリケーションを識別します。
  
 **メモ****PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) と**PR_ATTACH_TAG**のプロパティとは違います。 ペアにしたり、関連にはしないでください。 **PR_ATTACH_ENCODING**では、添付ファイル内のデータを変換するためのアルゴリズムを識別します。 「オブジェクト」より一般的な意味では、用語のオブジェクト識別子、および X.400 の使用法よりオブジェクト指向プログラミング。 
  
オブジェクトの識別子の構文と例のオブジェクト識別子は、MAPIOID で定義されます。H ヘッダー ファイルです。 **PR_ATTACH_TAG**の値は、MAPIOID で定義されている制限付きではありません。H. 
  
これらのオブジェクト識別子の詳細については、ASN.1、X.208、X.209 のマニュアルを参照してください。 ファイル転送の本文パーツ (FTBP) 環境の要素の参照がアプリケーションのオブジェクト識別子が検索されます。 
  
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



[PidTagAttachMimeTag 標準プロパティ](pidtagattachmimetag-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

