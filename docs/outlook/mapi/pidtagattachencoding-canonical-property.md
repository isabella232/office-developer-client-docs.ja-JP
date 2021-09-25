---
title: PidTagAttachEncoding 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9716af43b65b8bbc9b1d2c3b8b0b3d549b635afd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583584"
---
# <a name="pidtagattachencoding-canonical-property"></a>PidTagAttachEncoding 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルのエンコードを指定する ASN.1 オブジェクト識別子が含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_ENCODING  <br/> |
|識別子:  <br/> |0x3702  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、添付ファイル内のデータの変換に使用されるアルゴリズムを識別します。
  
 **メモ** プロパティ **PR_ATTACH_ENCODING****およびPR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) プロパティは混同しないでください。 これらはペアまたは関連付けではありません。 **PR_ATTACH_TAG** 元の添付ファイルを生成したアプリケーションを識別します。 "Object" はオブジェクト識別子という用語で、X.400 ではオブジェクト指向プログラミングよりもずっと一般的な意味を持ちます。 
  
オブジェクト識別子の構文とサンプル オブジェクト識別子は、MAPIOID で定義されます。H ヘッダー ファイル。 値は **PR_ATTACH_ENCODING** MAPIOID.H で定義されている値に限定されません。 たとえば、添付された Macintosh ファイルでは、MacBinary などの識別子を使用できます。 
  
これらのオブジェクト識別子の詳細については、ASN.1、X.208、X.209 のドキュメントを参照してください。 オブジェクト識別子は、FTBP (ファイル転送本文パーツ) 環境のアプリケーション参照要素に含まれる。 
  
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

