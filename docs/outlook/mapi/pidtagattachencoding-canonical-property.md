---
title: PidTagAttachEncoding の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: cdeb432e20f2779bbb625566108551748b48a01f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802480"
---
# <a name="pidtagattachencoding-canonical-property"></a>PidTagAttachEncoding の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
添付ファイルのエンコーディングを指定する ASN.1 オブジェクト識別子が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_ENCODING  <br/> |
|識別子:  <br/> |0x3702  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、添付ファイル内のデータを変換するためのアルゴリズムを識別します。
  
 **メモ****PR_ATTACH_ENCODING**および**PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) のプロパティとは違います。 ペアにしたり、関連にはしないでください。 **PR_ATTACH_TAG**は、最初の添付ファイルを生成したアプリケーションを識別します。 「オブジェクト」には、オブジェクト指向プログラミングでよりもより一般的な意味では、用語のオブジェクト識別子では X.400 があります。 
  
オブジェクトの識別子の構文と例のオブジェクト識別子は、MAPIOID で定義されます。H ヘッダー ファイルです。 **PR_ATTACH_ENCODING**の値は、MAPIOID で定義されている制限付きではありません。H. たとえば、Macintosh の添付ファイルは、MacBinary など識別子を使用することができます。 
  
これらのオブジェクト識別子の詳細については、ASN.1、X.208、X.209 のマニュアルを参照してください。 FTBP (ファイル転送のボディ部) 環境の要素の参照がアプリケーションのオブジェクト識別子が検索されます。 
  
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

